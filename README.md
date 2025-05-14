#  COVID-19 Data Analysis with MySQL

## Overview

This project analyzes global COVID-19 data using **MySQL**. The goal was to practice SQL skills by exploring real-world pandemic data and answering key questions about cases, deaths, and trends.

## Tools Used

- MySQL
- COVID-19 dataset from https://ourworldindata.org/covid-deaths

## Project Files
Split the data into two tables in Excel to simplify the visualization
- `covid_deaths.xlsx` 
- `covid_data.xlsx` 

## Key Questions Answered

- Total Cases vs Total Deaths
- Total cases vs population

## Example Query

```sql
- Total Cases vs Total Deaths
Select Location, date, total_cases,total_deaths, (total_deaths/total_cases)*100 as DeathPercentage
From PortfolioProject..CovidDeaths
Where location like '%states%'
and continent is not null 
order by 1,2

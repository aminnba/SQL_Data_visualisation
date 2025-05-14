# 🦠 COVID-19 Data Analysis with MySQL

## Overview

This project analyzes global COVID-19 data using **MySQL**. The goal was to practice SQL skills by exploring real-world pandemic data and answering key questions about cases, deaths, and trends.

## Tools Used

- MySQL
- COVID-19 dataset from https://ourworldindata.org/covid-deaths

## Project Files
Split the data into two tables in SQL to simplify the visualisation
- `covid_deaths.` 
- `covid_data.` 

## Key Questions Answered

- Which countries had the highest number of cases and deaths?
- What is the global death rate?
- How did the pandemic change over time?

## Example Queries

```sql
-- Total cases by country
SELECT location, MAX(total_cases) AS total_cases
FROM covid_data
GROUP BY location
ORDER BY total_cases DESC;

-- Global death rate
SELECT 
  SUM(total_deaths) / SUM(total_cases) AS global_death_rate
FROM covid_data;

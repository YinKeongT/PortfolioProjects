# PortfolioProjects

FILE 1:BigQuery.txt
It is a SQL and Tableau project on Covid-19 cases, death and vaccinations
Dataset is downloaded from https://covid.ourworldindata.org/data/owid-covid-data.xlsx
Dataset is separated into 2 files - CovidDeath.csv and CovidVaccination.csv
Upload CovidDeath and CovidVaccination into BigQuery
Query to check data uploaded correctly
Conduct data exploration by using queries
Create Table with summary of total cases, total deaths and percent death for visualization in Tableau later

FILE 2: Data Cleaning Portfolio Project Queries.sql
It is a data cleaning project using Microsoft SQL Server Management Studio on property sales transactions in Nashville
Dataset is downloaded from https://github.com/AlexTheAnalyst/PortfolioProjects/blob/main/Nashville%20Housing%20Data%20for%20Data%20Cleaning.xlsx
File is imported into Microsoft SSMS
Cleaning Step 1: Standardize Date Format by removing time from SaleDate Column by adding column SaleDateConverted (command ADD, SET + CONVERT)
Cleaning Step 2: Populate missing property address Update table a (NashvilleHousing) by Do SELF JOIN to find values to Populate into PropertyAddress = NULL; followed by SET PropertyAddress to ISNULL(column to be changed,column to be inserted)
Cleaning Step 3(a): Separate PropertyAddress to Address, City and State by using SUBSTRING, CHARINDEX and LEN
Cleaning Step 3(b): Add Tables OwnerSplitState, OwnerSplitCity and OwnerSplitAddress by Using ALTER TABLE NashvilleHousing, ADD <new column name> <schema>, then UPDATE NashvilleHousing, SET <new column>> = PARSENAME(REPLACE) 1 by 1
Cleaning Step 4: Change Y and N to Yes and No in for values in "SoldAsVacant" column using UPDATE function, SET, CASE, WHEN, THEN, ELSE, END
Cleaning Step 5: Check for duplicates using CTE, ROW NUMBER, OVER, PARTITION BY and DELETE rows that are duplicates
Cleaning Step 6: Delete unused column using ALTER TABLE, DROP COLUMN

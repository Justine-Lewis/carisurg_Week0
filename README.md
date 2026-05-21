# CariSurg Week 0 Tasks Repository
Repository for Week 0 CariSurg Programme Submissions

## Project Overview

This repository contains my Week 0, Tutorial 1 submission for the **CariSurg MedTech Pathways** programme.
The notebook focuses on basic Python data exploration and cleaning using a sample emergency triage dataset from the Mercer General Hospital scenario.

The main objective: 
- To clean the `Gender` column by converting inconsistent gender values into a consistent numeric format.

# Task1_CleaningGenderColumn is a Notebook that covers:
- Setting up the Python/Google Colab environment
- Importing common data analysis libraries
- Loading a CSV dataset with `pandas`
- Exploring the dataset structure
- Identifying inconsistent values in the `Gender` column
- Cleaning and remapping the `Gender` column
- Verifying the cleaned results

# Assignment2_DataCleaningFiO2: Data Cleaning Groupwork – FiO2 Column

This assignment focused on cleaning and preparing selected columns from the emergency triage dataset for analysis. 
The group reloaded the reduced dirty dataset from Assignment 1 and re-applied the previous gender cleaning step 
before continuing with additional data exploration and column-specific cleaning.  

### FiO2 Column Cleaning

My assigned column was `Fio2`, which represents the fraction of inspired oxygen given to a patient. 
The column was already stored as a float, but it still required inspection and cleaning.

The following steps were completed:

1. Checked the data type and unique values in the `Fio2` column.
2. Checked the number of missing values and the value range.
3. Created a histogram and box plot to visualize the FiO2 distribution.
4. Defined the valid FiO2 range as **21% to 100%**.
5. Checked for values outside the valid clinical range.
6. Replaced invalid values with `NaN`.
7. Filled missing FiO2 values using the mode.

### Results

After cleaning, the `Fio2` column had:

- No invalid out-of-range values
- Missing values filled with the mode
- A final range of **21.0 to 100.0**
- No remaining missing values

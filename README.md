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

# Assignment3_Visualisation: Clinical Data Visualisation

For the student challenge section of Tutorial 3, I created additional visualisations using the cleaned Mercer General Emergency Department dataset. The goal was to produce plots that were clinically meaningful, clearly labelled, and supported by appropriate reference lines.

### 1. Respiratory Rate vs FiO2 Scatter Plot

The first plot explores the relationship between **Respiratory Rate (RR)** and **Fraction of Inspired Oxygen (FiO2)**.

**Clinical question:**  
Do patients with higher respiratory rates tend to receive higher FiO2?

A scatter plot was used because both respiratory rate and FiO2 are numeric variables. Respiratory rate was placed on the x-axis because it can act as an indicator of respiratory distress, while FiO2 was placed on the y-axis to show the level of oxygen support given to the patient.

Clinical reference lines were added at:

- **21% FiO2**, representing room air
- **100% FiO2**, representing maximum oxygen support

This helped make the plot easier to interpret clinically by showing whether patients were receiving normal room air levels or increased oxygen support.

### 2. Respiratory Rate Histogram

The second plot shows the distribution of respiratory rates across patients in the emergency department dataset.

**Clinical question:**  
How are respiratory rates distributed in relation to abnormal adult respiratory rate ranges?

A histogram was used because respiratory rate is one numeric variable, and the goal was to observe its distribution across the dataset. The bins were calculated in intervals of 2 breaths per minute to give a clear view of how respiratory rates were spread.

Clinical reference zones were added for:

- **Bradypnea:** less than 12 breaths per minute
- **Normal/Eupnea:** 12–20 breaths per minute
- **Tachypnea:** greater than 20 breaths per minute

These clinical zones helped show how many patients had respiratory rates within the expected adult range and how many may have shown signs of abnormal breathing patterns.

### Skills Practiced

Through this challenge, I practiced:

- Selecting appropriate plot types based on the data and clinical question
- Using scatter plots to compare two numeric variables
- Using histograms to show the distribution of one numeric variable
- Adding clinical reference lines and shaded zones
- Labelling axes, titles, and legends clearly
- Saving visualisations as PNG files for GitHub and reporting

### Output Files

The visualisations created in this section were saved as:

- `my_plot.png` — Respiratory Rate vs FiO2 scatter plot
- `my_plot2.png` — Respiratory Rate distribution histogram

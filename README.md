# Sales Dataset Cleaning | Excel 

## Overview
This repository contains the original and cleaned versions of a sales dataset. I used Microsoft Excel to clean the data as part of my project.

## Tools Used
- Microsoft Excel
- Raw Bikesales Dataset (From Kaggle: sales_data_orginal.xlsx)

## Cleaning Steps Performed
- First import the data from `Data` section

- Create a new `working sheet` to perform the cleaning task

1. **Removed Duplicates**
   - Used `Remove Duplicates` tool to eliminate repeated rows based on the columns (ID,	Marital Status,	Gender,	 Income, 	Children,	Education,	Occupation, Home Owner,	Cars,	Commute Distance,	Region,	Age,	Purchased Bike)

2. **Standardized The Data For Vizualization**
   - Converted `Marital Status` column to proper format.
     steps involved---> ( ctrl+H ) over `Marital Status` ---> replace (`M` with `Married` and `S` with `Single`)
   - Ensured `Gender` column were replace as (`M` with `Male` and `F` with `Female`)
     
     NOTE:If not changed, there will be a conflict in the final vizualization to what `M` incidates, as it refers to both `Male` and `Married`.
   
3. **Corrected Data Types**
   - Changed `Income` to currency format.
     steps involved ---> click on `Income` on the Home-Tab ---> number section ---> choose currency`$` ---> remove `.00` format  inorder to keep it simple.

4. **Inserted New Column**
   - `Age`column consists of variable distinct values, hence it would be a difficult to show clear insights in the final dashboard
   - So create a new column say `Age Brackets` 
     =IF(M2>55,"Old",IF([@Age]>30,"Middle Aged",IF([@Age]<=30,"Adolescent","Invalid"))) (showing the use case of `NESTED IF` Statement).

5. **Commute Distance Formating**
   - replace `10+ Miles` as `More Than 10 Miles`
   - `ctrl+H` and Replace-All

6. **Created a Clean Version**
   - Saved the cleaned data as `sales_data_cleaned.xlsx`.



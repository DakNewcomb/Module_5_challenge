# Module_5_challenge
Module 5 Challenge


**Background**
You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

**Instructions**
This assignment is broken down into the following tasks:

_Prepare the data._
1. Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.
2. Display the number of unique mouse IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned data frame for the remaining steps.
3. Display the updated number of unique mouse IDs.

_Generate summary statistics._
Create a data frame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

Your summary statistics should include:
 - A row for each drug regimen. These regimen names should be contained in the index column.
 - A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

_Create bar charts and pie charts._
1. Generate two bar charts using Pandas and Matplotlib. Both charts should be identical and show the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study. 
2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

_Calculate quartiles, find outliers, and create a box plot._
1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:
   * Create a grouped data frame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.
   * Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.
   * Loop through each drug in the treatment list, locating the rows in the merged data frame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.
   * Determine outliers by using the upper and lower bounds, and then print the results.
2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.
 
_Create a line plot and a scatter plot._
1. Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.
2. Generate a scatter plot of mouse weight versus the average observed tumor volume for the entire Capomulin treatment regimen.

_Calculate correlation and regression._
1. Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
2. Plot the linear regression model on top of the previous scatter plot.

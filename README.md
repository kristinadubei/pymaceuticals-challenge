# pymaceuticals-challenge

![image](https://github.com/kristinadubei/pymaceuticals-challenge/assets/63558912/b846aa18-791e-4a55-bcca-18264b1743cb)

# Background
I've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, I've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked me with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked for a top-level summary of the study results.

# Process:
This assignment is broken down into the following steps:
1. Preparing the data.
2. Generating summary statistics.
3. Creating bar charts and pie charts.
4. Calculating quartiles, finding outliers, and creating a box plot.
5. Creating a line plot and a scatter plot.
6. Calculating correlation and regression.

### 1. Preparing the Data
Ran the provided package dependency and data imports, and then merged the mouse_metadata and study_results DataFrames into a single DataFrame.
Displayed the number of unique mice IDs in the data, and then checked for any mouse ID with duplicate time points. Displayed the data associated with that mouse ID, and then created a new DataFrame where this data was removed. Used this cleaned DataFrame for the remaining steps. Displayed the updated number of unique mice IDs.

### 2. Generating Summary Statistics
Created a DataFrame of summary statistics. The summary statistics includes:
- A row for each drug regimen. These regimen names contained in the index column.
- A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

### 3. Creating Bar Charts and Pie Charts
Generated two bar charts. Both charts are identical and show the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.
- Created the first bar chart with the Pandas DataFrame.plot() method.
- Created the second bar chart with Matplotlib's pyplot methods.

Generated two pie charts. Both charts are identical and show the distribution of female versus male mice in the study.
- Created the first pie chart with the Pandas DataFrame.plot() method.
- Created the second pie chart with Matplotlib's pyplot methods.

### 4. Calculating Quartiles, Finding Outliers, and Creating a Box Plot
Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculated the quartiles and IQR, and determined if there are any potential outliers across all four treatment regimens. Used the following substeps:
1. Created a grouped DataFrame that shows the last (greatest) time point for each mouse. Merged this grouped DataFrame with the original cleaned DataFrame.
2. Created a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.
3. Looped through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Appended the resulting final tumor volumes for each drug to the empty list.
4. Determined outliers by using the upper and lower bounds, and then printed the results.
5. Using Matplotlib, generated a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlighted any potential outliers in the plot by changing their color and style.

### 5. Creating a Line Plot and a Scatter Plot
Selected a single mouse that was treated with Capomulin, and generated a line plot of tumor volume versus time point for that mouse.
Generated a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

### 6. Calculating Correlation and Regression
Calculated the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
Ploted the linear regression model on top of the previous scatter plot.


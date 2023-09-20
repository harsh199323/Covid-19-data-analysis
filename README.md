# Covid-19-data-analysis

This Python script is designed to create a data visualization dashboard for COVID-19 data using the Dash framework. The code performs the following steps:

It imports necessary libraries including Pandas, NumPy, Plotly Express, and Dash for data manipulation and visualization.

Reads COVID-19 data from a CSV file and converts all columns to string data type.

Creates a new DataFrame with selected columns for analysis (iso_code, continent, location, date, new_deaths, new_cases, new_tests, hospital_beds_per_thousand).

Cleans the data by replacing 'nan' values with zeros and removing rows with missing values in 'iso_code' and 'continent'.

Calculates the month for each row based on the 'date' column and adds 'month_n' and 'month_num' columns to the DataFrame.

Filters the data to exclude the month of December and converts certain columns to the appropriate data types (integers and floats).

Groups the data by 'iso_code', 'continent', 'location', 'month_n', and 'month_num', aggregating the columns 'new_deaths', 'new_cases', 'new_tests', and 'hospital_beds_per_thousand'.

Adds rows for months that are not present in the original dataset to ensure completeness for cumulative calculations.

Calculates cumulative values for deaths, cases, and tests for each location and stores them in new columns ('cumil_deaths', 'cumil_cases', 'cumil_tests').

Initializes a Dash web application with a user interface for selecting visualization options, including a slider for selecting months, dropdowns for selecting data type, geographical scope, and cumulative/non-cumulative data, and a header.

Defines callback functions to update the graphs based on user selections.

Creates choropleth maps to visualize COVID-19 data (deaths, cases, tests) on a geographical map, with the option to display cumulative or non-cumulative data.

Creates a line graph to display cumulative data for deaths, cases, or tests over time for a specific month.

Runs the Dash web application

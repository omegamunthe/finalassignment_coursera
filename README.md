# STOCK-EXTRACTION
# Stock Data Graphing with Python

## Overview

This project entails the creation of a graphing function for visualizing stock data of two companies, Tesla and GameStop. The make_graph function accepts two dataframes as input: stock data and revenue data. The function then generates two subplots within a single figure, presenting the historical share price and revenue of each respective company. The data displayed in the graph is limited to information available up to June 2021.

## Dependencies

Before running the code, make sure you have the necessary libraries installed:

- Pandas
- Plotly
- Beautiful Soup (for web scraping)
- Requests (for web scraping)

## Instructions

### Define Graphing Function

The `make_graph` function takes three inputs: `stock_data`, `revenue_data`, and `stock`. 

- `stock_data`: A dataframe containing historical stock data for a company.
- `revenue_data`: A dataframe containing historical revenue data for a company.
- `stock`: A string representing the name of the stock (e.g., 'Tesla' or 'GameStop').

The function produces a subplot with two rows and one column. The first subplot illustrates historical share prices, while the second subplot visualizes historical revenue.

### Question 1: Extract Tesla Stock Data

To extract Tesla stock data, utilize the yfinance library. Create a ticker object for Tesla using the Ticker function with the ticker symbol "TSLA". Then, use the history function to extract historical stock data for Tesla, saving it in a dataframe named tesla_data. Set the period parameter to "max" to gather information for the maximum available time.

### Question 2: Extract Tesla Revenue Data

To extract Tesla revenue data, implement web scraping with the requests and BeautifulSoup libraries. Download the webpage containing Tesla revenue data from "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm" and store the response's text as html_data. Proceed to parse the HTML data using BeautifulSoup.

Use the read_html function to extract the table featuring Tesla Quarterly Revenue, storing it in a dataframe named tesla_revenue. This dataframe should include columns Date and Revenue. Remove commas and dollar signs from the Revenue column, and eliminate any null or empty rows from the dataframe. Display the last five rows of the tesla_revenue dataframe.

### Question 3: Extract GameStop Stock Data

For GameStop stock data extraction, use the yfinance library similarly to Question 1. Create a ticker object for GameStop with the Ticker function and the ticker symbol "GME". Use the history function to extract historical stock data for GameStop, storing it in a dataframe named gme_data. Set the period parameter to "max" for the maximum available time.

### Question 4: Extract GameStop Revenue Data

To extract GameStop revenue data, follow a web scraping approach similar to Question 2. Download the webpage containing GameStop revenue data from " https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html" and store the response text as html_data. Parse the HTML data using BeautifulSoup.

Use BeautifulSoup or the read_html function to extract the table featuring GameStop Quarterly Revenue, storing it in a dataframe named gme_revenue. The dataframe should include columns Date and Revenue. Remove commas and dollar signs from the Revenue column, and eliminate any null or empty rows from the dataframe. Display the last five rows of the gme_revenue dataframe.

### Question 5: Plot Tesla Stock Graph

Use the make_graph function to graph Tesla stock data. Call the function with the tesla_data and tesla_revenue dataframes, providing the title "Tesla" for the graph.

### Question 6: Plot GameStop Stock Graph

Use the make_graph function to graph GameStop stock data. Call the function with the gme_data and gme_revenue dataframes, and provide the title "GameStop" for the graph.

Note that the provided code assumes you have already installed the required libraries and imported them into your environment. Execute each section of the code sequentially to obtain the desired results.# finalassignment_coursera
# finalassignment_coursera

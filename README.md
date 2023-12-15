# Shripriti_project2
Pandas is a powerful and popular Python library used for data manipulation and analysis. It's widely employed in data science, machine learning, and general data handling tasks. Here's a brief overview of its daily usage and value:

Daily Usage:
Data Reading and Writing: Pandas can read data from various sources like CSV, Excel, SQL databases, HTML, JSON, and more. It enables users to effortlessly load data into a Pandas DataFrame for analysis.

Data Manipulation: Pandas offers a plethora of functions to manipulate data easily. Users can perform tasks like filtering, selecting specific columns, adding or removing rows, transforming data, merging datasets, and handling missing values.

Data Analysis and Exploration: With Pandas, you can quickly analyze and explore your dataset. This includes calculating summary statistics, grouping data, performing statistical operations, and visualizing data using built-in plotting functionality.

Time Series Analysis: Pandas provides robust support for time series data, making it easier to work with dates, time indexes, and time-based calculations
Importing Pandas
To use Pandas, you need to import it first:

python
Copy code
import pandas as pd
Creating a DataFrame
Create a DataFrame using Pandas, typically from a dictionary or other data structures:

python
Copy code
data = {'Column1': [value1, value2, value3],
        'Column2': [value4, value5, value6]}
df = pd.DataFrame(data)
Reading Data
Pandas can read data from various sources:

python
Copy code
# Reading from a CSV file
df = pd.read_csv('file.csv')

# Reading from an Excel file
df = pd.read_excel('file.xlsx')

# Reading from a SQL database
import sqlite3
conn = sqlite3.connect('database.db')
query = "SELECT * FROM table_name"
df = pd.read_sql(query, conn)
Viewing Data
Inspecting the DataFrame:

python
Copy code
# View the first few rows
df.head()

# View the last few rows
df.tail()

# View basic statistics of numerical columns
df.describe()
Selecting and Accessing Data
Accessing specific rows, columns, or elements:

python
Copy code
# Selecting a single column
df['Column1']

# Selecting multiple columns
df[['Column1', 'Column2']]

# Selecting rows by index
df.iloc[index]

# Selecting rows and columns by index
df.iloc[row_index, column_index]

# Conditional selection
df[df['Column1'] > value]
Data Manipulation
Performing various data manipulation operations:

python
Copy code
# Adding a new column
df['NewColumn'] = values

# Removing columns or rows
df.drop('Column1', axis=1)  # Remove a column
df.drop(0, axis=0)  # Remove a row by index

# Handling missing values
df.dropna()  # Drop rows with NaN values
df.fillna(value)  # Fill NaN values with a specific value

# Grouping data
df.groupby('Column1').mean()  # Group by Column1 and calculate mean
Data Visualization
Pandas integrates with Matplotlib for basic plotting:

python
Copy code
import matplotlib.pyplot as plt

# Plotting a column
df['Column1'].plot()

# Scatter plot
df.plot.scatter(x='Column1', y='Column2')
These are just a few basic functionalities of Pandas. The library offers a wide range of methods and functionalities to handle, manipulate, and analyze data efficiently.

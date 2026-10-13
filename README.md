# Python Fundamentals and Data Analysis

A beginner-friendly Jupyter Notebook documenting practical exercises in Python programming, data cleaning, exploration, grouping, and data visualization.

## Project Overview

This project is a learning notebook that progresses from core Python concepts to introductory data analysis with **Pandas** and visualizations with **Matplotlib**. It includes explanations, examples, and practice code intended to help beginners build confidence by working through concepts step by step.

## Learning Objectives

By working through the notebook, you will practise how to:

- Understand Python syntax, variables, data types, and operators.
- Display information and collect user input.
- Work with strings, formatted strings, and common string methods.
- Use conditional statements, loops, lists, and functions.
- Load tabular data into Pandas DataFrames.
- Inspect datasets and summarize their structure.
- Identify and handle missing values and duplicate records.
- Clean text values and convert date columns.
- Select rows and columns and filter records using conditions.
- Group data and calculate summary statistics.
- Create basic charts using Matplotlib.

## Tools and Libraries

- **Python** — programming language used for the exercises.
- **Jupyter Notebook** — interactive environment for code, notes, and outputs.
- **Pandas** — loading, cleaning, exploring, and summarizing tabular data.
- **Matplotlib** — creating charts and visualizing data.

Some notebook examples load the public `tips` dataset from the Seaborn project's GitHub repository. An internet connection is needed to run that particular data-loading cell.

## Notebook Contents

### 1. Python Fundamentals
- Variables and naming rules
- Syntax and syntax errors
- Data types: integers, floating-point numbers, strings, and Boolean values
- `print()` and `input()`
- Formatted strings (f-strings)
- Arithmetic and comparison operators
- String concatenation, repetition, indexing, slicing, and methods
- Conditional logic, loops, lists, and functions

### 2. Working with Tabular Data
- Reading CSV files with `pandas.read_csv()`
- Understanding file paths and the current working directory
- Inspecting data with methods such as `head()`, `info()`, `shape`, `describe()`, and `columns`
- Checking unique values and data types

### 3. Data Cleaning
- Detecting missing values
- Checking and removing duplicate rows
- Standardizing text capitalization and removing extra spaces
- Correcting known spelling inconsistencies
- Converting date values with `pandas.to_datetime()`
- Sorting records by date
- Resetting the DataFrame index
- Saving cleaned data to a CSV file with `to_csv()`

### 4. Selecting and Filtering Data
- Selecting one column or multiple columns
- Selecting rows and columns with `.iloc[]` and `.loc[]`
- Filtering with comparison conditions
- Combining conditions using `&` (AND) and `|` (OR)
- Excluding records with `~`
- Filtering text with `.str.contains()`
- Filtering for a set of values with `.isin()`
- Using `.copy()` when a separate working DataFrame is needed

### 5. Grouping and Aggregation
- Grouping records with `groupby()`
- Calculating sums, averages, minimums, maximums, and counts
- Grouping by one or multiple columns
- Applying multiple aggregation functions with `.agg()`
- Naming aggregated output columns
- Creating a custom aggregation function

### 6. Data Visualization with Matplotlib
The notebook introduces several common chart types:

- Line charts
- Vertical and horizontal bar charts
- Scatter plots
- Histograms
- Pie charts
- Multiple plots in one figure (subplots)
- Titles, axis labels, legends, colors, and reference lines
- Saving a chart to an image file

## Getting Started

### Requirements

Install Python and Jupyter Notebook, or use an environment such as Anaconda that includes them. Install the required libraries if they are not already available:

```bash
pip install pandas matplotlib notebook
```

### Open the notebook

1. Download or clone the project files to your computer.
2. Open Anaconda Navigator or a terminal.
3. Navigate to the folder containing `Exercise.ipynb`.
4. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `Exercise.ipynb` in the browser.
6. Run the cells from top to bottom, reading the explanations and checking each output.

In Jupyter, you can usually run the selected cell with **Shift + Enter**.

## Working with CSV Files

The notebook uses CSV files for data-cleaning practice. Make sure the file is stored in the folder where the notebook is running, or provide the correct file path.

Example:

```python
import pandas as pd

df = pd.read_csv("sales_dirty.csv")
df.head()
```

To check the current working directory:

```python
import os

print(os.getcwd())
```

To save a cleaned DataFrame:

```python
df.to_csv("clean_sales.csv", index=False)
```

`index=False` prevents Pandas from writing the DataFrame index as an extra CSV column. The output file is saved in the current working directory unless a different path is provided.

## Example: Simple Visualization

```python
import matplotlib.pyplot as plt

months = ["Jan", "Feb", "Mar", "Apr", "May"]
sales = [100, 120, 90, 150, 180]

plt.plot(months, sales, label="Sales")
plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.legend()
plt.show()
```

## Suggested Workflow

1. Read the explanation in each Markdown cell.
2. Run the related code cell.
3. Check the output before moving on.
4. Change example values and run the code again.
5. Practise with a small dataset before using a larger one.
6. For data cleaning, inspect the data before and after each change.
7. Save important outputs and keep an untouched copy of the original data.

## Notes and Limitations

- This is a learning notebook, not a packaged Python application.
- The notebook includes examples and exercises across several topics; it is not necessarily organized as a production-ready analysis pipeline.
- File paths such as `sales_dirty.csv` and `clean_sales.csv` depend on the files available in your working directory.
- Online datasets require an internet connection.
- Always inspect changes to missing values, dates, text, and duplicates before treating a dataset as clean.

## Project File

- `Exercise.ipynb` — the main Jupyter Notebook containing lesson notes, code examples, and practice exercises.

## Next Steps

- Complete the exercises without copying the examples first.
- Practise cleaning a small CSV dataset from beginning to end.
- Write a short summary of the main findings from a dataset.
- Create a small collection of clearly labelled charts.
- Build a beginner portfolio project that demonstrates data cleaning, analysis, and visualization.

---

*Created as documentation for the beginner Python and data-analysis learning notebook.*


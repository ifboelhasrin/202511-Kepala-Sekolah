# Data Analysis Project

This project provides tools and examples for analysing data from MySQL databases and Excel files using Jupyter Notebooks.

## Features

- **MySQL Database Connection**: Connect to MySQL databases and execute SQL queries
- **Excel File Reading**: Read single or multiple sheets from Excel files
- **Data Exploration**: Comprehensive data exploration and summary functions
- **Data Cleaning**: Functions to clean and preprocess data
- **Data Visualisation**: Various plotting functions for data analysis
- **Data Merging**: Combine data from MySQL and Excel sources
- **Export Results**: Export analysis results to Excel or CSV

## Setup

### 1. Install Required Libraries

```bash
pip install -r requirements.txt
```

Or install individually:
```bash
pip install pandas numpy mysql-connector-python sqlalchemy openpyxl matplotlib seaborn jupyter
```

### 2. Configure MySQL Connection

Open `data_analysis.ipynb` and update the MySQL configuration in section 3:

```python
MYSQL_CONFIG = {
    'host': 'your_host',
    'database': 'your_database_name',
    'user': 'your_username',
    'password': 'your_password',
    'port': 3306
}
```

### 3. Start Jupyter Notebook

```bash
jupyter notebook
```

Then open `data_analysis.ipynb`

## Usage

1. **Load Data from MySQL**:
   - Configure your database connection
   - Use `query_mysql()` function to execute SQL queries
   - Example: `df_mysql = query_mysql("SELECT * FROM your_table;")`

2. **Load Data from Excel**:
   - Use `read_excel_file()` to read a single sheet
   - Use `read_all_excel_sheets()` to read all sheets
   - Example: `df_excel = read_excel_file('path/to/file.xlsx')`

3. **Explore Data**:
   - Use `explore_data()` to get comprehensive data information
   - Use `clean_data()` to clean and preprocess data

4. **Visualise Data**:
   - `plot_numeric_distribution()`: Distribution plots
   - `plot_categorical_counts()`: Categorical counts
   - `plot_correlation_heatmap()`: Correlation analysis

5. **Combine Data**:
   - Use `merge_dataframes()` to combine MySQL and Excel data

6. **Export Results**:
   - Use `export_to_excel()` or `export_to_csv()` to save results

## Project Structure

```
.
├── data_analysis.ipynb    # Main Jupyter notebook
├── requirements.txt        # Python dependencies
└── README.md              # This file
```

## Notes

- Make sure your MySQL server is running and accessible
- Excel files should be in `.xlsx` or `.xls` format
- All functions include error handling and informative messages
- Examples are provided as comments in the notebook

## Requirements

- Python 3.8+
- MySQL Server (for database analysis)
- Jupyter Notebook or JupyterLab


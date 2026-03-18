# Supermarket Analysis - Pandas .loc Indexing Guide

## Overview
This Jupyter notebook demonstrates data exploration and analysis techniques using a supermarket sales dataset. It focuses on learning pandas label-based indexing with `.loc` and creating visualizations of product distribution.

## Dataset
- **File:** SuperMarket Analysis.csv
- **Description:** Contains supermarket sales transactions with columns including:
  - Gender
  - City
  - Sales
  - Product line
  - Customer type
  - Rating

## Contents

### 1. Data Loading & Exploration
- Load the CSV file using pandas
- Display first few rows and dataset shape
- Show data types and info
- Generate descriptive statistics
- Check for missing values

### 2. Pandas `.loc` Label-Based Indexing Tutorial
This section covers four main `.loc` use cases:

**Selecting rows by index label:**
- Single row selection
- Multiple rows selection

**Selecting rows based on boolean conditions:**
- Filter rows where Gender equals 'Female'

**Selecting specific columns by label:**
- Single column selection
- Multiple columns selection

**Selecting both rows and columns:**
- Combination selections with specific conditions
- Example: Sales and Rating for Members only

### 3. Data Visualization
Uses matplotlib and seaborn to create:
- Countplot showing distribution of products by product line and gender
- Countplot showing distribution of products by product line

## Requirements
```
pandas
matplotlib
seaborn
jupyter
```

## Usage
1. Ensure `SuperMarket Analysis.csv` is in the same directory as the notebook
2. Run the notebook cells in order using Jupyter
3. Each cell demonstrates a specific concept with output visualization

## Key Learning Points
- How to load and explore CSV data with pandas
- Using `.loc` for flexible data selection and filtering
- Creating conditional selections with boolean masks
- Visualizing categorical data distribution with seaborn

## Notes
- The visualizations help understand product popularity across different customer segments
- The `.loc` examples are practical patterns commonly used in data analysis workflows

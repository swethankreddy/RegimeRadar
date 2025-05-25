# RegimeRadar: Detecting Market Moods from Microstructure

## Project Overview

RegimeRadar is a project that introduces students to the intersection of machine learning and financial data by detecting hidden market patterns ("regimes") using unsupervised learning techniques. Since participants may not have prior experience in finance, Week 1 is fully dedicated to strengthening Python fundamentals that are essential for handling data and building models in upcoming weeks.

## Week 1 Assignments: Python Fundamentals

### Assignment 1: Python Installation and Environment Setup

1. **Objective**: Set up a Python development environment to prepare for data processing and ML workflows.
2. **Instructions for Installing Python**:

   * **Windows**:

     1. Download the latest Python installer from the [official Python website](https://www.python.org/downloads/).
     2. Run the installer and ensure you check the box that says "Add Python to PATH."
     3. Complete the installation.
   * **macOS**:

     1. Use Homebrew:

        ```bash
        brew install python
        ```
     2. Or download the installer from [python.org](https://www.python.org/downloads/).
   * **Linux**:

     1. Use your package manager (example for Ubuntu):

        ```bash
        sudo apt update
        sudo apt install python3
        ```
3. **Set Up a Virtual Environment (Optional but Recommended)**:

   ```bash
   pip install virtualenv
   virtualenv regime_env
   # Activate it:
   # Windows:
   regime_env\Scripts\activate
   # macOS/Linux:
   source regime_env/bin/activate
   ```
4. **Install Jupyter Notebook and Basic Libraries**:

   ```bash
   pip install notebook numpy pandas matplotlib
   ```
5. **Launch Jupyter Notebook** and create a new notebook titled `Week1_Setup.ipynb`
6. **Deliverable**: A short note on why isolated environments are useful in collaborative ML projects.

### Assignment 2: Python Basics

1. **Objective**: Strengthen foundational Python skills.
2. **Topics Covered**: Data types, functions, loops, conditionals.
3. **Tasks**:

   * In a Jupyter Notebook, complete the following:

     1. Write a function `calculate_area(radius)` that returns the area of a circle.
     2. Write a function `is_prime(n)` to check if a number is prime.
     3. Create a list from 1 to 50 and print all prime numbers.
     4. Generate a list of squares of the first 10 numbers.
4. **Deliverable**: Submit the `.ipynb` notebook with comments explaining each function and logic.

### Assignment 3: Working with NumPy

1. **Objective**: Learn basic operations with NumPy.
2. **Topics Covered**: Arrays, statistics, slicing, filtering.
3. **Tasks**:

   * Create a 1D NumPy array of 20 random integers between 1 and 100.
   * Calculate the mean, median, and standard deviation.
   * Filter and print only even numbers.
   * Create a 2D array (5x4) and slice the first 3 rows.
4. **Deliverable**: Submit your Jupyter Notebook with clear output and comments.

### Assignment 4: Data Handling with Pandas

1. **Objective**: Learn to manipulate tabular data using Pandas.
2. **Topics Covered**: DataFrames, filtering, basic stats, visualizations.
3. **Tasks**:

   * Load a sample CSV dataset (e.g., Iris or any dataset with numerical columns).
   * Show first 5 rows and dataset summary.
   * Calculate mean and median for numeric columns.
   * Filter rows with a specific condition (e.g., value > threshold).
   * Plot a histogram of a chosen column.
4. **Deliverable**: Submit your Pandas notebook with all tasks completed and explained.

---

# Titanic Dataset Analysis using Python

## Project Overview

This project performs Exploratory Data Analysis (EDA) on the Titanic Dataset using Python. The goal is to understand passenger information, identify missing values, perform data cleaning, and analyze factors affecting passenger survival.

## Dataset

The dataset contains information about Titanic passengers, including:

* PassengerId
* Survived
* Pclass
* Name
* Sex (Gender)
* Age
* Ticket
* Fare
* Embarked

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

## Project Workflow

### 1. Import Libraries

The required Python libraries are imported:

* NumPy
* Pandas
* Matplotlib
* Seaborn

### 2. Load Dataset

The Titanic dataset is loaded using Pandas.

```python
df = pd.read_csv("Titanic-Dataset.csv")
```

### 3. Initial Data Exploration

Basic dataset inspection is performed:

* View first records
* Check column names
* Dataset information
* Summary statistics
* Dataset shape

### 4. Missing Value Analysis

Null values are identified using:

```python
df.isnull().sum()
```

Special attention is given to the Age column.

### 5. Data Cleaning

Unnecessary columns are removed:

* Ticket
* Name
* PassengerId

```python
df.drop(['Ticket'], axis=1, inplace=True)
df.drop(['Name'], axis=1, inplace=True)
df.drop(['PassengerId'], axis=1, inplace=True)
```

### 6. Statistical Analysis

Several statistical operations are performed:

* Total survivors
* Average passenger class
* Minimum age
* Maximum age
* Standard deviation of age

### 7. Feature Analysis

Analysis includes:

* Passenger class distribution
* Embarkation distribution
* Survival statistics

### 8. Data Transformation

Gender values are converted into numerical format:

```python
df['Gender'] = df['Gender'].map({
    'male': 0,
    'female': 1
})
```

### 9. Survival Analysis

Passenger survival rates are analyzed based on different features.

## Results

The project provides insights into:

* Passenger demographics
* Missing data patterns
* Survival trends
* Class distribution
* Gender-based analysis

## How to Run

### Step 1

Clone the repository:

```bash
git clone https://github.com/your-username/titanic-data-analysis.git
```

### Step 2

Move into the project folder:

```bash
cd titanic-data-analysis
```

### Step 3

Install dependencies:

```bash
pip install -r requirements.txt
```

### Step 4

Launch Jupyter Notebook:

```bash
jupyter notebook
```

### Step 5

Open the notebook file and run all cells.

## Future Improvements

* Advanced visualizations
* Feature engineering
* Machine Learning models
* Survival prediction system

## Author

Eisha Younas

Data Analyst | Machine Learning Enthusiast | AI Learner


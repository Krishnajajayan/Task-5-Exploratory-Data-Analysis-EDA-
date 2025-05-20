# Titanic Dataset - Exploratory Data Analysis (EDA)

This repository contains the exploratory data analysis (EDA) for the Titanic dataset. The objective is to understand the data, identify patterns, and explore relationships to predict passenger survival.

## Dataset Overview

The Titanic dataset contains the following features:

- **PassengerId**: Unique ID for each passenger
- **Pclass**: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Name**: Name of the passenger
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings or spouses aboard
- **Parch**: Number of parents or children aboard
- **Ticket**: Ticket number
- **Fare**: Fare paid for the ticket
- **Cabin**: Cabin number
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
- **Survived**: Survival (0 = No, 1 = Yes)

## Objectives

- Perform an exploratory data analysis (EDA) to understand the dataset better.
- Visualize the relationships between features and survival.
- Handle missing data and identify trends in the dataset.

## Steps Taken

1. **Basic Overview**: 
   - Displayed dataset info using `.info()` and basic statistics using `.describe()`.
   - Checked for missing values using `.isnull().sum()`.

2. **Data Cleaning**:
   - Extracted the title from the passenger names and filled missing ages based on the median age within each title group.
   - Filled missing values in the `Embarked` column with the most frequent port of embarkation.
   - Extracted the deck from the `Cabin` column and dropped unnecessary columns (`PassengerId`, `Name`, `Ticket`, `Cabin`).

3. **Visualizations**:
   - **Survival Count**: Visualized the overall survival rate of passengers.
   - **Gender Distribution**: Analyzed the distribution of passengers by gender.
   - **Passenger Class Distribution**: Plotted the distribution of passengers across different classes.
   - **Age Distribution**: Created a histogram to visualize the distribution of passenger ages.
   - **Survival by Gender**: Investigated how survival rates differ between males and females.
   - **Survival by Class**: Explored survival rates across different passenger classes.
   - **Age vs Survival**: Visualized how age relates to survival using a boxplot.
   - **Survival by Title**: Analyzed survival based on the title of the passengers (e.g., Mr, Mrs).
   - **Survival by Deck**: Examined survival rates by the deck extracted from the cabin number.
   - **Survival by Embarked Port**: Plotted survival rates based on the embarkation port.
   - **Correlation Heatmap**: Visualized correlations between numeric features.
   - **Pairplot of Key Features**: Displayed pairwise relationships between age, fare, class, and survival.
   - **Age vs Fare Scatterplot**: Created a scatterplot to examine the relationship between age, fare, and survival.

## Key Observations

- **Survival Rates**:
  - More passengers did not survive than survived.
  - Females had a higher survival rate than males.
  - Passengers in 1st class had significantly higher survival rates than those in 2nd and 3rd classes.

- **Gender Distribution**:
  - There were more male passengers than female passengers.

- **Passenger Class**:
  - Most passengers were from 3rd class, with fewer in 1st and 2nd class.

- **Age Distribution**:
  - Most passengers were between the ages of 20 and 40.

- **Survival Factors**:
  - Younger passengers were more likely to survive.
  - Passengers with titles like 'Mrs' and 'Miss' had higher survival counts compared to 'Mr'.
  - Survival by deck indicated higher survival rates in decks B and C, but many cabins had missing data.

- **Embarked Port**:
  - Passengers who embarked from port 'S' had better survival chances than those from ports 'C' and 'Q'.

- **Fare**:
  - A higher fare seemed to correlate with a higher chance of survival, suggesting that wealth or class may have impacted survival chances.

## Final Summary of Findings

- **Survival**: Survival was strongly influenced by gender, with females having a much higher survival rate.
- **Passenger Class**: First-class passengers had better chances of survival compared to those in lower classes.
- **Age**: Younger passengers were more likely to survive.
- **Titles**: Titles like 'Mrs' and 'Miss' had higher survival counts compared to 'Mr'.
- **Deck and Embarked Port**: The deck had an impact on survival, but missing data made it difficult to draw firm conclusions. Passengers who embarked from port 'S' had better survival rates.
- **Fare**: A positive correlation between fare and survival suggests that wealth or class advantage played a role in survival chances.

## Requirements

- Python 3.x
- Pandas
- Matplotlib
- Seaborn

## Usage

To run the analysis, simply execute the Python script:

```bash
python titanic_eda.py

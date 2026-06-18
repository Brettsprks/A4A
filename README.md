# ACL Recovery Analysis: Relationship Between TSK-11 and AMI Performance Testing

## Project Overview

ACL injuries are becoming more and more common and are one of the most challenging injuries athletes face. While physical recovery is heavily monitored throughout rehabilitation, psychological factors such as fear of movement and reinjury can significantly influence recovery outcomes.

This project investigates the relationship between:

- **TSK-11 (Tampa Scale of Kinesiophobia)** scores
- **AMI (Athletic Movement Index)** performance scores

using rehabilitation data collected from patients at Davis Physical Therapy and Sports Rehab between 2023 and 2025.

The goal is to determine whether psychological readiness is associated with physical performance during recovery and return-to-sport progression.

---

## Research Question

**Can fear of movement (TSK-11) explain variation in athletic performance (AMI) during rehabilitation?**

### Hypothesis

Athletes with lower TSK-11 scores (less fear of movement) will demonstrate higher AMI performance scores.

---

## Dataset

### Source

Davis Physical Therapy and Sports Rehab rehabilitation tracking records.

These tests are done for various injuries such as hips, shoulders and knees. But for this, we are just looking into results with ACL patients. 

### Variables

| Variable | Description |
|-----------|-------------|
| Injury | Injury classification (ACL only) |
| Date of AMI | Date of assessment |
| Level | Rehabilitation progression level |
| Score % | Athletic Movement Index (AMI) score |
| TSK 11 | Tampa Scale of Kinesiophobia score |

### Years Included

- 2023
- 2024
- 2025

### Data Characteristics

- Longitudinal athlete tracking
- Repeated measurements per athlete
- Multiple injury classifications
- Psychological and physical performance metrics
- Real-world rehabilitation data

---

## Project Objectives

1. Clean and organize multi-year rehabilitation data.
2. Investigate trends in AMI and TSK-11 scores.
3. Visualize athlete recovery trajectories.
4. Examine the relationship between psychological readiness and performance.
5. Build predictive models using TSK-11 scores.
6. Demonstrate practical data science skills using healthcare and sports analytics data.

---

## Repository Structure

```text
A4A/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_extraction.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   ├── 04_modeling.ipynb
│   └── 05_final_report.ipynb
│
├── figures/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

## Data Science Workflow

### 1. Data Extraction

- Extracted rehabilitation records from PDF documents
- Consolidated data from multiple years
- Standardized column names and formats

### 2. Data Cleaning

- Removed incomplete observations
- Standardized injury categories
- Converted dates to datetime format
- Handled missing values
- Created athlete identifiers

### 3. Exploratory Data Analysis (EDA)

Investigated:

- AMI score distributions
- TSK-11 score distributions
- Injury frequencies
- Recovery progression trends
- Athlete-specific trajectories

### 4. Statistical Analysis

#### Correlation Analysis

Measured the strength and direction of the relationship between:

```text
TSK-11 Score ↔ AMI Score
```

#### Linear Regression

Model:

```text
AMI Score = β₀ + β₁(TSK-11)
```

Used to evaluate whether fear of movement predicts physical performance.

### 5. Longitudinal Analysis

Tracked individual athletes across multiple rehabilitation visits to visualize:

- Changes in AMI performance
- Changes in TSK-11 scores
- Overall recovery progression

---

## Technologies Used

### Programming

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Jupyter Notebook

### Skills Demonstrated

- Data Extraction
- Data Cleaning
- Data Wrangling
- Exploratory Data Analysis
- Statistical Analysis
- Linear Regression
- Data Visualization
- Longitudinal Analysis
- Research Communication

---

## Key Results

### Correlation Analysis

A correlation analysis was performed to quantify the relationship between TSK-11 and AMI scores.

**Correlation Coefficient:** 0.520431

### Regression Analysis

A linear regression model was developed using TSK-11 scores as a predictor of AMI performance.

**R²:** 0.036

### Observations

- Athletes generally improved AMI scores over time.
- Recovery patterns varied substantially between individuals.
- Psychological readiness appears to contribute to rehabilitation outcomes.

---

## Example Visualizations

### TSK-11 vs AMI Scatter Plot
<img width="696" height="546" alt="image" src="https://github.com/user-attachments/assets/54e54e05-8188-455f-a099-a3fb8172a695" />

Visualizes the relationship between fear of movement and athletic performance.

### Athlete Recovery Trajectories
<img width="785" height="490" alt="image" src="https://github.com/user-attachments/assets/841a891a-4925-46b9-960d-394f6436c897" />

Tracks individual AMI progression across rehabilitation visits.

### Distribution Analysis
<img width="568" height="454" alt="image" src="https://github.com/user-attachments/assets/31db7102-8848-4076-8dcb-273298f5b50d" />
<img width="563" height="453" alt="image" src="https://github.com/user-attachments/assets/ebdf7353-2b7b-47ef-8e4e-e3b5bd74fa46" />

Displays score distributions across the rehabilitation population.

---

## Future Improvements

Potential future work includes:

- Multiple linear regression
- Mixed-effects longitudinal models
- Return-to-sport classification models
- Random Forest and XGBoost prediction models
- Injury-specific subgroup analysis
- Time-to-recovery prediction

---

## Project Impact

This project demonstrates the application of data science techniques to sports medicine and rehabilitation analytics. It combines psychological and physical performance metrics to explore factors influencing athlete recovery while showcasing practical skills in data cleaning, statistical analysis, visualization, and predictive modeling.

---

## Author

### Brett Sparks

Data Science Student  
University of South Carolina

**GitHub:** https://github.com/Brettsprks

---

## License

This project is licensed under the MIT License.

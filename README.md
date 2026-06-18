ACL Recovery Analysis: Exploring the Relationship Between Kinesiophobia and Athletic Movement Index (AMI)
Project Overview

Anterior Cruciate Ligament (ACL) injuries are among the most common injuries in athletics and often require extensive rehabilitation before an athlete can safely return to sport. While physical recovery is heavily monitored, psychological factors such as kinesiophobia (fear of movement/reinjury) can significantly influence rehabilitation outcomes.

This project investigates whether TSK-11 (Tampa Scale of Kinesiophobia) scores are associated with AMI (Athletic Movement Index) performance scores during rehabilitation.

Using longitudinal rehabilitation data collected between 2023–2025, I cleaned, transformed, analyzed, and visualized athlete recovery trajectories to examine:

How fear of movement changes over time
Whether lower TSK-11 scores correspond to higher AMI performance
Recovery trends across individual athletes
The predictive power of TSK-11 for estimating AMI outcomes

The dataset contains repeated measurements from athletes recovering from ACL injuries and other orthopedic conditions, with AMI scores and TSK-11 assessments collected across multiple rehabilitation visits.

Research Question

Can psychological readiness (TSK-11 score) explain variation in physical performance (AMI score) among athletes undergoing rehabilitation?

Hypothesis

Higher levels of kinesiophobia will be associated with lower AMI performance scores.

Dataset
Source

Data were provided by Athletes for Athletes (A4A) rehabilitation program records.

Variables
Variable	Description
Injury	Injury type (ACL, knee, ankle, hip, etc.)
Date of AMI	Assessment date
Level	Rehabilitation progression stage
Score %	Athletic Movement Index performance score
TSK 11	Tampa Scale of Kinesiophobia score

Example entries include repeated AMI and TSK-11 measurements for athletes across multiple rehabilitation stages.

Years Included
2023 rehabilitation records
2024 rehabilitation records
2025 rehabilitation records
Project Structure
A4A/
│
├── data/
│   ├── raw/
│   │   ├── DAVIS_PTSR_AMI_Tracking_2023.pdf
│   │   ├── DAVIS_PTSR_AMI_Tracking_2024.pdf
│   │   └── DAVIS_PTSR_AMI_Tracking_2025.pdf
│   │
│   └── processed/
│       ├── combined_acl_dataset.csv
│       └── cleaned_acl_dataset.csv
│
├── notebooks/
│   ├── 01_data_extraction.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   ├── 04_modeling.ipynb
│   └── 05_final_report.ipynb
│
├── visualizations/
│   ├── correlation_scatter.png
│   ├── patient_progression.png
│   ├── tsk_distribution.png
│   └── regression_results.png
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
Methodology
1. Data Extraction
Parsed rehabilitation tracking PDFs
Extracted AMI scores and TSK-11 values
Consolidated records across years
2. Data Cleaning
Removed incomplete observations
Standardized injury classifications
Converted dates to datetime format
Filtered ACL-specific observations
Handled missing TSK-11 values
3. Exploratory Data Analysis

Investigated:

AMI score distribution
TSK-11 score distribution
Individual recovery trajectories
Year-to-year trends
Injury-specific outcomes
4. Statistical Analysis
Correlation Analysis

Measured strength and direction of relationship between:

TSK-11 ↔ AMI Score
Linear Regression

Model:

AMI Score = β₀ + β₁(TSK-11)

Used to estimate how much variability in AMI scores can be explained by fear of movement.

5. Longitudinal Analysis

Tracked athletes with multiple assessments to visualize:

Recovery progression
Changes in kinesiophobia
Physical performance improvement
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn (if used)
Scikit-Learn
Jupyter Notebook
Data Science Skills Demonstrated
Data extraction
Data cleaning
Feature engineering
Exploratory Data Analysis
Statistical analysis
Linear regression
Data visualization
Longitudinal data analysis
Research communication
Key Findings
Relationship Between Fear and Performance
Lower TSK-11 scores generally corresponded with improved AMI performance.
Psychological readiness appears to play a role in rehabilitation outcomes.
Longitudinal Recovery Trends
Most athletes demonstrated improving AMI scores over time.
Recovery trajectories varied considerably across individuals.
Predictive Modeling
Linear regression was used to quantify the relationship between psychological readiness and physical performance.
Model results provide insight into the proportion of AMI variability explained by TSK-11 scores.

(Update this section with your actual R², coefficient, and correlation values.)

Example Visualization
AMI vs TSK-11

Scatter plot with fitted regression line showing the relationship between fear of movement and athletic performance.

Individual Athlete Recovery

Time-series visualization displaying AMI progression across rehabilitation visits.

Future Work

Potential extensions include:

Multiple regression models incorporating injury type
Mixed-effects models for repeated measurements
Classification of return-to-sport readiness
Time-to-recovery prediction
Machine learning approaches (Random Forest, XGBoost)
Results Summary
Metric	Value
Observations	XXX
ACL Athletes	XXX
Correlation	XXX
R²	XXX
Mean AMI Score	XXX
Mean TSK-11 Score	XXX
Author

Brett Sparks

Data Science Student
University of South Carolina

LinkedIn: Add Link
GitHub: Add Link

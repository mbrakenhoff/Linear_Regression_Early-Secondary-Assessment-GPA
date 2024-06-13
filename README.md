# High School GPA Prediction Project

## Context
This project aims to analyze and predict the GPA of high school students using their ACT Aspire scores and other relevant factors. By leveraging a multiple linear regression model, we seek to identify key predictors of GPA and validate the model's accuracy. The ultimate goal is to use the model to predict future students' GPAs and implement interventions for those predicted to perform below a set level.

## Project Files
- **Dataset File (Final.xlsx)**: This file contains the dataset with various attributes including student ID, GPA, ACT Aspire scores in English, Math, Reading, and Science, and a flag indicating whether the student has ever received special services (IEP, 504, ELL/ESL, BIP).
- **R Markdown File (GPA_Prediction.rmd)**: This R Markdown file contains the complete workflow for the project. It includes data loading, processing, exploratory data analysis, model building, and evaluation.
- **HTML File (GPA_Prediction.html)**: This HTML file is the knitted version of the R Markdown file. It includes a table of contents for easy exploration of the project.

## How Users Can Get Started with the Project
To get started with this project, follow these steps:

1. **Download the Dataset**: Ensure the provided dataset (Final.xlsx) is placed in your working directory.

2. **Open the R Markdown File**: Launch RStudio and open GPA_Prediction.rmd to explore and run the code.

3. **Edit the Data Input Method**: Update the data input method to read the dataset from your preferred location:
    ```r
    library(readxl)
    df <- read_excel("path_to_your_directory/Final.xlsx")
    ```

4. **Run the R Markdown File**: Follow and edit the cells in the R Markdown file to preprocess the data, build and evaluate the multiple linear regression model, and generate insights.

5. **Alternatively, Open GPA_Prediction.html** in your browser for an easy viewing of the completed project.

## Data Description
The dataset contains various attributes related to students' academic performance and services received. Key attributes include:

- **ID**: Student identification number
- **GPA**: Grade Point Average at the end of 10th grade
- **English**: ACT Aspire English score (scaled from 0 to 60)
- **Math**: ACT Aspire Math score (scaled from 0 to 60)
- **Reading**: ACT Aspire Reading score (scaled from 0 to 60)
- **Science**: ACT Aspire Science score (scaled from 0 to 60)
- **Flag**: Indicates whether the student has ever received special services (0 for no, 1 for yes)

## Statistical Model
The final multiple linear regression model is given by:
\[ \hat{Y} = \beta_0 + \beta_1 \text{English} + \beta_2 \text{Science} + \epsilon \]

Where:
- \( \hat{Y} \) is the predicted GPA
- \( \beta_0, \beta_1, \beta_2 \) are the estimated regression coefficients
- \( \epsilon \) is the error term

## Summary of Findings
The study found that English and Science scores have statistically significant effects on GPA. The model explains 14.83% of the variation in GPA, indicating some predictive power. However, the prediction interval is wide, suggesting the model may have limited practical use in predicting individual students' GPAs.

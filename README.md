# Mortgage Loan Project for CSCI 3358
Codebase for data analysis, deep dive on bias, and predictive modeling for loan allocation in New York City.

## Startup
Once the repo is downloaded, download data from https://www.consumerfinance.gov/data-research/hmda/historic-data/?geo=nationwide&records=all-records&field_descriptions=labels. Download "All records" with both "Plain language labels and HMDA codes" and "HMDA codes only" for NY state from 2010-2017. Once downloaded, place the labeled data into the directory 'data/raw_data/labeled_data' and the coded data into  the directory 'data/raw_data/coded_data'. 
Once data is all downloaded, run through 'process_raw_data.ipynb' this will handle all preprocessing of the data for both the labeled and  coded data. The use cases for these data are different with the coded data being used soley for model building and analysis and the labeled data for data analytics.

## Data Analytics
For data analytics, we used 'stat_breakdown.ipynb'. This file uses the processed labeled data and contains breakdowns of inherent bias found in the dataset and explores trends we found. We also used this file as the initial platform for the model building to hone down what indicators are classified as sensitive attributes and make decisions on what indicators ought to be included in a model that determines whether a person qualifies for a loan.

## Model Building / Analysis
For the model building, we used 'model_building.ipynb'. This file utilizes the processed coded data and contains model creation and evaluation for the predictive loan allocation models. This includes dedicated accuracy and fairness metric evaluation for the models. Certain aspects of the code are currently commented out (specifcally for equalizing the number of entries based on a specific sensitive attribute), to run related experiments, uncomment and choose desired cases, then rerun entire notebook.  
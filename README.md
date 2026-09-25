# Contact Operations Data Rescue

A Python and Pandas based data-cleaning and operations analytics project designed to process unreliable contact-centre records and generate reliable operational metrics and queue-level insights.

## Project Overview

Contact-centre data can contain duplicate records, inconsistent labels, invalid values, and missing information. This project demonstrates how raw contact records can be cleaned, validated, analysed, and transformed into useful operational information.

The solution was developed as part of a practical data engineering and AWS-focused applicant challenge.

## Objectives

- Clean and standardise contact-centre data
- Handle missing and invalid values
- Remove duplicate contact records
- Convert timestamps and numeric fields into usable formats
- Calculate contact-centre performance metrics
- Assign priorities to customer contacts
- Generate queue-level operational summaries
- Validate results using assertions
- Create meaningful data visualisations
- Export cleaned and analysed data

## Technologies Used

- Python 3
- Pandas
- Matplotlib
- Jupyter Notebook
- Google Colab

## Data Processing Workflow

Raw Contact Data  
↓  
Data Cleaning & Validation  
↓  
Duplicate Removal  
↓  
Standardisation  
↓  
Operational Metrics  
↓  
Priority Assignment  
↓  
Queue-Level Analysis  
↓  
Visualisation & Export

## Key Functions

### `clean_contacts(df)`

Cleans and standardises the input contact data.

Main operations include:

- Cleaning contact IDs
- Parsing timestamps
- Removing invalid records
- Removing duplicate contact IDs
- Standardising channel and outcome values
- Validating wait and handle times
- Validating customer ratings
- Handling missing agent IDs and customer messages

### `calculate_metrics(clean_df)`

Calculates key operational metrics including:

- Total contacts
- Voice, chat, and email contacts
- Unknown-channel contacts
- Average wait time
- 90th percentile wait time
- Abandonment rate
- Resolution rate

### `assign_priority(contact)`

Assigns a priority level based on operational conditions and customer-message content.

Priority levels:

- High
- Medium
- Low

### `build_queue_summary(clean_df)`

Creates a queue-level summary containing:

- Number of contacts
- Average wait time
- Abandonment rate

The summary is sorted by contact volume and queue name.

## Validation

The notebook includes additional assertions to verify important parts of the solution, including:

- Required columns are present
- Contact IDs are valid after cleaning
- Channel values are standardised
- Priority values are valid
- Queue summary values are consistent
- Calculated metrics match the cleaned dataset

## Outputs

The project generates:

- `cleaned_contacts.csv`
- `queue_summary.csv`
- `submission_summary.json`
- Operational visualisation

> The original personalised challenge dataset is not included in this repository.

## Skills Demonstrated

- Data Cleaning
- Data Validation
- Python
- Pandas
- Exploratory Data Analysis
- Data Transformation
- Operational Metrics
- Data Quality Checks
- Data Visualisation
- Missing-Value Handling
- Reproducible Jupyter Notebook Workflows

## Learning Outcome

This project helped strengthen my understanding of how raw operational data can be transformed into reliable information for decision-making. It also provided practical experience in writing reusable Python functions, handling edge cases, validating results, and documenting a reproducible data workflow.

## Note

This repository is intended to demonstrate the technical approach and learning outcomes of the project. The original personalised challenge dataset and candidate-specific information are excluded for privacy and assignment-integrity reasons.



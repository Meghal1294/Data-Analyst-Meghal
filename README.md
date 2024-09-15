# Data-Analyst-Meghal
- Project Title: Descriptive Analysis of Council Voting Patterns (2023-2024)

Objective: The primary goal of this project is to conduct a descriptive analysis of council voting records from 2023 and 2024. Through this analysis, we aim to summarize key characteristics of voting patterns, identify trends, and generate insights that can inform future council decisions and engagement strategies.

Dataset: The dataset includes council voting records from 2023 and 2024 and contains the following key features:

Vote Number: Unique identifier for each voting session.
Vote Date: The date of the voting event.
Agenda Description: Brief description of the agenda item being voted on.
Council Member: The name of the council member who participated in the vote.
Vote: Whether the council member voted "In Favour" or "In Opposition."
Decision: Outcome of the vote (e.g., "Carried Unanimous" or "Lost").
Vote Detail ID: Unique identifier for the vote's detailed record.

Methodology:
Data Collection and Preparation:
Load the dataset using data analysis tools like Excel

Descriptive Statistics:
Calculate summary statistics for key variables, including:
Total number of In favor votes .
Breakdown of decisions (Carried Unanimously, Carried and lost).

Data Visualization:
Create visual representations to illustrate findings:
Bar charts displaying the agenda items with the most in-favor votes.

Insights and Findings:
Summarize the insights derived from the analysis, highlighting:
Trends in favor and opposition voting over time (e.g., increase or decrease in unanimous decisions).

![Screenshot 2024-09-15 111349](https://github.com/user-attachments/assets/561efa2f-2965-4984-ad1d-030b26dc2447)
![Screenshot 2024-09-15 111231](https://github.com/user-attachments/assets/0dad5db4-a7f9-4e1f-9a22-2eceaf98a88d)
![Screenshot 2024-09-15 111855](https://github.com/user-attachments/assets/896fa2d3-764d-43be-bfda-f121c82efb6f)
![Screenshot 2024-09-15 112042](https://github.com/user-attachments/assets/ec06e7bc-2552-49a1-b3e6-b395c4e3de74)
![Screenshot 2024-09-15 134659](https://github.com/user-attachments/assets/e6b79458-0c29-49f4-8b51-b5c137b71787)
![Screenshot 2024-09-15 134757](https://github.com/user-attachments/assets/f7ee3207-eb5e-4fe1-a73b-b4c447e0386e)

- Project Title: Data Wrangling and ETL Pipeline Implementation for Council Voting Records (2023-2024) using AWS DataBrew and AWS Glue

Objective: The primary goal of this project is to perform comprehensive data wrangling and implement an ETL (Extract, Transform, Load) pipeline to prepare a clean and consistent dataset of council voting records from 2023 and 2024. This process aims to enhance the accuracy and usability of the dataset for analysis, reporting, and decision-making regarding council voting trends and behaviors.

Background: The council voting records from 2023 and 2024 contain valuable insights into council decisions and voting behaviors. However, inconsistencies in data formatting, missing values, and duplicate entries can hinder accurate analysis. By leveraging AWS Glue and AWS DataBrew, the project aims to clean, transform, and organize this dataset for efficient use in council reporting and future analysis.

Dataset: The dataset includes council voting records, with features such as:
Meeting Type: The type of council meeting (e.g., Council, Public Hearing).
Vote Date: The date of the vote.
Vote Number: A unique identifier for each vote.
Agenda Description: The subject matter of the vote (e.g., rezoning decisions).
Vote Start Date Time: The timestamp when the vote started.
Council Member: The council member casting the vote.
Vote Classification: Whether the vote was "In Favour" or "In Opposition."
Decision: The outcome of the vote (e.g., "Carried Unanimous," "Lost").
Vote Detail ID: Unique identifier for detailed vote information.

Methodology:
Data Collection:
Collect datasets from council records for 2023 and 2024, stored in the RAW folder of AWS S3.

Data Wrangling with AWS DataBrew:
Initial Assessment:
Load the data in AWS DataBrew to perform an initial assessment, identifying issues such as missing values, duplicate records, and inconsistent data types.
Generate summary statistics for key variables, including voting patterns and participation by council members.

Data Cleaning:
Use DataBrew’s cleaning tools to:
Address missing values using methods like imputation or exclusion.
Remove duplicate vote records.
Standardize categorical variables (e.g., council member names and meeting types).
Format date-time fields appropriately (e.g., converting "Vote Start Date Time" to a proper date-time object).
Rename columns for improved readability (e.g., "Vote" to "Vote Classification").

Transformation:
Use DataBrew transformations to:
Derive new columns such as year extracted from vote date for temporal analysis.
Perform basic data aggregation to summarize monthly or yearly trends in voting behavior.

Profiling and Validation:
Conduct data profiling in AWS DataBrew to ensure data quality and consistency, confirming that no errors or outliers persist.

 ETL Pipeline Implementation with AWS Glue:

Extract:
Use AWS Glue to extract the source data from the RAW folder in AWS S3. Load both the 2023 and 2024 datasets separately.
Transform:
Apply the following transformations within the AWS Glue pipeline:
Change Schema: Adjust the schema for consistency across both 2023 and 2024 data, ensuring columns are standardized.
Filter: Exclude unnecessary records based on specific criteria (e.g., filtering out non-relevant meeting types or votes).
Aggregate: Summarize data such as total votes per council member or by agenda item across the two years.
Union: Combine the 2023 and 2024 datasets into a unified dataset for seamless reporting and analysis.
Derived Columns: Create additional features (e.g., vote duration, year of voting) to enrich the dataset for further analysis.
Joins: If applicable, join this data with other relevant sources, such as additional council information or historical voting records.
Load:
Once the ETL pipeline has been successfully run, store the cleaned and transformed data in the Curated folder in AWS S3 for future use in reporting and analysis.

Data Consolidation:
Consolidate the cleaned and transformed dataset, ensuring that all vote records across 2023 and 2024 are consistently formatted and linked through unique identifiers like the Vote Detail ID.

Documentation and Validation:
Document the entire data wrangling and ETL process, detailing the transformations and cleaning methods applied in both AWS DataBrew and AWS Glue.

Tools and Technologies:
AWS Glue for implementing the ETL pipeline, including schema changes, filtering, aggregation, and joining of data.
AWS DataBrew for data cleaning, transformation, profiling, and additional data wrangling steps.
AWS S3 for data storage, both in the RAW and Curated folders.
Excel for additional data manipulation, if necessary.


Deliverables:
A cleaned and transformed council voting dataset, stored in AWS S3 Curated folder, ready for analysis and reporting.
A detailed report documenting the steps involved in the data wrangling and ETL pipeline implementation using AWS DataBrew and AWS Glue, including challenges encountered and methods used.
Visualizations illustrating the results of the EDA, confirming data quality and the success of the transformations.

Timeline:
Week 1: Data wrangling and cleaning using AWS DataBrew, data assessment, and transformations.
Week 2: ETL pipeline setup and execution using AWS Glue.
Week 2: Final data validation, documentation, and reporting.


![Screenshot 2024-09-15 140834](https://github.com/user-attachments/assets/46ad5e60-e29b-486a-86af-891a67c250d7)
![Screenshot 2024-09-15 140915](https://github.com/user-attachments/assets/eeaedddd-008e-4a11-b5f0-ba5eda357f24)
![Screenshot 2024-09-15 144259](https://github.com/user-attachments/assets/14ab28d2-d3b0-42c9-b3f2-afc90c39b4a4)
![Screenshot 2024-09-15 153158](https://github.com/user-attachments/assets/48b93bfd-f86f-44cd-ac9e-36a0f06faf18)







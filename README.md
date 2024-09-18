# Data-Analyst-Meghal


**Project 1:Council Voting Patterns (2023-2024)**
-  **Project Title 1A: Descriptive Analysis of Council Voting Patterns (2023-2024)**

**Objective**: The primary goal of this project is to conduct a descriptive analysis of council voting records from 2023 and 2024. Through this analysis, we aim to summarize key characteristics of voting patterns, identify trends, and generate insights that can inform future council decisions and engagement strategies.

**Dataset**: The dataset includes council voting records from 2023 and 2024 and contains the following key features:
Vote Number: Unique identifier for each voting session.
Vote Date: The date of the voting event.
Agenda Description: Brief description of the agenda item being voted on.
Council Member: The name of the council member who participated in the vote.
Vote: Whether the council member voted "In Favour" or "In Opposition."
Decision: Outcome of the vote (e.g., "Carried Unanimous" or "Lost").
Vote Detail ID: Unique identifier for the vote's detailed record.

**Methodology**:
Data Collection and Preparation:
Load the dataset using data analysis tools like Excel

**Descriptive Statistics**:
Calculate summary statistics for key variables, including:
Total number of In favor votes .
Breakdown of decisions (Carried Unanimously, Carried and lost).

**Data Visualization**:
Create visual representations to illustrate findings:
Bar charts displaying the agenda items with the most in-favor votes.

**Insights and Findings**:
Summarize the insights derived from the analysis, highlighting:
Trends in favor and opposition voting over time (e.g., increase or decrease in unanimous decisions).

**Tools and Technologies**:
AWS Services: Amazon S3 for data storage
Microsoft excel for Data Visualization, Loading data

**Deliverables**:
Data Loading and Preparation:
Steps to load data from Amazon S3.
Descriptive Statistics:
Summary statistics for key variables (e.g., total number of disciplinary actions, breakdown by type and outcome).
Data Visualization:
Visualizations created 




![Screenshot 2024-09-15 111349](https://github.com/user-attachments/assets/561efa2f-2965-4984-ad1d-030b26dc2447)
![Screenshot 2024-09-15 111231](https://github.com/user-attachments/assets/0dad5db4-a7f9-4e1f-9a22-2eceaf98a88d)
![Screenshot 2024-09-15 111855](https://github.com/user-attachments/assets/896fa2d3-764d-43be-bfda-f121c82efb6f)
![Screenshot 2024-09-15 112042](https://github.com/user-attachments/assets/ec06e7bc-2552-49a1-b3e6-b395c4e3de74)
![Screenshot 2024-09-15 134659](https://github.com/user-attachments/assets/e6b79458-0c29-49f4-8b51-b5c137b71787)
![Screenshot 2024-09-15 134757](https://github.com/user-attachments/assets/f7ee3207-eb5e-4fe1-a73b-b4c447e0386e)



- **Project(1B) Title: Data Wrangling and ETL Pipeline Implementation for Council Voting Records (2023-2024) using AWS DataBrew and AWS Glue**

**Objective**: The primary goal of this project is to perform comprehensive data wrangling and implement an ETL (Extract, Transform, Load) pipeline to prepare a clean and consistent dataset of council voting records from 2023 and 2024. This process aims to enhance the accuracy and usability of the dataset for analysis, reporting, and decision-making regarding council voting trends and behaviors.

**Background**: The council voting records from 2023 and 2024 contain valuable insights into council decisions and voting behaviors. However, inconsistencies in data formatting, missing values, and duplicate entries can hinder accurate analysis. By leveraging AWS Glue and AWS DataBrew, the project aims to clean, transform, and organize this dataset for efficient use in council reporting and future analysis.

**Dataset**: The dataset includes council voting records, with features such as:
Meeting Type: The type of council meeting (e.g., Council, Public Hearing).
Vote Date: The date of the vote.
Vote Number: A unique identifier for each vote.
Agenda Description: The subject matter of the vote (e.g., rezoning decisions).
Vote Start Date Time: The timestamp when the vote started.
Council Member: The council member casting the vote.
Vote Classification: Whether the vote was "In Favour" or "In Opposition."
Decision: The outcome of the vote (e.g., "Carried Unanimous," "Lost").
Vote Detail ID: Unique identifier for detailed vote information.

**Methodology**:
Data Collection:
Collect datasets from council records for 2023 and 2024, stored in the RAW folder of AWS S3.

**Data Wrangling with AWS DataBrew**:
Initial Assessment:
Load the data in AWS DataBrew to perform an initial assessment, identifying issues such as missing values, duplicate records, and inconsistent data types.
Generate summary statistics for key variables, including voting patterns and participation by council members.

**Data Cleaning**:
Use DataBrew’s cleaning tools to:
Address missing values using methods like imputation or exclusion.
Remove duplicate vote records.
Standardize categorical variables (e.g., council member names and meeting types).
Format date-time fields appropriately (e.g., converting "Vote Start Date Time" to a proper date-time object).
Rename columns for improved readability (e.g., "Vote" to "Vote Classification").

**Transformation**:
Use DataBrew transformations to:
Derive new columns such as year extracted from vote date for temporal analysis.
Perform basic data aggregation to summarize monthly or yearly trends in voting behavior.

**Profiling and Validation**:
Conduct data profiling in AWS DataBrew to ensure data quality and consistency, confirming that no errors or outliers persist.

**ETL Pipeline Implementation with AWS Glue**:
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

**Data Consolidation**:
Consolidate the cleaned and transformed dataset, ensuring that all vote records across 2023 and 2024 are consistently formatted and linked through unique identifiers like the Vote Detail ID.

**Documentation and Validation**:
Document the entire data wrangling and ETL process, detailing the transformations and cleaning methods applied in both AWS DataBrew and AWS Glue.

**Tools and Technologies**:
AWS Glue for implementing the ETL pipeline, including schema changes, filtering, aggregation, and joining of data.
AWS DataBrew for data cleaning, transformation, profiling, and additional data wrangling steps.
AWS S3 for data storage, both in the RAW and Curated folders.
Excel for additional data manipulation, if necessary.

**Deliverables**:
A cleaned and transformed council voting dataset, stored in AWS S3 Curated folder, ready for analysis and reporting.
A detailed report documenting the steps involved in the data wrangling and ETL pipeline implementation using AWS DataBrew and AWS Glue, including challenges encountered and methods used.

**Timeline**:
Week 1: Data wrangling and cleaning using AWS DataBrew, data assessment, and transformations.
Week 2: ETL pipeline setup and execution using AWS Glue.
Week 2: Final data validation, documentation, and reporting.


![Screenshot 2024-09-15 140834](https://github.com/user-attachments/assets/46ad5e60-e29b-486a-86af-891a67c250d7)
![Screenshot 2024-09-15 140915](https://github.com/user-attachments/assets/eeaedddd-008e-4a11-b5f0-ba5eda357f24)
![Screenshot 2024-09-15 144259](https://github.com/user-attachments/assets/14ab28d2-d3b0-42c9-b3f2-afc90c39b4a4)
![Screenshot 2024-09-15 153158](https://github.com/user-attachments/assets/48b93bfd-f86f-44cd-ac9e-36a0f06faf18)


-
-  **Project(1C) Title: Implementation of Data Quality Control Measures for Council Voting Records (2023-2024)**

**Objective**: The primary objective of this project is to establish a comprehensive Data Quality Control (DQC) framework for the Council Voting Records (2023-2024) dataset. This framework will ensure the accuracy, completeness, consistency, and reliability of the council’s voting records, which are essential for analysis, reporting, and decision-making processes related to council operations.

**Background**:
As the council maintains voting records spanning from 2023 to 2024, challenges have surfaced related to inaccuracies, missing fields, duplicates, and inconsistent data formats across the dataset. These issues, if left unaddressed, can negatively affect analysis, transparency, and operational efficiency. This project aims to implement robust data quality control measures to enhance the reliability and usability of these records, ensuring compliance with internal governance standards.

**Scope**:
The project will focus on the following key areas:
Data Profiling: Analyzing the council voting dataset to assess its quality.
Data Cleansing: Developing processes to correct inaccuracies, eliminate duplicates, and standardize formats.
Data Validation: Implementing validation rules and checks to ensure data integrity across voting records.
Monitoring and Reporting: Establishing dashboards and ongoing monitoring processes to track data quality metrics.

**Methodology**:
Current State Assessment:
Conduct a thorough analysis of the Council Voting Records (2023-2024) to identify issues like missing fields, duplicates, and inconsistent data types (e.g., varying date formats, missing agenda descriptions).
Focus on key fields like Vote Date, Vote Number, Council Member, Agenda Description, Vote Classification, and Decision to assess their impact on council operations and reporting.

**Data Profiling**:
Utilize AWS DataBrew and other profiling tools to assess the dataset’s completeness, uniqueness, validity, consistency, and accuracy.
Document key findings such as missing vote details, incorrect classifications, or inconsistent council member names, highlighting areas that need immediate attention.

**Establish Data Quality Metrics**:
Define clear data quality metrics and Key Performance Indicators (KPIs) to evaluate and track data quality over time. These metrics may include:
Completeness (e.g., percentage of missing fields like Vote Date or Agenda Description).

**Monitoring and Reporting**:
AWS CloudWatch and CloudTrail are integrated for real-time monitoring of data quality, resource utilization, and user activities.
Create dashboards that track metrics such as track the expected charges incurred by utilizing S3 and another to tally the number of objects in the bucket
To keep costs under control, we put up a CloudWatch alarm that sends an email notice whenever the expected charges reach $35
Schedule monthly reports to review data quality trends and performance against established KPIs.

**Feedback Mechanism**:
Establish a feedback loop to continually assess and improve data quality processes based on user input and observed results.
Implement user-friendly feedback forms or automatic alerts if data quality issues are detected by council staff during the voting process.

**Tools and Technologies**:
AWS Glue: For ETL (Extract, Transform, Load) pipeline implementation and data validation.
AWS CloudWatch and CloudTrail: For monitoring data quality metrics, resource usage, and user activity in real-time.
Data visualization tools  for monitoring dashboards and real-time data quality tracking.

**Deliverables**:
A comprehensive Data Quality Control plan, detailing procedures, metrics, and responsibilities for council voting data quality management.
Cleaned and validated council voting records dataset, ready for analysis and reporting, stored in AWS S3 Curated folder.
Documentation of data quality metrics and KPIs that will be tracked over time, including error rates, completeness, and consistency.
Training resources, including materials and workshops, designed to educate council staff on data quality practices.
Monitoring dashboards that visualize real-time data quality metrics and provide alerts when deviations occur.

**Timeline**:
Week 1: Conduct data profiling using AWS DataBrew, assess current state, and define data quality metrics.
Week 2: Implement data cleansing and validation rules in AWS Glue and set up monitoring in CloudWatch and CloudTrail.
Week 2: Set up data quality dashboards and alarms for real-time monitoring and reporting.

![Screenshot 2024-09-15 160430](https://github.com/user-attachments/assets/30689a2f-45b2-49b1-9ad5-500b90a50baf)
![Screenshot 2024-09-15 160549](https://github.com/user-attachments/assets/e1828b48-99f7-44f6-97a5-0ea75c921b97)
![Screenshot 2024-09-15 160642](https://github.com/user-attachments/assets/7530577d-fafa-41b9-8fed-8975974ea1b9)
![Screenshot 2024-09-15 160721](https://github.com/user-attachments/assets/23ad482a-33fc-43d7-adad-dc48306d6ac9)
![Screenshot 2024-09-15 160754](https://github.com/user-attachments/assets/63bcb8fd-7c31-4156-83b2-cdf471cd8b4e)
![Screenshot 2024-09-15 162057](https://github.com/user-attachments/assets/1cd4c343-2b0e-4245-a4a7-761a6baf5358)


 
  
  - **Project 2:  Student Disciplinary Records (2022-2024)**
  
-  **_Project 2A: Descriptive Analysis of Student Disciplinary Records (2022-2024)_**

**Objective**: The primary goal of this project is to conduct a descriptive analysis of student disciplinary records from 2022 to 2024. Through this analysis, we aim to summarize key characteristics of disciplinary actions, identify trends, and generate insights that can inform future disciplinary policies and student engagement strategies.

**Dataset**: The dataset includes student disciplinary records from 2022 to 2024 and contains the following key features:
Student ID: Unique identifier for each student.
First Name: The first name of the student.
Last Name: The last name of the student.
Date of Record: The date when the disciplinary action was recorded.
Grade Level: The grade level of the student.
Type of Action: The type of disciplinary action taken (e.g., Minor, Major).
Description/Type of Misconduct: Brief description of the misconduct.
Outcome/Action Taken: The outcome of the disciplinary action (e.g., Suspension, Detention).

**Methodology**:
Data Collection and Preparation: Load the dataset using data analysis tools like Excel.
Descriptive Statistics: Calculate summary statistics for key variables, including:
Total number of disciplinary actions.
Breakdown of actions by type (Minor, Major).
Breakdown of outcomes (Suspension, Detention, etc.).

**Data Visualization**: Create visual representations to illustrate findings:
Bar charts displaying the Percentage of Major Action (PMAT) taken

**Insights and Findings**: Summarize the insights derived from the analysis, highlighting:
Trends in disciplinary actions over time (e.g., increase or decrease in certain types of misconduct).
Patterns in outcomes based on grade level or type of misconduct

**Tools and Technologies**:
AWS Services: Amazon S3 for data storage
Microsoft excel for Data Visualization, Loading data

**Deliverables**:
Data Loading and Preparation:
Steps to load data from Amazon S3.
Descriptive Statistics:
Summary statistics for key variables (e.g., total number of disciplinary actions, breakdown by type and outcome).
Data Visualization:
Visualizations created 
![Screenshot 2024-09-17 221309](https://github.com/user-attachments/assets/c85cb808-4bce-4b95-986e-c87841335d45)
![Screenshot 2024-09-17 221452](https://github.com/user-attachments/assets/e158ebeb-02d1-4420-bf0c-bf0d3ca9b64c)
![Screenshot 2024-09-17 221531](https://github.com/user-attachments/assets/d684dbe1-9642-4a98-80f3-6a78ee22184e)
![Screenshot 2024-09-17 222654](https://github.com/user-attachments/assets/dc02c189-8b59-479c-a5fc-4f5ecbfc41de)


**_Project(1B) Title: Data Wrangling and ETL Pipeline Implementation for Student Disciplinary Records (2022-2024) using AWS DataBrew and AWS Glue_**

**Objective**: The primary goal of this project is to perform comprehensive data wrangling and implement an ETL (Extract, Transform, Load) pipeline to prepare a clean and consistent dataset of student past records from 2022 to 2024. This process aims to enhance the accuracy and usability of the dataset for analysis, reporting, and decision-making regarding student performance and trends.

**Background**: The student past records from 2022 to 2024 contain valuable insights into student performance and trends. However, inconsistencies in data formatting, missing values, and duplicate entries can hinder accurate analysis. By leveraging AWS Glue and AWS DataBrew, the project aims to clean, transform, and organize this dataset for efficient use in educational reporting and future analysis.

**Dataset**: The dataset includes student records, with features such as:
Student ID: A unique identifier for each student.
Enrollment Date: The date the student enrolled.
Course: The course the student is enrolled in.
Grades: The grades achieved by the student.
Attendance: Attendance records of the student.
Graduation Date: The date the student graduated (if applicable).

**Methodology**:
Data Collection: Collect datasets from student records for 2022 to 2024, stored in the RAW folder of AWS S3.
Data Wrangling with AWS DataBrew:

**Initial Assessment**:
Load the data in AWS DataBrew to perform an initial assessment, identifying issues such as missing values, duplicate records, and inconsistent data types.
Generate summary statistics for key variables, including student performance and attendance patterns.

**Data Cleaning**:
Use DataBrew’s cleaning tools to:
Address missing values using methods like imputation or exclusion.
Remove duplicate student records.
Standardize categorical variables (e.g., course names).
Format date fields appropriately (e.g., converting “Enrollment Date” to a proper date-time object).
Rename columns for improved readability (e.g., “Grades” to “Student Grades”).

**Transformation**:
Use DataBrew transformations to:
Derive new columns such as year extracted from enrollment date for temporal analysis.
Perform basic data aggregation to summarize yearly trends in student performance.

**Profiling and Validation**:
Conduct data profiling in AWS DataBrew to ensure data quality and consistency, confirming that no errors or outliers persist.
ETL Pipeline Implementation with AWS Glue:
Extract:Use AWS Glue to extract the source data from the RAW folder in AWS S3. Load the datasets for 2022, 2023, and 2024 separately.
Transform: Apply the following transformations within the AWS Glue pipeline:
Change Schema: Adjust the schema for consistency across all years, ensuring columns are standardized.
Filter: Exclude unnecessary records based on specific criteria (e.g., filtering out non-relevant courses).
Aggregate: Summarize data such as total grades per student or by course across the three years.
Union: Combine the datasets from 2022, 2023, and 2024 into a unified dataset for seamless reporting and analysis.
Derived Columns: Create additional features (e.g., year of enrollment) to enrich the dataset for further analysis.
Joins: If applicable, join this data with other relevant sources, such as additional student information or historical records.
Load: Consolidate the cleaned and transformed dataset, ensuring that all student records across 2022 to 2024 are consistently formatted and linked through unique identifiers like the Student ID.

**Documentation and Validation**:
Document the entire data wrangling and ETL process, detailing the transformations and cleaning methods applied in both AWS DataBrew and AWS Glue.

**Tools and Technologies**:
AWS Glue for implementing the ETL pipeline, including schema changes, filtering, aggregation, and joining of data.
AWS DataBrew for data cleaning, transformation, profiling, and additional data wrangling steps.
AWS S3 for data storage, both in the RAW and Curated folders.
Excel for additional data manipulation, if necessary.

**Deliverables**:
A cleaned and transformed student dataset, stored in AWS S3 Curated folder, ready for analysis and reporting.
A detailed report documenting the steps involved in the data wrangling and ETL pipeline implementation using AWS DataBrew and AWS Glue, including challenges encountered and methods used.

**Timeline**:
Week 1: Data wrangling and cleaning using AWS DataBrew, data assessment, and transformations.
Week 2: ETL pipeline setup and execution using AWS Glue.
Week 2: Final data validation, documentation, and reporting.


![Screenshot 2024-09-17 231413](https://github.com/user-attachments/assets/552600ae-a498-4701-8504-76d2d691d360)
![Screenshot 2024-09-17 224146](https://github.com/user-attachments/assets/b8493ce1-7ed9-452b-bce1-239802a6284b)
![Screenshot 2024-09-17 231142](https://github.com/user-attachments/assets/772e7aa6-5827-4b69-a3c5-c79a8e014bad)









**Project(1C) Title: Implementation of Data Quality Control Measures for Student Disciplinary Records (2022-2024)**

**Objective**: The primary objective of this project is to establish a comprehensive Data Quality Control (DQC) framework for the Student Disciplinary Records (2022-2024) dataset. This framework will ensure the accuracy, completeness, consistency, and reliability of the student records, which are essential for analysis, reporting, and decision-making processes related to educational operations.

**Background**: As the institution maintains student records spanning from 2022 to 2024, challenges have surfaced related to inaccuracies, missing fields, duplicates, and inconsistent data formats across the dataset. These issues, if left unaddressed, can negatively affect analysis, transparency, and operational efficiency. This project aims to implement robust data quality control measures to enhance the reliability and usability of these records, ensuring compliance with internal governance standards.

**Scope**: The project will focus on the following key areas:
Data Profiling: Analyzing the student dataset to assess its quality.
Data Cleansing: Developing processes to correct inaccuracies, eliminate duplicates, and standardize formats.
Data Validation: Implementing validation rules and checks to ensure data integrity across student records.
Monitoring and Reporting: Establishing dashboards and ongoing monitoring processes to track data quality metrics.

**Methodology**:
Current State Assessment:
Conduct a thorough analysis of the Student Past Records (2022-2024) to identify issues like missing fields, duplicates, and inconsistent data types (e.g., varying date formats, missing course descriptions).
Focus on key fields like Enrollment Date, Student ID, Student Name, Course Description, Grade, and Attendance to assess their impact on educational operations and reporting.

**Data Profiling**:
Utilize AWS DataBrew and other profiling tools to assess the dataset’s completeness, uniqueness, validity, consistency, and accuracy.
Document key findings such as missing student details, incorrect classifications, or inconsistent student names, highlighting areas that need immediate attention.
Establish Data Quality Metrics:Define clear data quality metrics and Key Performance Indicators (KPIs) to evaluate and track data quality over time. These metrics may include:
Completeness (e.g., percentage of missing fields like Enrollment Date or Course Description).

**Monitoring and Reporting**:
AWS CloudWatch and CloudTrail are integrated for real-time monitoring of data quality, resource utilization, and user activities.
Create dashboards that track metrics such as the number of records processed and data quality trends.
To keep costs under control, set up a CloudWatch alarm that sends an email notice whenever the expected charges reach $35.
Schedule monthly reports to review data quality trends and performance against established KPIs.

**Feedback Mechanism**:
Establish a feedback loop to continually assess and improve data quality processes based on user input and observed results.
Implement user-friendly feedback forms or automatic alerts if data quality issues are detected by staff during data entry or analysis.

**Tools and Technologies**:
AWS Glue: For ETL (Extract, Transform, Load) pipeline implementation and data validation.
AWS CloudWatch and CloudTrail: For monitoring data quality metrics, resource usage, and user activity in real-time.
Data visualization tools: For monitoring dashboards and real-time data quality tracking.

**Deliverables**:
A comprehensive Data Quality Control plan, detailing procedures, metrics, and responsibilities for student data quality management.
Cleaned and validated student records dataset, ready for analysis and reporting, stored in AWS S3 Curated folder.
Documentation of data quality metrics and KPIs that will be tracked over time, including error rates, completeness, and consistency.
Training resources, including materials and workshops, designed to educate staff on data quality practices.
Monitoring dashboards that visualize real-time data quality metrics and provide alerts when deviations occur.

**Timeline**:
Week 1: Conduct data profiling using AWS DataBrew, assess current state, and define data quality metrics.
Week 2: Implement data cleansing and validation rules in AWS Glue and set up monitoring in CloudWatch and CloudTrail.
Week 3: Set up data quality dashboards and alarms for real-time monitoring and reporting

![Screenshot 2024-09-17 231903](https://github.com/user-attachments/assets/c042e1e8-6b19-437c-9a8b-02c2f7120afb)

























# Nashville Housing Data Cleaning

![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Microsoft SQL Server](https://img.shields.io/badge/Microsoft_SQL_Server-8080cc?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![Microsoft Office](https://img.shields.io/badge/Microsoft_Office-D83B01?style=for-the-badge&logo=microsoft-office&logoColor=white)
![Microsoft Word](https://img.shields.io/badge/Microsoft_Word-2B579A?style=for-the-badge&logo=microsoft-word&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)


## Problem Description
In the field of data analytics, raw datasets are often messy and unformatted, requiring significant transformation before they can be used for exploratory analysis. This project focuses on the Nashville Housing dataset, which contains over 56,000 rows of housing records. The objective is to utilize SQL to clean and standardize this data, addressing inconsistencies in date formats, missing address information, and redundant records.


## Background Information
Data cleaning is a critical phase of the data analysis process, often accounting for the majority of a researcher's time. For the Nashville Housing dataset, specific challenges included concatenated address strings, inconsistent boolean-style fields, and duplicate entries that could skew statistical results. By applying systematic SQL queries, the dataset is transformed into a structured format that enhances data usability and accuracy.


## Dataset Information
The dataset comprises several columns detailing property transactions in Nashville, including:
1. **UniqueID:** A distinctive identifier for each entry
2. **ParcelID:** A unique identifier for the specific parcel of land
3. **PropertyAddress:** The physical address of the property
4. **SaleDate:** The date the property was sold
5. **SalePrice:** The price at which the home was sold
6. **LegalReference:** Legal documentation identifiers for the property
7. **SoldAsVacant:** Indicates if the property was vacant at the time of sale
8. **OwnerAddress:** The address of the property owner


## Problem Statement
The central challenge of this project is to implement robust SQL queries to standardize data across a large table. The pivotal tasks include:
- **Data Standardizing:** Converting the SaleDate from a timestamped datetime format to a simplified date format.
- **Missing Value Population:** Filling null values in the *PropertyAddress* field by using a self-join to match addresses with identical *ParcelID* entries.
- **String Parsing:** Separating concatenated address fields into individual columns for Street Address, City, and State using SUBSTRING and PARSENAME functions.
- **Data Uniformity:** Standardizing the *SoldAsVacant* field by converting inconsistent "Y" and "N" entries into "Yes" and "No" via CASE statements.
- **Duplicate Removal:** Identifying and deleting **104** duplicate rows using a Common Table Expression (CTE) and the ROW_NUMBER windows function.
- **Schema Cleanup:** Removing obsolete or redundant columns, such as original addresses and tax districts, to streamline the final table.


## Outcome
Successful execution of these SQL scripts results in a cleaned and standardized database that is significantly more usable for business intelligence and reporting. By breaking down addresses and standardizing fields, the data becomes more granular and friendly for analysis, ensuring that subsequent data-driven decisions are based on accurate and high-quality information.


## Tools Used for this Project
- **Microsoft SQL Server:** Used as the primary database engine for importing, storing, and manipulating the 56,000+ rows of housing data.
- **T-SQL (Transact-SQL):** The core language used to write all cleaning queries.
- **JOINS (Self-Join):** Utilized to link the table to itself to populate missing PropertyAddress data based on matching ParcelID values.
- **String Functions (SUBSTRING, CHARINDEX, LEN):** Employed to parse the PropertyAddress into separate columns for Address and City.
- **PARSENAME & REPLACE:** Used as an efficient alternative to substrings for splitting the OwnerAddress into Address, City, and State by converting delimiters into periods.
- **CASE Statements:** Applied to standardize the SoldAsVacant field, transforming inconsistent "Y/N" values into a uniform "Yes/No" format.
- **CTEs & Windows Functions (ROW_NUMBER):** A Common Table Expression was combined with ROW_NUMBER and PARTITION BY to identify and delete 104 duplicate records.
- **DDL (Data Definition Language):** Used ALTER TABLE and DROP COLUMN to modify the table schema and remove redundant fields.

## Author
- <b>©2026 Gaurav Kamble
- <b>[LinkedIn](https://www.linkedin.com/in/gaurav-kamble/)</b>
- <b>[Tableau Public](https://public.tableau.com/app/profile/datagaurav/vizzes)</b>
- <b>[Kaggle](https://www.kaggle.com/justgk)</b>
- <b>[Email](mailto:gauravksse@gmail.com)</b>

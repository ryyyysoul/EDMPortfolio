# ***Midterm Lab Task 2 - Data Cleaning and Transformation using POWER QUERY***
This portfolio provides an in-depth overview of the process involved in data cleaning and preparation utilizing Power Query, a powerful tool for data manipulation. The dataset under consideration comprises several interconnected tables, each containing valuable information that requires meticulous attention. Throughout this portfolio, various cleaning techniques will be applied systematically to enhance the overall quality and consistency of the data. This preparatory work is crucial, as it lays the foundation for effective analysis and ensures that the insights derived from the data are reliable and meaningful. By addressing issues such as missing values, duplicate entries, and inconsistencies, we can significantly improve the dataset's integrity and usability, ultimately leading to more accurate and insightful analyses.
## **STEP 1 - Data Cleaning process**
- Download the dataset (Uncleaned_DS_jobs.csv)
- Open Excel
- Go to Data → New Query → Open File → Text/CSV
- Click Load and then Edit using Power Query Editor
## **STEP 2 - Duplicate Raw Data**
- Right-click the dataset in the Queries pane
- Select Duplicate
## **STEP 3 - Clean Salary Data**
- Select the Salary Estimate column
- Go to Transform Menu → Extract → Text Before Delimiter
- Type “(“ and click OK
- Create two new columns: Min Salary and Max Salary

Select Salary Estimate column → Add Column Menu → Column from Examples → From Selections

Type the first min salary value and press Enter (all rows will auto-fill)

Rename the column to “Min Sal”

Repeat the process for Max Salary
## **STEP 4 - Duplicate Raw Data**
## **STEP 5 - Duplicate Raw Data**
Here are the screenshots showcasing the table transformation process
## **STEP 6 - Here's the screenshot of my output before I started data cleaning (See screenshot)**
<img src="Images/raw2.png" alt="Alt Text" width="900" height="800">

## **STEP 7 - Here's the screenshot of my output after I started data cleaning (See screenshot)**
<img src="Images/task2.png" alt="Alt Text" width="900" height="600">

## **In Power Query**
<img src="Images/Uncleaned_DS_jobs.PNG" alt="Alt Text" width="900" height="600">

## ***Here's the Physical Data Model***
<img src="Images/QueryDependencies.PNG" alt="Alt Text" width="900" height="600">

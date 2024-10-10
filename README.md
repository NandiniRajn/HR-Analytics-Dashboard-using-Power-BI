# HR-Analytics-Dashboard-using-Power-BI

This HR analytics Power BI project provides insights into an organisation's attrition, which helps the HR team analyse and monitor employee data further and make data-driven decisions related to employee retention, development, and recruitment.

[Download the dataset from here.](https://github.com/NandiniRajn/HR-Analytics-Dashboard-using-Power-BI/blob/main/HR%20Dataset.xlsx)

## Step by step process:

**1. Data Gathering:** 
  - Import raw data .xlsx file into Power BI & transform data to Power Query editor for cleaning and data processing.

**2. Data cleaning:**
  - Check the empty column, duplicates, errors etc, and then remove it.
  - Replacing values in columns with values and naming.
  - check all column's data types, and change the data type by using the auto-detect data type function in the Power query editor.

**3. Data processing:**
  - In the Power Query editor, create a new column called "Attrition Count" by using this formula (=Table.AddColumn(#"Changed Type1", "Attrition Count", each if [Attrition] = "Yes" then 1 else 0) 
  - Change This new column data type by using this formula (= Table.TransformColumnTypes(#"Added Conditional Column",{{"Attrition Count", Int64.Type}}))
  - then creating the Attrition Rate, add a new measure (Attrition Rate = DIVIDE(SUM('HR data'[Attrition Count]), SUM('HR data'[Employee Count]),")).

**4. Data analysis:**
  - The process of analysis entails producing a variety of visual representations, including bar charts, (KPIs), table charts, Area charts, pie charts, slicers, and other pertinent visualizations. These tools are employed to acquire insights and present data comprehensively and easily understandable.
  - These tools are utilized to gain insights and present data comprehensively and easily understandable.

### Summary of dashboard:

1. **Average Age:** The Average Age is 36.92 and the minimum age is 18 in this organisation.
2. **Total Attrition:** A total of 237 employees left the organization, 150 male and 87 female and the attrition rate is 0.16.
3. **Total Employees: ** The organization has a total employing 1470 active employees 1233, making more improvements for growth employees.
4. **Education Field Impact: ** Education in life Sciences field Employees highest in total employees and 2nd field employees is Medical 3rd is Marketing, emphasizing the need to address retention challenges in this specific area.
5. 3. **Departmental Attrition:** The Research and Development Department has the highest attrition rate at 56.13%, suggesting potential areas for improvement in employee retention strategies in this department.
7. **Highest Income Job Role:**  The top highest income job roles are Manager income of 17k, Second Research and Director's salary of 16k and third Health care representative 7k salary. 


![HR Analytics dashboard]( https://github.com/NandiniRajn/HR-Analytics-Dashboard-using-Power-BI/blob/main/HR%20Dashboard1.pdf)


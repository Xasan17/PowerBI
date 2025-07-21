1. List three data sources Power BI can connect to.
Microsoft Excel

SQL Server

Web (HTML/XML/JSON via URL)

2. What is the first step to import data into Power BI Desktop?
Click "Get Data" and choose the appropriate data source (e.g., Excel, CSV, SQL Server).

3. How do you refresh imported data in Power BI?
Click the "Refresh" button on the Home tab to update all connected data sources.

4. What file formats can Power BI import directly? (Name two.)
.csv

.xlsx (Excel)

5. What does the "Navigator" window show after selecting a data source?
It displays a list of available tables, sheets, or objects from the selected source for preview and selection.

6. Import Sales_Data.csv and load only the "Product" and "Price" columns.
Open Power BI → Get Data → Text/CSV → select the file

Click Transform Data

Remove all columns except "Product" and "Price"

Click Close & Load

7. How would you change OrderDate to a date format during import?
In Power Query:

Click on the "OrderDate" column → go to the Transform tab → select Data Type → choose Date

8. What is the difference between "Load" and "Transform Data" in the import dialog?
Load: Directly loads the data into the Power BI model

Transform Data: Opens Power Query to clean, filter, and shape the data before loading

9. Why might you see an error when connecting to a SQL database? (Name one reason.)
Incorrect login credentials (e.g., wrong username or password)

10. How do you replace a data source after importing it?
In Power BI:

Go to Transform Data → Data Source Settings → select the source → click Change Source…

11. Write the M-code to import only rows where Quantity > 1.
m
Copy
Edit
= Table.SelectRows(Source, each [Quantity] > 1)
12. How would you change the data source if Sales_Data.csv changed?
Go to Transform Data → Data Source Settings → select the current file path → click Change Source…

Browse and select the new file

13. Troubleshoot: Your CSV import fails due to a "mixed data type" error—how do you fix it?
In Power Query, manually set the correct data type for each column

Or use Table.TransformColumnTypes to explicitly convert columns to specific types

14. Connect to a live SQL database with parameters (e.g., filter by year).
Create a parameter in Power Query (Home → Manage Parameters)

Use the parameter in a native SQL query, e.g.:

sql
Copy
Edit
SELECT * FROM Sales WHERE YEAR(OrderDate) = @Year
Or dynamically filter using the parameter in Power Query steps

15. How would you automate data imports using Power BI and Power Automate?
In Power Automate, create a flow that:

Triggers on a schedule or event (e.g., file updated in SharePoint)

Uses the Power BI connector to refresh a dataset



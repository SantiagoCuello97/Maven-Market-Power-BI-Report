# Maven Market Business Intelligence Project

![2](https://github.com/user-attachments/assets/b7f7b4b3-a7ef-4e4c-b569-a010731f559e)

This project covers the complete workflow of Business Intelligence using data from Maven Market, a multinational grocery chain with locations in Canada, Mexico, and the United States. The project starts with data connection and modeling and concludes with creating interactive reports in Power BI. It is divided into four main phases:

## Table of Contents
- [Part 1: Connecting & Shaping Data](#part-1-connecting--shaping-data)
- [Part 2: Building the Data Model](#part-2-building-the-data-model)
- [Part 3: Adding DAX Measures & Calculated Columns](#part-3-adding-dax-measures--calculated-columns)
- [Part 4: Building the Interactive Report](#part-4-building-the-interactive-report)

## Part 1: Connecting & Shaping Data
1. **Initial Setup**: 
   - Automated data modeling options were disabled.
   - The data load locale was set to U.S. English.

2. **Data Load**: 
   - CSV files for customers, products, stores, regions, calendar, returns, and transactions were imported and structured.

3. **Table Transformations**:
   - In the **Customers** table:
     - New columns for full name and birth year were created.
     - A conditional column indicated if customers have children.
   - In **Products**:
     - Columns for discount price and average price by brand were added.
     - Null values in the recyclable and low-fat columns were corrected.
   - In **Stores**:
     - Columns for full address and area code were added.
   - In **Calendar**:
     - Columns were created for week start, day, month, quarter, and year.

4. **File Combination**: 
   - Transaction files from different years were combined, and data types were adjusted.

5. **Refresh Settings**: 
   - Only the main data tables were enabled for report refresh.

## Part 2: Building the Data Model
1. **Relationship Modeling**: 
   - In the Model view, data tables were connected with lookup tables using primary/foreign keys, establishing one-to-many, single-directional relationships.

2. **Snowflake Schema**: 
   - A snowflake schema connected lookup tables (e.g., Stores and Regions), feeding into data tables.

3. **Hiding Foreign Keys**: 
   - Foreign keys were hidden from the data view to simplify the report model.

4. **Formatting & Categorization**: 
   - Date, currency, and geographic formats were updated across tables.

## Part 3: Adding DAX Measures & Calculated Columns
1. **Calculated Columns**: 
   - Columns such as “End of Month” and “Weekend” were added in Calendar, along with age, priority level, and country abbreviations in Customers, and years since last remodel in Stores.

2. **Key Metrics**:
   - Measures calculated quantities sold and returned, showing an average return rate of 0.99%.
   - Metrics for transaction and return counts assessed performance.
   - Measures for total revenue, cost, and profit margin achieved a 59.67% profit margin.
   - Weekend and weekday revenue breakdowns provided sales insights.
   - YTD and 60-day revenue measures tracked sales performance over time.

3. **Month-over-Month Comparisons**: 
   - Measures included last month’s transactions, revenue, profit, and returns, along with a revenue target metric that increased by 5% over the prior month.

## Part 4: Building the Interactive Report
1. **Report Setup**: 
   - The main report tab was renamed "Topline Performance" and included the Maven Market logo.

2. **Matrix & KPI Visualization**: 
   - The matrix visual displayed transactions, profit, and return rate by product brand.
   - KPI cards highlighted current month transactions, profit, and returns.

3. **Map & Breakdown Charts**: 
   - An interactive map visualized transactions by city, complemented by a treemap showing transaction breakdown by country, state, and city.

4. **Revenue Trend**: 
   - A column chart displayed weekly revenue trends, and a gauge chart compared revenue against targets.

5. **Bookmarks & Notes**: 
   - Specific bookmarks, such as “Portland 1000 Sales,” and a “Notes” page with navigation buttons highlighted key findings.

The final report delivers an interactive experience, enabling users to analyze key business metrics and make data-informed decisions through integrated Power BI insights.

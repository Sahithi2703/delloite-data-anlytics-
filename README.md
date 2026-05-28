# delloite-data-anlytics-
The dashboard shows the total machine downtime for each factory and device type. 
The factory with the tallest bar has the highest downtime and indicates the most operational issues. 
Using the filter helps analyze which device types contributed most to downtime in that factory.
## Objective of the Task
You need to analyze machine telemetry data using Tableau and identify which factory has the highest machine downtime.
The data is stored in a JSON file and contains machine status information such as:
1. Install Tableau and open it.
2. Extract `daikibo-telemetry-data.json.zip`.
3. Import the JSON file into Tableau.

   * Select/check **all schema levels** while importing.
4. Create a Calculated Field:

   * Name: `Unhealthy`
   * Formula:
```tableau
IF [status] = "unhealthy" THEN 10 ELSE 0 END
```
5. Create Sheet 1:

   * Name: `Down Time per Factory`
   * Rows → Factory
   * Columns → SUM(Unhealthy)
   * Bar chart
6. Create Sheet 2:
   * Name: `Down Time per Device Type`
   * Rows → Device Type
   * Columns → SUM(Unhealthy)
   * Bar chart
7. Create Dashboard:
   * Add both sheets.
8. Make first chart a filter:
   * Click chart dropdown → “Use as Filter”
9. Click the factory with the highest bar (most downtime).
10. Take screenshot of dashboard and upload it.



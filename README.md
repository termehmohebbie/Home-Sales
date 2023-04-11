# Home_Sales
## Activity 
In this challenge, we used our knowledge of SparkSQL to determine key metrics about home sales data such as the number of bedrooms, bathrooms, floors, square footage, year built and sale price. Then used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Instructions

- Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.
- Import the necessary PySpark SQL functions for this assignment.
- Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.
- Create a temporary table called home_sales.
- Answer the following questions using SparkSQL:
.What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
- Cache your temporary table home_sales.
- Check if your temporary table is cached.
- Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
- Partition by the "date_built" field on the formatted parquet home sales data.
- Create a temporary table for the parquet data.
- Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
- Uncache the home_sales temporary table.
- Verify that the home_sales temporary table is uncached using PySpark.
- Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.

## Results
### Average Price for a Four Bedroom House sold in each year
![WhatsApp Image 2023-04-11 at 12 46 24 PM](https://user-images.githubusercontent.com/114199979/231232897-e5c429aa-6017-47f8-b658-bfe350b6a427.jpeg)


### Average Price of a House with 3 Bedrooms and 3 Bathrooms sold in each year
![WhatsApp Image 2023-04-11 at 12 53 55 PM](https://user-images.githubusercontent.com/114199979/231234843-76a34e23-ee09-43fd-9913-9dfbc261966e.jpeg)


### Average Price of a House with 3 Bedrooms, 3 Bathrooms, 2 Floors and is greater than or equal to 2,000 square feet sold in each year
![WhatsApp Image 2023-04-11 at 12 57 00 PM](https://user-images.githubusercontent.com/114199979/231235484-42485c0b-3e80-4634-88f0-fdba5aaf8ec1.jpeg)


### Ratings for Average Price of Houses costing more than or equal to $350,000
![WhatsApp Image 2023-04-11 at 1 00 33 PM](https://user-images.githubusercontent.com/114199979/231236389-f25d07c2-9cb4-4c6b-9a00-40f00e53ccc0.jpeg)

### Runtime for different methods
* Uncached : 0.9923596382141113 seconds
* Cached : 0.557523250579834 seconds
* Parquet Partitioned : 0.9352474212646484 seconds

This analysis shows that using cached data or the parquet data frame, we can have faster runtime as compared to querying the original data.

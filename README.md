# Home_Sales

# Summary Report
This report presents the findings of our analysis of a home sales dataset. We have used PySpark to perform various operations, including reading the dataset, creating temporary views, running SQL queries, caching, and saving the data in Parquet format.


<p align="center">
  <img width="460" height="500" src="https://user-images.githubusercontent.com/97980927/228965889-f04e0db0-04b7-415c-bda9-ad8a1f13aee9.png">
</p>


** The dataset was read from an AWS S3 bucket into a PySpark DataFrame.
** A temporary view called "home_sales" was created from the DataFrame to enable SQL queries.
** The average price for a four-bedroom house sold in each year was calculated and rounded to two decimal places.
** The average price of a home for each year built with 3 bedrooms and 3 bathrooms was calculated and rounded to two decimal places.
** The average price of a home for each year built with 3 bedrooms, 3 bathrooms, two floors, and at least 2,000 square feet was calculated and rounded to two decimal places.
** The "view" rating for the average price of a home greater than or equal to $350,000 was calculated and rounded to two decimal places. The runtime of the query was determined.
** The temporary table "home_sales" was cached to improve query performance.
** Using the cached data, the query filtering out the view ratings with an average price greater than or equal to $350,000 was run again. The runtime was determined and compared to the uncached runtime.
** The DataFrame was written to a Parquet file, partitioned by the "date_built" field.
** The Parquet formatted data was read into a new DataFrame and a temporary table was created for it.
** The query filtering out the view ratings with an average price greater than or equal to $350,000 was run using the Parquet DataFrame. The runtime was determined and ** compared to the cached version.
** The "home_sales" temporary table was uncached and verified to be no longer cached in memory.

## Our findings indicate that caching can improve query performance, especially for larger datasets and more complex queries. Additionally, saving data in Parquet format allows for more efficient querying and storage, as well as partitioning based on specific columns for better performance.

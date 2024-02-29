# Customer Segmentation Through Purchase History Data

## Problem Statement - 
  Aim to utilize the potential of purchase history data to segment customers effectively, facilitating personalized marketing campaigns and maximizing customer satisfaction.

### Dataset Information -
Raw Dataset Info - 2.6 Million records and 8 columns: event_time, order_id, product_id, category_id, category_code, brand, price, user_id.
Clean Dataset Info - 2 Million records and 19 columns: user_id,	order_id,	category_id,	brand,	price,	cat_1,	cat_2,	cat_3,	max_purchase_by_user,	class_id,	class_category,	recency,	frequency,	monetary,	customer_type,	cust_value,	Date,	Time,	spending.


## Data Cleaning & Preprocessing -
1. Removed duplicate records .
2. Kept the data for year 2020 only as there were only 2 distinct years(1970,2020).
3. Removed the records ,where brand values are none.
4. Assign category as miscellaneous where null values are present.
5. Split the category_code column into 3 columns (cat_1,cat_2,cat_3) on the occurrence of dot ‘.’
6. Calculated  average of price column and assign that value to records where price were zero.
7. Among 2 million records , 1.5 million user ids are not available.
8. The challenge here was to fill null values of user id from available distinct user id such that it should not affect the consistency of data.
9. Calculated the count of distinct user IDs for each category and assigned random user IDs to null values on basis of category column.


[ Visualization in Tableau ](https://public.tableau.com/app/profile/tejas.shinde6818/viz/CDAC-Project_17086852664780/CustomerSegmentationDashboard?publish=yes)

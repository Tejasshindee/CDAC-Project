# Customer Segmentation Through Purchase History Data

## Problem Statement : 
  Aim to utilize the potential of purchase history data to segment customers effectively, facilitating personalized marketing campaigns and maximizing customer satisfaction.

### Dataset Information :
Raw Dataset Info - 2.6 Million records and 8 columns: event_time, order_id, product_id, category_id, category_code, brand, price, user_id.

Clean Dataset Info - 2 Million records and 19 columns: user_id,	order_id,	category_id,	brand,	price,	cat_1,	cat_2,	cat_3,	max_purchase_by_user,	class_id,	class_category,	recency,	frequency,	monetary,	customer_type,	cust_value,	Date,	Time,	spending.


## Data Cleaning & Preprocessing :
- Removed duplicate records.
- Kept the data for year 2020 only as there were only 2 distinct years(1970,2020).
- Removed the records ,where brand values are none.
- Assign category as miscellaneous where null values are present.
- Split the category_code column into 3 columns (cat_1,cat_2,cat_3) on the occurrence of dot ‘.’
- Calculated  average of price column and assign that value to records where price were zero.
- Among 2 million records , 1.5 million user ids are not available.
- The challenge here was to fill null values of user id from available distinct user id such that it should not affect the consistency of data.
- Calculated the count of distinct user IDs for each category and assigned random user IDs to null values on basis of category column.

## RFM Model :
- RFM stands for Recency, Frequency, Monetary.
- It is a marketing analysis technique used to evaluate customer behavior.
- It is ideal for numerical data.
- As purchase dataset includes transactional information like order_id, event_time, price. RFM model will be perfectly fit for this scenario.

## K-Means Clustering :
- Well-suited for segmenting customers based on RFM metrics.
- Efficiently partitions the data into clusters by minimizing the sum of squared distances between data points.
- Assemble RFM score into single feature vector.
- Apply trained K-means model to make the predictions, assigning each customer to the nearest cluster centroid.
- Interpret resulting clusters to understand customer segments based on purchasing behavior.


## Visualization using Tableau :
Plotted graphs that will interpret the segmentation of customers on various factors.
[Here are some graphs](https://public.tableau.com/app/profile/tejas.shinde6818/viz/CDAC-Project_17086852664780/CustomerSegmentationDashboard?publish=yes)

## Conclusion :


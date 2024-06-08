# Amazon-Order_Report

1- Our Data contains order details for duration March, April, May, June for year 2022, which all were ordered from Amazon.in.

2- Order details order no, shipping state, shipping city, order status, amount, B2B or B2C etc.

3- Our target is to create dashboard which represents total order amount by month, state. Number of orders by business type, merchant type, by shipping state. Also,
   all of it can be filtered by state.
   
4- As expected, our data wasn't 100% ready for visualization, needed some transformation.

5- There were around 60 unique entries in state column. As we know there are total 28 states and 8 territories.

6- Other values were duplicates in the form of lower case or abbreviations. Therefore, all entries converted into uppercase.

7- Lot of columns have null values, needed to remove before loading the data. The column "fulfilled by" have around 70% null values, therefore it got dropped.

8- Around 6% of data was null in Amount column, we tried to fill it all by mean and mode values simuntaneously. But we witnnesed a unnecessary peak in kde plot
   when data with null values and data without it compared. Therefore, we didn't moved forward with mean and mode method.
   
9- Instead of mean and mode null values in "Amount" column filled with forwad fill and our kde plot overlapped properply.

10- In the currency column, null values filled with "INR" as our whole data is from Indian market.

11- The courier satatus column is also filled with mode value.

12- After all these tranformation our data is ready for transformation. Please refer to ipynb file for pandas code and image Power Bi dashboard.

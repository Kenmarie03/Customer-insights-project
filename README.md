# Customer-insights-project
Entry-level data analysis project demonstrating data cleaning, visualization, and insights using Python.

Python 
import pandas as pd 
#Load your data
df = pd.read_csv('Customer_data.cs)

# Remove Duplicate customer IDs
df.drop_duplicates(subset=['custom_id' ], keep="first , inplace=True) 

# Fill the missing age with the median 
median_age =df[ 'age' ].median() 
df[ 'age' ].fillna(median_age, inplace=True

#Convert purchase_data to datatime objects
df[ 'purchase_date'  ] = pd.to_date(df[  'purchase_date' ] ) 

print( " Data cleaning complete! ) 


import matplotib.pyplot as plt 
import seaborn as sns

# Distribution of customer ages 
plt.figure(figsize=( 10, 6)) 
sns.histplot(df[ 'age' ], bins=20, kde=True
plt.ylabel( 'age' ) 
plt.xlabel( 'Number of customers' ) 
plt.show() 


# Total spending by product category
category_sopending = df.groupby( 'product_category') [ 'price' ].sum().sort_values(ascending=Flase
plt.figure(figsize=(12, 7)
sns.barplot(x=category_spending.index, y=category_spending.values
plt.title( 'Total Spending by Prodcut Category' )
plt.xlabel( 'Product Category' )
plt.ylabel( 'Total Spending ($) ' ) 
ks(rotation=45, ha='right' ) 
t_layout() 
() 

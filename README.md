# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv('Data_set.csv')
df.info()
print(df.isnull().sum())
df['show_name']=df['show_name'].fillna(df['show_name'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].median())
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.info()
print(df.isnull().sum())
```
# OUPUT
### BEFORE CLEANING THE DATA

![before-cleaning-data](https://user-images.githubusercontent.com/93427278/160145076-d8c74d91-2536-4c16-88b8-4d718d716b3d.png)

### AFTER CLEANING THE DATA

![after-cleaning-data](https://user-images.githubusercontent.com/93427278/160145033-3f289ece-85ca-47e7-bc3d-3722919e6d06.png)

# RESULT
Thus, the given data is read, cleaned and the cleaned data is saved into the file.

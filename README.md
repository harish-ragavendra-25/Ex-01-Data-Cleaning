# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)

df.head(5)

df.tail(5)

df.describe()

df.info()

df.isnull().sum()

df=df[~df.duplicated()]
print(df)

df['Gender'].fillna(value=df['Gender'].mode())

df['LoanAmount'].fillna(value=df['LoanAmount'].median())
```

# OUPUT
![ex1output](https://user-images.githubusercontent.com/114852180/226175948-2e7557e4-6052-4487-8a2a-7a4b8dbac8a8.png)

![head and tail](https://user-images.githubusercontent.com/114852180/226175971-feb08341-5c1e-45a2-8d57-66bc1bce8981.png)

![describe and info](https://user-images.githubusercontent.com/114852180/226176000-ea5c964c-6c16-4bbd-8839-67d57d618635.png)


![isnull](https://user-images.githubusercontent.com/114852180/226176067-66d59b15-bc04-4ee4-95ef-d8d44dfef950.png)

![mean](https://user-images.githubusercontent.com/114852180/226176220-22300b8c-27b7-49d5-9cf6-91ee68472052.png)

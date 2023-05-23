# Titanic_Dataset_Pandas
Titanic Survival Prediction Analysis


## Pandas :

## Data Structures
- Series: A one-dimensional labeled array capable of holding any data type. It is similar to a column in a spreadsheet or a dictionary in Python.

## Functions:
pd.Series(data, index): Create a new Series object from data and optional index labels.

## Methods:
- s.values:     Retrieve the values of the Series.
- s.index:      Retrieve the index labels of the Series.
- s.head(n):    Return the first n rows of the Series.
- s.tail(n):    Return the last n rows of the Series.
- s.describe(): Generate descriptive statistics of the Series.

## DataFrame: 
- A two-dimensional labeled data structure with columns of potentially different data types. 
   - It is similar to a table in a relational database or a spreadsheet.

## Functions:
pd.DataFrame(data, index, columns): Create a new DataFrame object from data, index labels, and column names.

## Methods:

- df.head(n):      Return the first n rows of the DataFrame.
- df.tail(n):      Return the last n rows of the DataFrame.
- df.describe():   Generate descriptive statistics of the DataFrame.
- df.info():       Display a summary of the DataFrame's metadata.
- df.shape:        Retrieve the dimensions (rows, columns) of the DataFrame.
- df.columns:      Retrieve the column names of the DataFrame.
- df.index:        Retrieve the index labels of the DataFrame.
- df.values:       Retrieve the values of the DataFrame as a NumPy array.
- df.sort_values(by): Sort the DataFrame by one or more columns.
- df.groupby(by):     Group the DataFrame by one or more columns.
- df.dropna():        Remove rows with missing values.
- df.fillna(value):   Replace missing values with a specified value.

## Data Manipulation :

pd.concat(objs):           Concatenate multiple Series or DataFrames vertically or horizontally.
df.merge(right):           Merge two DataFrames based on a common column.
df.join(right):            Join two DataFrames based on their indexes.
df.pivot(index, columns, values): Reshape the DataFrame by converting unique values of one column into multiple columns.
df.melt(id_vars):          Unpivot a DataFrame from wide format to long format.
df.apply(func):            Apply a function to each element or row/column of the DataFrame.
df.map(dict):              Map values of a Series to new values using a dictionary.
df.rename(columns, index): Rename columns or index labels of the DataFrame.
df.sort_values(by):        Sort the DataFrame by one or more columns.
df.drop_duplicates():      Remove duplicate rows from the DataFrame.

## Data Analysis:

- df.describe():       Generate descriptive statistics of the DataFrame.
- df.corr():           Compute pairwise correlation of columns.
- df.cov():            Compute pairwise covariance of columns.
- df.mean(), df.median(), df.min(), df.max():     Compute various statistical measures.
- df.groupby(by):      Group the DataFrame by one or more columns and perform aggregations.
- df.value_counts():   Count unique values in a column.
- df.isnull():         Check for missing values in the DataFrame.
- df.dropna():         Remove rows with missing values.
- df.fillna(value):    Replace missing values with a specified value.
- df.sample(n):        Randomly sample rows from the DataFrame.

## What difference between .iloc[] and .loc[] :

   * data.iloc[row_indexer, column_indexer]
   * data.loc[row_indexer, column_indexer]

    - data.iloc[0]              # Access the first row
    - data.iloc[:, 2]           # Access the third column for all rows

    - data.loc['A']             # Access the row with label 'A' 
    - data.loc[:, 'Column1']    # Access 'Column1' for all rows

  
- iloc[] uses integer positions for indexing, while .loc[] uses labels or conditions.
- .iloc[] is primarily used when you want to access data based on its position, without relying on the labels or names.

- .loc[] is mainly used when you want to access data based on labels or conditions, such as specific row or column labels, or boolean conditions on the data.

-----------------------------------------------------------------------------------------------------------
## Categorical Data:

- Categorical data represents variables that can take on a limited number of distinct categories or levels. These categories can be represented by strings, integers, or other data types. Examples of categorical data include gender (e.g., "Male" or "Female"), product categories (e.g., "Electronics," "Clothing," "Furniture"), or rating levels (e.g., "Low," "Medium," "High"). 
- Categorical data is typically non-numeric and is often represented as text values.

In pandas, categorical data can be represented using the Categorical data type. It provides efficient storage and enables various operations specific to categorical data.

## Numerical Data:

- Numerical data, as the name suggests, represents quantitative values that can be measured or expressed as numbers. 

  Numerical data can be further divided into two subtypes:

- a. ## Continuous numerical data: Continuous numerical data represents variables that can take any value within a certain range or interval. Examples include temperature, height, weight, or time. Continuous numerical data is typically represented using floating-point numbers.

- b. ## Discrete numerical data: Discrete numerical data represents variables that can only take specific, separate values. Examples include the number of siblings, the count of items, or the number of occurrences of an event. Discrete numerical data is typically represented using integers.

- In pandas, numerical data is often stored as either int64 (integer) or float64 (floating-point) data types.

- Pandas provides various functionalities to work with both categorical and numerical data, including data manipulation, 
aggregation, and analysis. 
-------------------------------------------------------------------------------------------------------------

## Data Structures
# Series :

- pd.Series(data, index): 
    - Creates a new Series object from data and optional index labels.



## DataFrame
- pd.DataFrame(data, index, columns): 
    - Creates a new DataFrame object from data, index labels, and column names.

data = {'Name': ['John', 'Emma', 'Peter'],
        'Age': [25, 30, 28],
        'Country': ['USA', 'UK', 'Canada']}

df = pd.DataFrame(data)

print(df)
--------------------------------------------------------------------------------------------------------------

## What diffrence between User "objects", "float64", and "int64" :
## object: 
 - The "object" data type in pandas represents strings and mixed data types. It is a general-purpose data type that can store any Python object. It is commonly used when a column contains a mixture of different data types or when the exact data type is unknown. Examples include strings like "Hello" or "123", which can also include non-numeric characters.
## float64: 
- The "float64" data type represents floating-point numbers, which are decimal numbers. It provides a high level of precision for numerical calculations. Examples of float values are 3.14 or 2.71828. Float values can include a decimal point and can be positive or negative.
## int64: 
- The "int64" data type represents integer numbers, which are whole numbers without a fractional component. It is used for storing numerical values without decimal places. Examples of int values include 42, -10, or 1000.

--------------------------------------------------------------------------------------------------------------

## what does mean data["Survived"] == 0 in pandas:

In pandas, data["Survived"] == 0 is a conditional statement that is used as a filter to select specific rows from a DataFrame based on a particular condition.

Let's say you have a DataFrame called data that contains information about passengers on a ship, and one of the columns is "Survived" which indicates whether a passenger survived (1) or did not survive (0).

By using data["Survived"] == 0, you are checking for rows where the "Survived" column has a value of 0, meaning the passenger did not survive. This creates a Boolean mask that selects only the rows where the condition is True.

## data["Survived"] == 1 vs data["Survived"] == 0 :

- data["Survived"] == 1 means checking the rows where the "Survived" column has a value of 1, indicating the passengers who survived.

- Similarly, data["Survived"] == 0 means checking the rows where the "Survived" column has a value of 0, indicating the passengers who did not survive.

- By using these conditional statements, you can divide the data into two categories based on the value of the "Survived" column: survivors and non-survivors. You can then perform specific tasks or analysis on each of these categories separate.

---------------------------------------------------------------------------------------------------------------

## Difference between loc() and iloc() in Pandas DataFrame :
   * https://www.geeksforgeeks.org/difference-between-loc-and-iloc-in-pandas-dataframe/

- functioning. loc() and iloc() are used for slicing data from the Pandas DataFrame.

### The loc() function :
 - is label based data selecting method which means that we have to pass the name of the row or column which we want to   select
 - loc() can accept the boolean data unlike iloc().

### The iloc() function :
 - is an indexed-based selecting method which means that we have to pass an integer index in the method to select a specific row/column. 
 - This method does not include the last element of the range passed in it unlike loc(). 
 - iloc() does not accept the boolean data unlike loc().

----------------------------------------------------------------------------------------------------------------

### Working with Missing Data in Pandas :

- Pandas treat None and NaN as essentially interchangeable for indicating missing or null values. To facilitate this convention, there are several useful functions for detecting, removing, and replacing null values in Pandas DataFrame :

- isnull()
- notnull()
- dropna()
- fillna()
- replace()
- interpolate()

-------------------------------------------------------------------------------------------------------------------

## Delete a column from a Pandas DataFrame 
- " drop() " : Remove specific single columns. 
    - df.drop(['A'], axis=1) 

- " drop() " : Remove specific multiple columns
    - df.drop(['XX', 'XX'], axis=1) 

- " drop() " : Remove columns based on column index
    - df.drop(df.columns[[0, 0, 0]], axis=1, inplace=True) 

- " Drop Columns from a Dataframe using iloc[] and drop() method. 
    - df.drop(df.iloc[0, 0, 0], inplace=True, axis=1)

-------------------------------------------------------------------------------------------------------------------

## DataFrame.dropna() Method:

 - Sometimes CSV file has null values, which are later displayed as NaN in Pandas DataFrame. Pandas dropna() method allows the user to analyze and drop Rows/Columns with Null values in different ways. 
     - axis: axis takes int or string value for rows/columns. Input can be 0 or 1 for Integer and ‘index’ or ‘columns’ for String. 

--------------------------------------------------------------------------------------------------------------------

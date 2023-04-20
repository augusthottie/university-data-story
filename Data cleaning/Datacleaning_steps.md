# Data cleaning steps

To clean the data, you can follow these steps using Python and related libraries:

## Merge all files

- If you have multiple data files to be cleaned, you can use a library like Pandas to read and merge them into a single DataFrame.
- This can be done using the pd.concat() function, which concatenates DataFrames along a given axis (usually rows), and the resulting merged DataFrame can be used for further cleaning tasks.

## Remove inconsistent rows

- You may come across rows in the dataset where the Year column has values like 2022 or 2023, and a large portion of the data in those rows is missing or null. In such cases, you can use Pandas' powerful data filtering capabilities to identify and remove these rows from the DataFrame.
- This can be achieved using boolean indexing and the dropna() function, which removes rows with any missing values.

## Replace null values  Replace null values in "rank" column

-The next step is to handle missing values in the "rank" column. One approach is to replace them with an appropriate value, such as the median or 50% quantile of the available data. This can be done using the fillna() function in Pandas, which fills null values with a specified value or method.

- After filling the null values, you can convert the "rank" column to the desired data type, such as int64, using the astype() function.

## Replace null values in overall and teaching scores

- Similar to the "rank" column, you can replace missing values in the "overall" and "teaching" columns with an appropriate value, such as the 25% quantile of the available data. This can be achieved using the fillna() function in Pandas, followed by converting these columns to the desired data type, if needed.

## Convert columns to numeric type

- Some columns in the dataset, such as "scores_international_outlook" and "scores_industry_income", may be stored as strings or objects. To perform numerical calculations or analysis on these columns, it is important to convert them to numeric data types.
- This can be done using the pd.to_numeric() function in Pandas, which converts a column to a numeric type, while handling any errors or inconsistencies in the data.

## Handle non-null values like "-"

- Sometimes, you may encounter non-null values in the dataset that are represented as special characters, such as "-". These values can affect data analysis and calculations. To address this, you can use Pandas to replace these non-null values with an appropriate value, such as the mean or median of the respective column.
- This can be done using the replace() function in Pandas, followed by performing necessary calculations or analysis on the cleaned dataset.

In summary, data cleaning involves various tasks such as merging data, handling missing values, converting columns to appropriate data types, and addressing inconsistencies in the data. Python and its libraries, such as Pandas, provide powerful and flexible tools to perform these tasks efficiently and effectively.

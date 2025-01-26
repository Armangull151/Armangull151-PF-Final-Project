
# Project: Pandas Analytical Data Analysis

## Overview
This project involves analyzing data using Python's powerful **pandas** library. The notebook contains various steps, including data loading, cleaning, exploration, visualization, and analysis to derive meaningful insights.

## Features
- Data cleaning and preprocessing
- Exploratory data analysis (EDA)
- Visualization of trends and patterns
- Summary statistics and insights

## Getting Started

### Prerequisites
- Python 3.x
- Jupyter Notebook
- Required libraries: pandas, numpy, matplotlib, seaborn (install these using `pip install <library_name>`)

### Installation
1. Clone this repository or download the project files.
2. Ensure all dependencies are installed (see above).

## Notebook Outline
- ## NAME : **M REHMAN FAROOQ**
  ### ROLL.NO : AI-1B-109

- ### import pandas

### Example Code:
```python
import pandas as pd
```

- ### 1. Read CSV file

### Example Code:
```python
df=pd.read_csv("world happiness report.csv")  #read the csv file
df
```

- ### 2. Data Inspection

### Example Code:
```python
df.head()  #display the first 5 rows of the dataframe
# df.head(10)  #display the first 10 rows of the dataframe
```

### Example Code:
```python
df.tail()  #display the last 5 rows of the dataframe
# df.tail(10)  #display the last 10 rows of the dataframe
```

### Example Code:
```python
df.sample()  #display a random row from the dataframe   
```

### Example Code:
```python
df.shape #display the number of rows and columns in the dataframe
```

### Example Code:
```python
df.size   
```

### Example Code:
```python
df.dtypes  #display the data types of each column in the dataframe
```

### Example Code:
```python
df.values  #display the values in the dataframe
```

### Example Code:
```python
df.info()  # DataFrame ke structure aur data types ki information deta hai.
```

### Example Code:
```python
df.index #display the index of the dataframe
```

### Example Code:
```python
df.describe()  #display the statistical summary of the dataframe
```

### Example Code:
```python
df.describe().include=all # DataFrame ke numerical columns ke liye basic statistics provide karta hai.Numerical columns ke statistics dikhata hai jaise mean, median, standard deviation, minimum aur maximum values.
df
```

### Example Code:
```python
df.columns  #DataFrame ke columns ke names ko display karta hai.
```

### Example Code:
```python
# df['Overall rank']   #single columns ko select karta hai.
df[["Social support",'Generosity']]  # Multiple columns ko select karta hai.
```

### Example Code:
```python
df.Score   #Column ke name ke sath DataFrame ke column ko select karta hai.
```

### Example Code:
```python
df.loc[2]   #Specific row ko select karta hai.
```

### Example Code:
```python
df.loc[35:40]  #Specific range of rows ko select karta hai.
```

### Example Code:
```python
df.loc[35:40, ['Country or region','Score']]  #Specific range of rows aur columns ko select karta hai.
```

### Example Code:
```python
df.iloc[2,-1]  #[row_index, column_index]  Specific row and column ko select karta hai.
```

### Example Code:
```python
df.iloc[[2,3],8] #Multiple rows and specific column ko select karta hai.
```

### Example Code:
```python
df.iloc[2:5,8]  #Range of rows and specific column ko select karta hai.
```

### Example Code:
```python
df.iloc[2:5,8:10]  #Range of rows and columns ko select karta hai.
```

- ### 4. Data Filtering

### Example Code:
```python
df[df['Social support'] > 1]  #Dataframe ke specific column ke values ko filter karta hai.
```

### Example Code:
```python
df[df["Score"] > 4]  #Dataframe ke specific column ke values ko filter karta hai.
```

- ### 5. Data Manipulation

### Example Code:
```python
df.insert(5, "joy", 5)    #DataFrame me naya column insert karta hai.
df
```

### Example Code:
```python
df['In.mean']=df["Score"].mean()   #DataFrame me naya column insert karta hai.
df['In.mean']  
df
```

### Example Code:
```python
df['Social support'].fillna(('7.8'),inplace=True)    #DataFrame me missing values ko fill karta hai.
df['Social support']
```

### Example Code:
```python
df["unhealthy life expectancy"] = 10   #new column add karta hai.
df
```

### Example Code:
```python
df.rename(columns={"unhealthy life expectancy":"unhealthy_life_expect"},inplace=True)  #column ka name change karta hai.
df
```

### Example Code:
```python
df.drop(columns=["unhealthy_life_expect"],inplace=True)  #column ko delete karta hai.
df
```

### Example Code:
```python
df.sort_values(by="Country or region") #DataFrame ko specific column ke values ke basis par sort karta hai.
```

- ### 6. Handling Missing Data

### Example Code:
```python
df.isnull()   #DataFrame ke har element ko check karta hai ke wo null hai ya nahi.
```

### Example Code:
```python
df.isnull().sum()  #DataFrame ke har column me kitne null values hai wo count karta hai.
```

### Example Code:
```python
df.dropna()  #DataFrame ke null values ko drop karta hai.
```

### Example Code:
```python
df.fillna(0)  #DataFrame ke null values ko fill karta hai.
```

### Example Code:
```python
del df["joy"] #column ko delete karta hai.
df
```

### Example Code:
```python
df["adding_Score_Generosity"]=df["Score"]+df["Generosity"]  #DataFrame ke columns ke values ko add karta hai.
df
```

### Example Code:
```python
df = df.drop("give specific row number")  #specific row ko delete karta hai.
df
```

- ### 7. Grouping and Aggregation

### Example Code:
```python
df.groupby("Social support").describe()   #`DataFrame ko specific column ke basis par group karta hai.

```

### Example Code:
```python
df.agg({"Generosity":"sum"})  #DataFrame ke specific column ke values ka sum calculate karta hai.
```

- ### 8. Input/Output

### Example Code:
```python
df.to_csv("new.csv")  #DataFrame ko csv file me convert karta hai.
```

### Example Code:
```python
df2=pd.read_csv('new.csv')
df2
```

- ### 9. Merging and Joining

### Example Code:
```python
pd.merge(df,df2,on="Country or region")  #DataFrame ko merge karta hai.
```

### Example Code:
```python
df.join(df2, lsuffix='_left', rsuffix='_right')  # DataFrame ko join karta hai. 
```

- ### 10. Statistical analysis

### Example Code:
```python
df["Score"].mean()   #DataFrame ke specific column ke values ka mean calculate karta hai.
```

### Example Code:
```python
df["Score"].median()
```

### Example Code:
```python
df["Score"].mode()  #DataFrame ke specific column ke values ka mode calculate karta hai.
```

### Example Code:
```python
df["Score"].min()   #DataFrame ke specific column ke values ka minimum value calculate karta hai.
```

### Example Code:
```python
df["Score"].max()   #DataFrame ke specific column ke values ka maximum value calculate karta hai.
```

### Example Code:
```python
df["Score"].std()  #DataFrame ke specific column ke values ka standard deviation calculate karta hai.
```

- ### 11. Handling Duplicates

### Example Code:
```python
df.duplicated  #DataFrame me duplicate values ko check karta hai.
```

### Example Code:
```python
df.duplicated("Score").sum()  #DataFrame me kitne duplicate values hai wo count karta hai.
```

### Example Code:
```python
df.drop_duplicates()  #DataFrame me duplicate values ko drop karta hai.
```

### Example Code:
```python
df["Score"] = df["Score"].replace(3.083, 7)   #DataFrame ke specific column ke values ko replace karta hai.
df
```

- ### 12. Change datatype

### Example Code:
```python
df["Social"] = df["Score"].astype(str)
df.dtypes
```

- ### 13. Visualization

### Example Code:
```python
df["Perceptions of corruption"].value_counts().plot(kind= "area")  #DataFrame ke specific column ke values ko count karta hai.
```

### Example Code:
```python
df["Generosity"].value_counts().plot(kind="line")   #DataFrame ke specific column ke values ko count karta hai.
```

### Example Code:
```python
df["Generosity"].value_counts().plot(kind="kde")
```

### Example Code:
```python
df["Generosity"].value_counts().plot(kind="hist")
```

### Example Code:
```python
df["Generosity"].value_counts().plot(kind="density")
```

### Example Code:
```python
df["Score"].value_counts().plot(kind="pie")  #DataFrame ke specific column ke values ko count karta hai.
```


## Outputs
The notebook generates insightful outputs such as data visualizations, statistical summaries, and trends.

## License
This project is open-source and available for use.

---
*This README was auto-generated from the provided Jupyter Notebook.*

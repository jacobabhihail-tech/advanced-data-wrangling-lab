# Day 2 Cheatsheet

## Missing Values
df.isnull().sum()

## Missing Value Percentage
(df.isnull().sum()/len(df))*100

## Duplicates
df.duplicated().sum()

## View Duplicates
df[df.duplicated()]

## Data Types
df.info()

## Unique Values
df["column"].unique()

## Convert to Datetime
df["order_date"] = pd.to_datetime(
    df["order_date"],
    format="mixed",
    dayfirst=True
)

## Detect Non-Numeric Characters
df["sales"].str.contains(r"[^0-9.]", regex=True)

## Remove Commas
df["sales"] = df["sales"].str.replace(",", "")

## Convert to Numeric
df["sales"] = pd.to_numeric(df["sales"])

## Outlier Detection
df.boxplot(column="sales")
df.boxplot(column="profit")
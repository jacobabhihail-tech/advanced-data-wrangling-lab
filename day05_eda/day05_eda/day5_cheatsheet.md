# Day 5 Cheatsheet

## Distribution
df["sales"].describe()

sns.histplot(df["sales"])

## Skew
df["sales"].skew()

## Correlation
df[
    ["sales","profit","quantity","discount","shipping_cost"]
].corr()

sns.heatmap(
    df[
        ["sales","profit","quantity","discount","shipping_cost"]
    ].corr(),
    annot=True
)

## Anomaly Spotting
sns.boxplot(x=df["sales"])

## Business Insights

df.groupby("category")["sales"].sum()

df.groupby("category")["profit"].sum()

df.groupby("region")["sales"].sum()
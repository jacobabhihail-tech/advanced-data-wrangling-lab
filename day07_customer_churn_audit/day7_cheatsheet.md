# Day 7 Cheatsheet

## Audit

df.info()

df.isnull().sum()

df.duplicated().sum()

## Type Fixes

df["Onboard_date"] = pd.to_datetime(df["Onboard_date"])

## Feature Engineering

df["tenure_group"] = pd.cut(
    df["Years"],
    bins=[0,3,6,10],
    labels=["New","Medium","Old"]
)

## Churn Analysis

df.groupby("tenure_group")["Churn"].mean()

df.groupby("Account_Manager")["Churn"].mean()

df.groupby("Num_Sites")["Churn"].mean()

## Visualization

sns.barplot(...)

plt.show()

## Rule

Turn analysis into business insights.
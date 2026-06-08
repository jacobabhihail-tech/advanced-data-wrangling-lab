# Day 3 Cheatsheet

## Feature Creation
df["profit_margin"] = df["profit"] / df["sales"]

## One-Hot Encoding
pd.get_dummies(df["segment"], prefix="segment", dtype=int)

## Binning
df["sales_category"] = pd.cut(
    df["sales"],
    bins=3,
    labels=["Low", "Medium", "High"]
)

## Scaling
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()
df["sales_scaled"] = scaler.fit_transform(df[["sales"]])

## Datetime Features
df["order_year"] = df["order_date"].dt.year
df["order_month"] = df["order_date"].dt.month
df["order_day"] = df["order_date"].dt.day_name()

## Pipeline
from sklearn.pipeline import Pipeline

sales_pipeline = Pipeline([
    ("scaler", MinMaxScaler())
])
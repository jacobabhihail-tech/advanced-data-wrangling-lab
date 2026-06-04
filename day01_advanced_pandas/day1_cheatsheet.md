# Day 1 Cheatsheet

## Filtering
df[df["sales"] > 500]

## Multiple Conditions
df[(condition1) & (condition2)]

## GroupBy
df.groupby("category")["sales"].sum()

## Multiple Aggregations
df.groupby("category").agg({
    "sales":["sum","mean"]
})

## Pivot Table
pd.pivot_table(
    df,
    values="sales",
    index="category"
)

## Vectorization
np.where(condition, true_value, false_value)
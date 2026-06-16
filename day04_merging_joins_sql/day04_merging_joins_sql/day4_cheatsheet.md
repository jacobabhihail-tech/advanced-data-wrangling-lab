# Day 4 Cheatsheet

## Merge
pd.merge(df1, df2, on="column")

## Inner Join
pd.merge(df1, df2, on="column", how="inner")

## Left Join
pd.merge(df1, df2, on="column", how="left")

## Right Join
pd.merge(df1, df2, on="column", how="right")

## Outer Join
pd.merge(df1, df2, on="column", how="outer")

## Concat
pd.concat([df1, df2])

## Subquery Thinking
avg = df["column"].mean()

df[df["column"] > avg]

## Window Function Thinking
df["group_total"] = (
    df.groupby("group")["value"]
    .transform("sum")
)
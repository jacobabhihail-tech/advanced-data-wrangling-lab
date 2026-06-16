# Day 6 Cheatsheet

## Heatmap
sns.heatmap(df.corr(), annot=True)

## Scatter Plot
sns.scatterplot(data=df, x="sales", y="profit")

## Pairplot
sns.pairplot(df[numeric_columns])

## Dashboard Style Plot
fig, axes = plt.subplots(2, 2)

## Storytelling Rule
Do not describe the chart.

Describe what the chart means for the business.
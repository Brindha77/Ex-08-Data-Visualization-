# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
# DEVELOPED BY : R.BRINDHA
# REG NO : 212222230023
# Reading the given dataset :
```
import pandas as pd
df=pd.read_csv("/content/Superstore (3).csv",encoding='unicode_escape')

df.head()
```
# Data Visualization using Seaborn :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
# 1.Line Plot :
```
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)

sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)

sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
# 2.Scatterplot :
```
sns.scatterplot(x='Category',y='Sub-Category',data=df)

sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)

plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
# 3.Boxplot :
```
sns.boxplot(x="Sub-Category",y="Discount",data=df)

sns.boxplot( x="Profit", y="Category",data=df)
```
# 4.Violin Plot :
```
sns.violinplot(x="Profit",data=df)
```
# 5.Barplot :
```
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)

sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
# 6.Pointplot :
```
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
# 7.Count plot :
```
sns.countplot(x="Category",data=df)

sns.countplot(x="Sub-Category",data=df)
```
# 8.Histogram :
```
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
```
# 9.KDE Plot :
```
sns.kdeplot(x="Profit", data = df,hue='Category')
```
# Data Visualization Using MatPlotlib :
# 1.Plot :
```
plt.plot(df['Category'], df['Sales'])
plt.show()
```
# 2.Heatmap :
```
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
# 3.Piechart :
```
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
```
# 4.Histogram :
```
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
# 5.Bargraph :
```
plt.bar(df.index,df['Category'])
plt.show()
```
# 6.Scatterplot :
```
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
# 7.Boxplot :
```
plt.boxplot(x="Sales",data=df)
plt.show()
```

# OUPUT

# Reading the given dataset :
![1](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/e35b252a-0685-4a25-a356-84758540bfc9)

# Data Visualization Using Seaborn :
# 1.Line Plot :
![2](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/85d6b39d-eebe-424d-8e21-99d2f1f502e0)


![3](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/0d266280-5950-4023-9ad5-4b3a1ac2ed55)


![4](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/d7a2d617-6214-45da-9779-3a6cb9f0d033)


# 2.Scatterplot :
![5](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/213e1cb0-3bc3-4dca-b8f1-174e4d7232c0)


![6](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/a676f7ac-624c-4b0a-88c9-8fed00915bf8)


![7](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/a2e5fbd8-c475-4ead-b625-4c2226aa70d6)


# 3.Boxplot :
![8](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/f3ef8a0d-47af-481b-8b3d-86541e797dfb)


![9](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/9368188a-041e-44f6-96f3-30673d84405f)

# 4.Violin Plot :
![10](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/f951afcc-e3ac-4f19-97ce-54a0a6883cfe)

 
# 5.Barplot :
![11](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/a0c0d306-7037-4f9c-8997-60b338e2bcff)


![12](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/a9875e00-b61b-450b-bc34-5cf9a9c77827)


# 6.Pointplot :
![13](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/dbf4ef7a-fafd-4347-80cc-d6bffc474d83)

# 7.Count plot :
![14](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/1fdf8fea-3065-438e-95c5-179defd8c522)

![15](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/eb8bba04-7ff2-4c41-ad25-39a6c021abb8)

# 8.Histogram :
![16](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/39f0e7f5-1fc8-46cb-ae86-3a207b5cbefd)

# 9.KDE Plot :
![18](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/08ae20d2-d6cd-42cb-95ec-b9ac82d83583)


# Data Visualization Using Matplotlib :
# 1.Plot:
![19](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/7ad01998-daea-4cba-aa65-54876f9925e3)

# 2.Heatmap :
![20](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/8c59b8c1-0838-46aa-bac2-9086836908e0)


# 3.Piechart :
![21](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/a7b890a3-abe6-4fb6-9efd-e472a3890820)


# 4..Histogram :
![22](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/8679d213-b52e-4016-9343-8382745945be)


# 5.Bargraph :
![23](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/83c8a290-1948-42bc-9e8e-ae0a421bb8a8)


# 6.Scatterplot :
![24](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/38d5997c-aca6-4870-be73-bb8d7e78e0ea)


# 7.Boxplot :
![25](https://github.com/Brindha77/Ex-08-Data-Visualization-/assets/118889143/8d4775a7-3fed-49df-b441-e13bd382146a)


# Result :
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.

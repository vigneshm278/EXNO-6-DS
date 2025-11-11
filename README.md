# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("/content/titanic_dataset (1).csv")
 df.head()
```
<img width="1545" height="257" alt="image" src="https://github.com/user-attachments/assets/0f0e2d15-3a52-477a-bf35-9720bb93576c" />


## 1.Line Plot:

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="534" height="435" alt="download" src="https://github.com/user-attachments/assets/34546afc-eb71-4e0c-9bd2-051852825bfd" />


## 2. Multi Line Plot:
```
 x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```
<img width="534" height="435" alt="download" src="https://github.com/user-attachments/assets/fb70b794-2fe2-4f65-a4df-1c542d54538a" />


##  TO VISUALIZE RELATIONSHIPS:
##  1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="686" height="470" alt="download" src="https://github.com/user-attachments/assets/45fcf0ed-2737-46aa-98a7-73b84063f438" />



##  2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="571" height="455" alt="download" src="https://github.com/user-attachments/assets/bf998061-0d82-4c19-ace3-9fed1fe4865a" />


##  3.Bubble Chart

```

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="571" height="455" alt="download" src="https://github.com/user-attachments/assets/f0ee702d-595e-48b0-884f-582839a2ded2" />



 ## TO CAPTURE DISTRIBUTIONS
##  1.Histogram
```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="571" height="432" alt="download" src="https://github.com/user-attachments/assets/e8672f1d-1d73-4930-a078-09d11a1851ae" />




##  2.Box Plot
```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="562" height="455" alt="download" src="https://github.com/user-attachments/assets/c77ba9bb-74e3-41bf-80b3-1107fa4f767a" />




##  3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="571" height="455" alt="download" src="https://github.com/user-attachments/assets/7849439f-d5f8-48e0-ad6d-5c6d9463920a" />




 ## 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="584" height="455" alt="download" src="https://github.com/user-attachments/assets/1d96f4eb-7f4c-445e-aa21-2d70bcdf7705" />





##  5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="596" height="505" alt="download" src="https://github.com/user-attachments/assets/6fa78fcf-75f8-4252-91e9-f69a9c77a7ca" />





# Result:
 
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

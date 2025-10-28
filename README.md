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
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1570" height="257" alt="image" src="https://github.com/user-attachments/assets/8bdde14d-c3a6-4f53-af73-87ed6f0e90e7" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="830" height="580" alt="image" src="https://github.com/user-attachments/assets/dfcdc489-682b-48c9-bb24-a8135f4723c8" />


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

<img width="941" height="587" alt="image" src="https://github.com/user-attachments/assets/71223cb5-f593-4fbf-bdcd-09c8311599d9" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="1660" height="731" alt="image" src="https://github.com/user-attachments/assets/43f14df1-5cfe-49e2-86fd-de9456fda9a0" />


```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="977" height="587" alt="image" src="https://github.com/user-attachments/assets/40c6aaab-b1ab-4397-b42c-fe0fbde48ffe" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="946" height="585" alt="image" src="https://github.com/user-attachments/assets/9d513c39-cf87-4e8f-99c5-cd62acd6485e" />


```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="1030" height="572" alt="image" src="https://github.com/user-attachments/assets/a472b49a-c31d-4bba-9b57-8f3033918be5" />


```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="1650" height="709" alt="image" src="https://github.com/user-attachments/assets/737ec359-d422-4731-bb0a-1ac8aeb65123" />


```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="1030" height="588" alt="image" src="https://github.com/user-attachments/assets/4f717f91-f5d3-4f2d-9cf5-3dc3656f4a1e" />


```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()


```

<img width="1010" height="716" alt="image" src="https://github.com/user-attachments/assets/fd880e1d-2bf0-4670-96f5-c982f1b009e3" />


```


numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="1098" height="648" alt="image" src="https://github.com/user-attachments/assets/ac3895cc-e762-4142-941d-36e80579f8b9" />






# Result:
Thus , to perform data visualization using seaborn python library for the given datas is successfully completed.

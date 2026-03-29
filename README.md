# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
#importing the dataset

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris

iris=load_iris()
df=pd.DataFrame(data=iris.data, columns=iris.feature_names)
```

<img width="1322" height="448" alt="image" src="https://github.com/user-attachments/assets/5dad4536-a74e-495e-ae96-5f045e1e9215" />

```
#Line chart
x=df['sepal length (cm)']
y=df['petal length (cm)']
plt.plot(x,y, color='red',linewidth=1.5)
plt.xlabel('SEPAL LENGTH (in cm)')
plt.ylabel('PETAL LENGTH (in cm)')
plt.show()
```

<img width="1331" height="652" alt="image" src="https://github.com/user-attachments/assets/de7f158c-4023-46fa-9dcd-0de396eacd8e" />

```
#Scatter Plot
plt.scatter(x,y,color='purple',marker='o')
plt.xlabel('SEPAL LENGTH (in cm)')
plt.ylabel('PETAL LENGTH (in cm)')
plt.title('IRIS - SEPAL LENGTH VS PETAL LENGTH')
plt.show()
```

<img width="1335" height="668" alt="image" src="https://github.com/user-attachments/assets/a218f20f-c9bc-4595-ab33-e0f6257f2a14" />


```
import pandas as pd 
import matplotlib.pyplot as plt
data={
    'Study Hours': [1,2,3,4,5,6,7,8,9,10,11,12],
    'Marks': [25,34,38,86,45,49,57,67,65,78,89,99]
}

#Bar Chart
df=pd.DataFrame(data)
plt.bar(df['Study Hours'],df['Marks'], color='blue', width=1.6, hatch='/', edgecolor='black', linewidth=1.5, alpha=0.8)
plt.xlabel('Hours Studied')
plt.ylabel('Marks Scored')
plt.title('Study Hours vs Marks')
plt.plot(df['Study Hours'],df['Marks'],color='red')
plt.show()
```

<img width="1180" height="749" alt="image" src="https://github.com/user-attachments/assets/3a54d1ea-6430-43f6-add1-77a642f19ec7" />

```
#Histogram
plt.hist(df['Marks'], bins=5, edgecolor='black',rwidth=0.9, color='brown', alpha=0.8)
plt.xlabel('Marks',color='red')
plt.ylabel('Frequency',color='red')
plt.title('Histogram - Frequency of Marks', color='violet')
plt.show()
```

<img width="1317" height="654" alt="image" src="https://github.com/user-attachments/assets/676ca34a-e3e3-4c02-a901-b1a9d6784ded" />

```
#Pie Chart
data={
    'Months': ['Jan-Apr','May-Jul','Aug-Oct','Nov-Dec'],
    'Sales': [26,18,24,16]
}
df=pd.DataFrame(data)

plt.pie(df['Sales'],labels=df['Months'],shadow=True, colors=['lightcoral', 'skyblue', 'yellowgreen', 'orange'], explode=(0.1,0,0,0), autopct='%1.1f%%', startangle=90,counterclock=False)
plt.title('Quarterly Sales Report', color='purple', fontsize=18)
plt.show()
```

<img width="1313" height="710" alt="image" src="https://github.com/user-attachments/assets/17d7ee88-b7bc-4d27-affc-baf3d5a1e320" />

```
#Area Chart
Months = ['Jan', 'March', 'June', 'September', 'December']
Leaves = [12, 23, 14, 15, 10]

plt.fill_between(Months, Leaves, color='orange', alpha=0.8)
plt.plot(Months, Leaves, color='red', linewidth=2.2)
plt.xlabel('Months')
plt.ylabel('No.of Leaves')
plt.title('Leave Analysis')
plt.show()
```

<img width="1341" height="740" alt="image" src="https://github.com/user-attachments/assets/052b2935-3893-474b-abd5-eb0a23d50b5e" />

# Result:
Hence, different visualisation tools have been used form Matplotlib and the program is successfully executed.

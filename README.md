# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.

### PROGRAM:
```
DEVELOPED BY:S.BARATH
REGISTER NUMBER:212224240022
```
```py
from matplotlib import pyplot as plt
import pandas as pd

df=pd.read_csv("/content/test.csv")

df.head()

df['Month']=pd.to_datetime(df['Month'])


df.dtypes

df.set_index('Month',inplace=True)

df_resampled = df['#Passengers'].resample('D').interpolate()
df_resampled.plot(kind='line',label='Total Sales', color='black')
plt.title('Time Series Plot of Number of passengers ecah day')
plt.xlabel('Day')
plt.ylabel('Number of passengers')
plt.legend()
plt.grid(True)
plt.show()
```


### OUTPUT:
![735fa0f2-5e44-40f3-9758-f10d914525e2](https://github.com/user-attachments/assets/81c242ab-6d5d-4549-bfc6-8cf81a683083)







# RESULT:
Thus we have created the python code for plotting the time series of given data.

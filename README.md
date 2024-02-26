# <p align="center">Ex.No: 01 PLOT A TIME SERIES DATA</p>
###  Date: 

### AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
### ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
### PROGRAM:

### Population:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
### Market Price:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
### Temperature:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```

### OUTPUT:
### Population:
![Screenshot 2024-02-26 215148](https://github.com/Vishwarathinam/TSA_EXP1/assets/95266350/912dd43e-895d-45ae-a794-3c1b1611060c)

### Market Price:
![Screenshot 2024-02-26 215136](https://github.com/Vishwarathinam/TSA_EXP1/assets/95266350/cba29aa9-c02e-4ea1-8b2d-dd6a62c62c76)

### Temperature:
![Screenshot 2024-02-26 215102](https://github.com/Vishwarathinam/TSA_EXP1/assets/95266350/1214813a-6875-41c0-9a64-7a5cd75392f9)

### RESULT:
Thus we have created the python code for plotting the time series of given data.

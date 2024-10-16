# Ex.No: 08     MOVINTG AVERAGE MODEL AND EXPONENTIAL SMOOTHING

REG NO: 212222240057

NAME :  Mahalakshmi k

### Date: 

### AIM:

To implement Moving Average Model and Exponential smoothing Using Python.

### ALGORITHM:

1. Import necessary libraries

2. Read the electricity time series data from a CSV file,Display the shape and the first 20 rows of
the dataset

3. Set the figure size for plots

4. Suppress warnings

5. Plot the first 50 values of the 'Value' column

6. Perform rolling average transformation with a window size of 5

7. Display the first 10 values of the rolling mean

8. Perform rolling average transformation with a window size of 10

9. Create a new figure for plotting,Plot the original data and fitted value

10. Show the plot

11. Also perform exponential smoothing and plot the graph

### PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

# Sample data creation for demonstration
data = {
    'Date': pd.date_range(start='2020-01-01', periods=100, freq='D'),
    'Cases': [10, 15, 20, 30, 50, 70, 100, 150, 200, 250] * 10
}
df = pd.DataFrame(data)
df.set_index('Date', inplace=True)

# Define the window size for the moving average
window_size = 7  # 7-day moving average

# Calculate the moving average
df['Moving_Average'] = df['Cases'].rolling(window=window_size).mean()

# Plotting the results
plt.figure(figsize=(14, 7))
plt.plot(df['Cases'], label='Actual Cases', color='blue')
plt.plot(df['Moving_Average'], label='7-Day Moving Average', color='orange')
plt.title('COVID-19 Cases with Moving Average')
plt.xlabel('Date')
plt.ylabel('Number of Cases')
plt.legend()
plt.grid()
plt.show()
```
### OUTPUT:


![covid](https://github.com/user-attachments/assets/38128ef0-1cd5-4181-a1d1-037adcc2c303)


### RESULT:
Thus we have successfully implemented the Moving Average Model and Exponential smoothing using python.

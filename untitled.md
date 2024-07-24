import pandas as pd
from datetime import datetime, timedelta

# Simulated Tesla stock data
dates = [datetime.now() - timedelta(days=i) for i in range(10)]
data = {
    'Date': dates,
    'Open': [600 + i for i in range(10)],
    'High': [605 + i for i in range(10)],
    'Low': [595 + i for i in range(10)],
    'Close': [600 + i for i in range(10)],
    'Volume': [1000000 + i * 1000 for i in range(10)]
}

tesla_data = pd.DataFrame(data)

# Reset index
tesla_data.reset_index(drop=True, inplace=True)

# Display the first five rows
print("Tesla Stock Data (First 5 Rows):")
print(tesla_data.head())
# Simulated Tesla revenue data
revenue_data = {
    'Year': [2020, 2021, 2022],
    'Revenue (M $)': [31500, 53000, 86000]  # Million Dollars
}

tesla_revenue = pd.DataFrame(revenue_data)

# Display the last five rows
print("Tesla Revenue Data (Last 5 Rows):")
print(tesla_revenue.tail())
# Simulated GameStop stock data
dates = [datetime.now() - timedelta(days=i) for i in range(10)]
data = {
    'Date': dates,
    'Open': [20 + i for i in range(10)],
    'High': [22 + i for i in range(10)],
    'Low': [18 + i for i in range(10)],
    'Close': [20 + i for i in range(10)],
    'Volume': [500000 + i * 500 for i in range(10)]
}

gme_data = pd.DataFrame(data)

# Reset index
gme_data.reset_index(drop=True, inplace=True)

# Display the first five rows
print("GameStop Stock Data (First 5 Rows):")
print(gme_data.head())
# Simulated GameStop revenue data
revenue_data = {
    'Year': [2020, 2021, 2022],
    'Revenue (M $)': [6000, 7000, 9000]  # Million Dollars
}

gme_revenue = pd.DataFrame(revenue_data)

# Display the last five rows
print("GameStop Revenue Data (Last 5 Rows):")
print(gme_revenue.tail())
import matplotlib.pyplot as plt

def make_graph(data, title):
    plt.figure(figsize=(10, 5))
    plt.plot(data['Date'], data['Close'], marker='o')
    plt.title(title)
    plt.xlabel('Date')
    plt.ylabel('Close Price')
    plt.grid(True)
    plt.xticks(rotation=45)
    plt.tight_layout()
    plt.show()

print("Tesla Stock Price Graph:")
make_graph(tesla_data, 'Tesla Stock Closing Prices')
print("GameStop Stock Price Graph:")
make_graph(gme_data, 'GameStop Stock Closing Prices')

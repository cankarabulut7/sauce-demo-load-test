# SauceDemo Load Test with Apache JMeter

This project contains a **JMeter performance/load test** for the [SauceDemo](https://www.saucedemo.com) website.  
The test simulates a realistic user scenario from login to cart interaction and measures the system's performance under load.

## 🔍 Test Scenario

Each virtual user performs the following steps:

1. **Login** using credentials from a CSV file  
2. **Add an item to cart**
3. **Navigate to the shopping cart**
4. **Remove the item**

## 🧪 Test Configuration

- **Tool:** Apache JMeter  
- **Number of Threads (Users):** 300  
- **Ramp-up Period:** 120 seconds  
- **Loop Count:** 1 (each user runs the scenario once)
- **Data Source:** User credentials loaded from `users.csv`

### Ramp-up Explanation

- 300 users are started over a period of 120 seconds.
- That means one user is started every `0.4` seconds (300 / 120).

## 🔌 Required Plugins

- To run this test plan properly, the following JMeter plugins are required:
  **JMeter Plugins Manager**,
  **WebDriver Sampler**

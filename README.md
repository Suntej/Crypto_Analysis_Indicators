# Crypto_Analysis_Indicators
A set of tools to indicate cryptocurrencies which can be bought or sold using technical indicators such as StocH RSI , Moving averages,Boolinger Bands and other technical indicators


For each time frame
Minute / Hour / Daily I need to store data in a different table. CSV for now
You need to download historical data only once. - This is already working in examples.py file. The data is being written to CSV file. Need to store it in database. CSV for now

Highest Priority Requirement - After that we will download only the previous day/hour/minute data.(For this check out the historical functions only in cryptocompare_maverick.py file. The start and end time parameter values only will change) - This thing needs to run periodically. (For example after every 24 hours,I will download previous 1 day data, after every 1 hour I will download previous 1 hour data, After every 5 minutes I will download previous 5 minute data). 

After every download of different time-frames all data analysis and technical indicators calculation will also be automated.

Keep the code flexible enough so that If need be a table  CSV can be created with a new time-frame.
I need to calculate different statistical parameters for all the time-frames. For example Mean,Standard Deviation,Correlation,Co-Variance ,etc.
Further I will also experiment with different machine learning models and try to fit the data in them.
I need code to be modular enough with proper Object oriented programming.


I need an function interface where I can read data from the CSV file by passing 
Coin Symbol 
Number of rows in excel starting from latest time unit
Time unit which is either minute/hour/day 
 and get data in the following format
{
    'open': list of open prices of that coin symbol,
    'High': Same as above,
    'Low': Same as above ,
    'close': Same as above,
    'volume': Same as above. This is the volumeTo column in excel.
}
Example - getOHLCVData(Coin Symbol,30,Day) returns a latest 30 Day 1-Day data of that coin.





Also I plan to integrate notifiers into this app after a basic analytics framework is built.
For notifier check this out https://github.com/AbenezerMamo/crypto-signal/tree/master/app/notifiers

Use API data from Coinmetrics.io , store it in a database and then analyse it with cryptocurrency price together.


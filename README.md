# Stock Market Analysis (VBA)
## Overview of Project
The aim of this project is to provide basic quantitative metrics (volume and the year returns for the FYE 2017 and 2018) to help making an investment decision for a selected list of green energy stocks.

## Code Source Analysis
### Time execution analysis
Using images and examples of your code, compare the stock performance between 2017 and 2018, as well as the execution times of the original script and the refactored script.

### Pros and cons of refactoring code

#### Original Source Code
For the original source code, the pros was the simplicity to understand the operations. At first, the variable i the the number of the ticker from the selected array then the code will loop accross the data sheet for a the selected year and will aggregate the volume and fill the starting date and ending date. 

The cons are the time responsiveness at 0.52 on average and the loop is done 12 times in order to fill the 12 tickers. 

#### Refactoring Source Code
For the original source code, the pros are the speed to aggregate the data for the 12 tickers. The code uses an array with a tickerIndex that scan the selected year and store the volume, start price and ending price of the selected period on the first execution. By aggregation all the information for the 12 tickers once, we confirm a time execution of 0.10 in average which is 0.4 quicker than the original. (See below)

![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png?raw=true)
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png?raw=true)

The cons are if the analyst wants to add a 13th ticker, he may enconter a complexity in editing the code since they are many array to edit. Also, it is important to have the raw data filtered by ticker otherwise the refactored code won't generate the correct starting and ending price.

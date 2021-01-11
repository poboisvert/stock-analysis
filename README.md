# Stock Market Analysis (VBA Module)
## Overview of Project
The aim of this project is to provide quantitative metrics (volume and returns (LTM) for the FYE 2017 and 2018) to help making an investment decision for a selected list of green energy stocks. The results indicate a high volatity for the green energy industry with return of more than 199% in 2017 and a decrease of -62.6% in 2018.

## Stock Performance Analysis
### Performance Analysis of FYE 2017
Steve base his decision mostly on historical returns and judgment (her parent's opinion). Based on the figure 1, all stocks seems to have a steady liquidity with a large volume of shares traded (over 100MM+). The conclusions for the selected year are (1) investors were able to get a higher valuation of their shares with an increase of 67% on average for the last twelve months (LTM) and (2) based on the volume the investors are forcasting an increase in revenues.

### Performance Analysis of FYE 2018
In 2018, all stocks seems to have a steady liquidity with a large volume of shares traded. Based on the figure 2, DQ (favorite of Steve's parent) return the lowest with a FYE performance of -62.6%. The conclusions for this year are (1) investors lost -102% on average of what the price of their share was at the closing day of 2017 and (2) this industry offer a high volatility that may not be a fit for steve's parents.

### Conclusion of the returns
Based on 2017 and 2018, the tickers ENPH and RUN are making profits for their investors in both year. Based on historical results and volumes, these two could be a better choice comparing to the favorite (DQ). TERP is considered the worst performer in that category with only negative returns (-7.2% for FYE 2017 and -5.0% for FYE 2018). 

## Code Source & Time execution analysis

##### Figure 1: Time execution and 12 stocks performance (2017)
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png?raw=true)
##### Figure 2: Time execution and 12 stocks performance (2018)
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png?raw=true)

### Pros and cons of refactoring code

#### Original Source Code
For the original source code, the pros are the simplicity to understand all the steps and the speed to modify the source code. At first, the variable "i" selects the number of the ticker from the selected array and will loop accross the sheet for a the selected year in order to aggregate the volume and generate a starting date and ending date value. 

The cons are the time responsiveness at 0.52s on average, and it will loop 12 times in order to fill the 12 tickers. The design pattern could be improve since some functions are duplicated.

#### Refactoring Source Code
For the original source code, the pros are the speed to aggregate the data for the 12 tickers. The code uses an array with a tickerIndex that scan the selected year and store the volume, start price and ending price of the selected period on the first execution. By aggregation all the information for the 12 tickers once, we confirm a time execution of 0.10s on average (Figure 1 & 2) which is 0.4s quicker than the original. The last pros would be it offer the capacity to gather and analyse more data since the run time is less and the CPU utilization is lower.

The cons are if the analyst wants to add a 13th ticker, he may enconter a complexity in editing the code since they are many array to edit. Also, it is important to have the raw data filtered by ticker otherwise the refactored code won't generate the correct starting and ending price. Lastly, the code doesn't include an error message if we have a ticker in the raw data that is not included in the array.

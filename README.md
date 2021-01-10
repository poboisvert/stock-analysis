# Stock Market Analysis (VBA Module)
## Overview of Project
The aim of this project is to provide quantitative metrics (volume and returns (LTM) for the FYE 2017 and 2018) to help making an investment decision for a selected list of green energy stocks. The results indicate a high volatity for the green energy industry with return of more than 199% in 2017 and a decrease of -62.6% in 2018.

## Stock Performance Analysis
### Performance Analysis of FYE 2017
Steve base his decision mostly on historical returns and trend (her parent's opinion). Based on the figure 1 all stocks seems to have a steady liquidity with a large volume of shares traded. The conclusion for this year are (1) investors were able to get a higher valuation of their shares with an increase of 67% on average for the last twelve months (LTM).

### Performance Analysis of FYE 2018
In 2018, all stocks seems to have a steady liquidity with a large volume of shares traded. Based on the figure 2, DQ (favorite of Steve's parent) return the lowest with -62.6%. The conclusion for this year are (1) investors lost of -102% on average of what the price of their share was at the closing day of 2017 and this industry offer a high volatility that may not be a fit for steve's parents.

### Conclusion of the returns
Base on 2017 and 2018, the comanies ENPH and RUN, are making profits for their investor in both year. Based on historical results and volumes, these two could be a better choice comparing to the favorite (DQ). TERP is considered the worst performer in that category with only negative return of -7.2% for FYE 2017 and -5.0% for FYE 2018. 

## Code Source & Time execution analysis

##### Figure 1: Time execution and 12 stocks performance for 2017
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png?raw=true)
##### Figure 2: Time execution and 12 stocks performance for 2017
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png?raw=true)

### Pros and cons of refactoring code

#### Original Source Code
For the original source code, the pros was the simplicity to understand the operations. At first, the variable i the the number of the ticker from the selected array then the code will loop accross the data sheet for a the selected year and will aggregate the volume and fill the starting date and ending date. 

The cons are the time responsiveness at 0.52 on average and the loop is done 12 times in order to fill the 12 tickers and the design pattern to create a code once could be improve since many parts are repetitive.

#### Refactoring Source Code
For the original source code, the pros are the speed to aggregate the data for the 12 tickers. The code uses an array with a tickerIndex that scan the selected year and store the volume, start price and ending price of the selected period on the first execution. By aggregation all the information for the 12 tickers once, we confirm a time execution of 0.10 on average (Figure 1 & 2) which is 0.4 quicker than the original. (See below)

The cons are if the analyst wants to add a 13th ticker, he may enconter a complexity in editing the code since they are many array to edit. Also, it is important to have the raw data filtered by ticker otherwise the refactored code won't generate the correct starting and ending price.

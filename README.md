# Stock Market Analysis (VBA)
## Overview of Project
The aim of this project is to provide basic quantitative metrics (volume and the year returns for the FYE 2017 and 2018) to help making an investment decision.

## Code Source Analysis
### Time execution analysis
Using images and examples of your code, compare the stock performance between 2017 and 2018, as well as the execution times of the original script and the refactored script.
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png?raw=true)
![alt text](https://github.com/poboisvert/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png?raw=true)

### Pros and cons of refactoring code

#### Original Source Code
For the original source code, the pros was the simplicity to understand the operations. At first, the variable i the the number of the ticker from the selected array then the code will loop accross the data sheet for a the selected year and will aggregate the volume and fill the starting date and ending date. The cons are the time responsiveness at 0.52 on average and the loop is done 12 times in order to fill the 12 tickers. 

#### Refactoring Source Code



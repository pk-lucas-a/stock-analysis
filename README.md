# Automation of Analysis of Stock Data
Automated analysis of 12 stocks to uncover annual trends for investment research.

## Overview of Project

### Purpose
Investors have selected stock DQ without any research. A dataset of daily stock outcomes over 2 years was collected for this stock and 11 others. The stock dataset is summarized by total daily volume and annual percent of return for either of the two years to uncover insights before the final investment decision. 


## Results of Stock Analysis

### Stock Performance Comparison
Overall, stocks had a much higher return in 2017 than 2018. All stocks except RUN and ENPH had negative returns in 2018. DQ performed the best in 2017 at a near 200% return, but had a -63% return the following year. This high level of variability highlights the need for longer and more detailed trend analysis. Future stock performance cannot be known with complete certainty, and the negative returns should be used to illustrate the risk involved in limiting investment to a single stock. 

![stock-analysis](Resources/VBA_2017_Performance.png) ![stock-analysis](Resources/VBA_2018_Performance.png)


### Code Performance Comparison
Execution times before refactoring the code were near 0.9 seconds. After refactoring the execution times were lowered to about 0.145 seconds. In other words, running the orignial code takes about 6 times longer than the refactored execution. 

![stock-analysis](Resources/VBA_Challenge_2017.png) ![stock-analysis](Resources/VBA_Challenge_2018.png)


## Summary of Methods

### Pros and Cons of Refactoring in General
The main disadvantage of refactoring code is the time and effort it takes. The process also presents a risk of introducing bugs or errors. 
The advantages of refactoring are that the code becomes faster, more extensible to different situations, and more easily maintainable. Reorganizing the code makes it cleaner and more understandable to other coders. 

### Consequences of Refactoring this VBA
In this case, arrays were created with an index variable. Because the tickers were ordered in groups together, the index could be increased when the last stock ticker was observed so that the For loop only loops once instead of searching all rows for a specific ticker over each of 12 loops. This made the code execute much faster. The code is better organized and so it would be easier to maintain or adjust. However we are still limited to the same 12 stocks in the future, so it is not very extensible. The process took some time and debugging to come to the same output, saving us just 0.76 seconds per run. Our code isn't very long. A longer code would benefit more from refactoring for execution speed. 

### Limitations and Further Analysis
We should look deeper into the trends of each stock over a longer period so we can identify patterns and test forecasting models before making our decision.


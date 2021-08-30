# Stock Analysis

## Project Overview
The objective of this stock analyis was to refactor, or improve, the existing code to improve Steven's analysis time.
Steven currently has working code, however the current state of the script may not be effective if he wishes to expand the number of stocks.
It could also potentially take longer if he is dealing with a larger volume of data.

## Results
The new and improved refactored code allows Steven to expand the number of stocks he may want to analyze.
Additionally the code runs faster as it takes advantage of array indexing rather than a fixed input.

When running the old code, it took [0.3125 seconds](Resources/2017_Initial_Code.png) to complete the analysis for 12 stocks for both 2017 and 2018.
When running the refactored code, it took [0.28125 seconds](Resources/2017_Refactored_Code.png) to complete the analysis for the same stocks for both 2017 and 2018.
This is a notable 11% increase. This [screenshot](Resources/Old_vs_Refactored_Runtimes.png) illustrates the difference.

The improvement was due to being able to count and index the tickers.
The first ["For" loop](Resources/For_Loop_Init.png) was made to index and store data for each ticker that was initialized. 
This change to the code also allowed me to skip the ["increase the tickerIndex"](Resources/tickerIndex.png) instruction '3d'. 
Since the initial "For" loop included the tickerIndex, there was no reason to increase it at the end of the loop after analyzing the starting & ending prices.
Using ``` Next tickerIndex ``` meant that we did not need to manually increase the tickerIndex via ```tickerIndex = tickerIndex + 1```


## Summary

Overall, the refactored code is a bit more complex, however it has more advantages than disadvantages.
Below illustrates both the advantages and disadvantages of the refactored code.

### Advantages
* The code runs faster when it is refactored
* The code does not rely on a fixed user input of stocks to analyze (# of tickers). This allows the Steven to analyze as many stocks as he'd like.
* The code can be expanded to a much larger data set due to the use of array indexing

### Disadvantages
* The code is slightly more complex in order to include array indexing for # of tickers

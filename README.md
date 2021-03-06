# Stock-Analysis
## Overview of Project
The purpose of this analysis is to help Steve analyze the performance stocks that promote green energy. We will be looking at data from twelve different green energy stocks over the course of 2017 and 2018, using VBA code to extract data points of interest, such as total volume and yearly return. We will be specifically looking at the performance of the DQ stock (Daqo New Energy Corp) at Steve's request.
## Results
### Stock Performance 2017
For 2017, we can see from our table that all of our green energy stocks had a positive return with the exception of TERP (-7.2%).
<p align="center"

![alttext](https://github.com/sd2wiebe/Stock-Analysis/blob/main/Resources/2017_performance.png)

</p>
We can observe that the average return on this portfolio of stocks is 67.3%, so it is safe to say that these green energy stocks did very well in 2017. Our stock of interest, DQ, saw a return of 199.4%, topping the list. 

### Stock Performance 2018
For 2018, it was quite a different story for our green energy stocks. As we can see in our table, there were only two out twelve of our stocks that had a positive return (albeit those stocks did do very well, ENPH and RUN observed a 81.9% and 84% return respectively).
<p align="center"

![alttext](https://github.com/sd2wiebe/Stock-Analysis/blob/main/Resources/2018_Performance.png)
</p>
The average return for 2018 across all of our stocks was a tough -8.5%. It was a particularly tough year for DQ, with a deprecated return of -62.6%. 

### Code performance
In order to measure code performance, I used a code that measured the time it takes to execute the code by putting
```startTime = Timer ``` at the start of the VBA code, and ```endtime = Timer ``` at the end. Then in order to display the runtime I used a ```MsgBox``` and displayed ```endTime - startTime```. Initially the code I had used to create the summary tables for [2017](https://github.com/sd2wiebe/Stock-Analysis/blob/main/Resources/VBA_Challenge_initial_code_2017.png) and [2018](https://github.com/sd2wiebe/Stock-Analysis/blob/main/Resources/VBA_Challenge_initial_code_2018.png) had a runtime of over 2 seconds each. 
After refactoring the code to loop through the data only once, I saw a more efficient performance, with both codes for [2017](https://github.com/sd2wiebe/Stock-Analysis/blob/main/Resources/VBA_Challenge_2017.png) and [2018](https://github.com/sd2wiebe/Stock-Analysis/blob/main/Resources/VBA_Challenge_2018.png) running in less than .4 seconds. In order to achieve this substantially more efficient code, I utilized multiple arrays. Each array stored values for total volume, opening price, and closing price respectively. This way we only had to loop through the data once, and then output the values stored in the arrays for each stock.

## Results
### DQ Stock
After reviewing the analysis of DQ's performance over 2017-2018, we can safely conclude that it does not look like the best green energy stock to invest in at this point. DQ showed a substantial return in 2017, however since then its been trending negatively, with a -62.6% return over 2018.
### Refactored code
There are numerous benefits to refactoring code. A code can be refactored to be more easily understood, and thus easier to debug, or to make modifications to upon revisiting. A well designed code will also be easier to maintain and enhance. When the code design is improved, it can make the program run more efficiently as well.
Some disadvantages to refactoring code includes the time investment. Sometimes it might be easier to re-write a more efficient, well designed code from scratch, rather than spend an exorbitant amount of time trying to refactor existing code. Another factor that might make you rethink refactoring a code would be cost associated.

### Refactored Stocks-Analysis code
The main advantage of the first Stock-Analysis VBA code was the simple design. For this code, I used a nested loop to simply and accurately produce the correct outputs. However it was clear among revisiting the code that there was a more eloquent and efficient design that could be used. I found the refactored code much easier to debug, as it was easier to read the code top to bottom and see where the problem was occuring. Another big advantage to the refactored code is that it would be very easy to add enhancements later. If you wanted to add more columns to the excel output, you could simply implement another array and block of code to store and output that data. 




# Bootcamp-Project-1
## Project 1 – Can you beat the market?
- Vidhi Mehta
- Justin Tran
- Dmytro Denysenko
## FinTech Bootcamp
October 3rd 2022
## installation instructions
-you need to $ pip install yahoo-finance
-you need to modify the path for the .csv file
### Motivation & Summary Slide
80% of fund managers are not able to beat the market, but can we beat the market?
Hypothesis : Team member Justin believed we can beat the stock market, Vidhi and Dmytro did not believe we can.
If we can find the answer, then we can know whether or not to invest the index funds or pick individual stocks.
Summary: all high beta stock portfolios beat both the Nasdaq 100 and S&P 500 index
One low beta stock portfolio beat high beta stock portfolio – Tesla
Having a high beta 10 years ago doesn’t correlate with having a high beta now
## List of Questions Asked
- Can you beat the stock market ”Index Fund”?
- Should you use beta as an indicator to beat the stock market?
- Does having a high beta today predicts if a stock has a high beta in the future?
- Does being a bear market or bull market affect whether you should use beta as an indicator?
- Does high beta change 3 months after a crash (September 2008 to December 2008)? 
- Does low beta change 3 moths after a crash (September 2008 to December 2008)?
## Reasons why the questions were asked:
- To earn more money
- To invest in an index fund or individual stock
- To know if beta is an effective indicator to pick stocks
- To know if beta is a consistent indicator to pick stocks
- To know if beta changes in a bear or bull market
- To know if beta changes from right after a crash to a recovery
## Questions & Data:
- What data do we need & where can we find it?
- We need stock betas and prices from 2008 (bear market), 2012 (bull market) and 2022 (present)
- We can get it from David
- We also need data from the crash i.e., September 2008 and a good amount of time after i.e., December 2008
## Data Cleanup
# Clean up process:
- Change the excel file to a .csv file because pandas doesn’t accept an excel file
- Set the index to tickers for easier visualization
- Drop the NaN where necessary
- Create 6 different data frames from the csv file to easily visualize the data
- Separate the information received from Yahoo Finance API into 3 years – 2008, 2012 and 2022. Each year is separated into high beta stocks and low beta stocks
## Exploration
- Find if there is a correlation between a stock’s beta 10 years ago and its beta today
- Find if the portfolios of high beta stocks beats QQQ (Nasdaq 100) and SPY (S&P 500)
- Find if the portfolios of low beta stocks loses to QQQ (Nasdaq 100) and SPY (S&P 500)
- Find if the results are different between 2012 (bull market) and 2008 (bear market)
- Find if the high beta stocks in September 2008 are similar or different to high beta stocks in December 2008 
- Find if the low beta stocks in September 2008 are similar or different to low beta stocks in December 2008
- Problems that we encountered
- Pandas does not work with excel
- A lot of NaN in 2008 that needed to be dropped in order to sort betas
- Alpaca does not have data from 2008 and 2012, so we had to use Yahoo Finance
## Steps taken for Data Analysis
- Use the correlation method to find the correlation between 2012 and 2022 betas:
betas_df[[“Beta 09/2012”,“Beta 09/2022"]].corr(method=‘pearson’)
- Compare returns of high beta stock portfolios to SPY and QQQ
- Compare returns of low beta stock portfolios to SPY and QQQ
- Compare the results from 2008 portfolios and 2012 portfolios
- Compare the high beta stocks in September 2008 and December 2008
- Compare the low beta stocks in September 2008 and December 2008
## Interesting findings
- These figures suggest that high beta stocks beats the market overtime and market beats low beta stocks overtime
- Low beta portfolio with Tesla beat the market and the high beta portfolio
- There is no strong correlation between past beta and current beta
## Expectations
- Justin : High beta would beat the market and market would beat low beta stocks
- Vidhi and Dmytro : Market would beat the high beta stock portfolios 
- Justin expected that a stock’s beta from 10 years ago will remain similar to its beta today
- Justin expected that high beta stock portfolio of 2008 would be similar to high beta stock portfolio of 2012
- Justin expected high beta stocks to outperform the market regardless of if the stocks were bought in bear or bull market 
- Justin expected that high beta stocks would be different right after a crash compared to a good amount of time after the crash
## Results
- According to the correlation analysis there is a relatively strong correlation between a stock’s beta from 10 years ago to its beta today
- The betas of many stocks changed by an amount that was unexpected by Justin
- Portfolio for 2008 was very different than 2012
- High beta stocks beat the market regardless of if they were bought in a bear or bull market
- The list of high beta stocks and low beta stocks were very similar right after the crash compared to good amount of time after the crash
## Postmortem
- No new difficulties arose after the analysis
## Additional Questions if there was extra time: 
- Does same pattern exist 10 years from now or 20 years from now?
- Why was Tesla such an outlier?
- If we can predict Tesla type outlier, find them early?
- Look at all outliers such as Tesla and see if we can find a commonality?
- Does high beta stocks from 20 or 30 years ago outperform the market?

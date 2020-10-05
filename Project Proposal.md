# The Relationship between TED spread and volatility
## Background

In finance, the TED spread is the difference between the three-month Treasury bill and the three-month LIBOR (London Interbank Offer Rate) based in US dollars. 
To put it another way, the TED spread is the difference between the interest rate on short-term US government debt and the interest rate on interbank loans. The formula of TED spread follow:   
$$TED spread = 3Month LIBOR rate – 3Month Treasury rate$$.   
Generally treasury rate and LIBOR rate are very similar, as they have very similar nature (short-term borrowings with low default probability and high liquidity). 
And in principal the only difference is the small default risk of large banks, as US government is widely considered to have no default risk. When the banks are more likely to default, for example, in financial crisis, the spread will increase. 
And the market instability, which could be illustrated using stock volatility, should have an impact to the credit risk of these banks. 
Thus we are interested in building a predictive model of the TED spread using stock index volatility, and researching on their statistical relationship.
## Significance
Interest rate fluctuation is a critical topic in finance, as it indicates the change of risk and required return embedded in the economic activities. 
There are many factors impacting the interest rate including economic growth, market conditions, credit risk of loan-issuers, liquidity of loans, investors’ risk preference. 
Thus it is difficult to research on the influence of a single factor to interest rate. 
By examining the relationship between the stock index volatility and the TED spread, it actually isolate other major factors and primarily focus on the impact from market instability to credit risk, which may contribute to further research on interest risk modeling.    
## Research Questions
### 1.	How the stock market volatility (Russell 3000 index) impact the TED spread.
> In principal, the stock market volatility should have impact on the TED spread. 
And we plan to use statistical learning models like autoregression to explore the relationship between TED spread and the Russell 3000 index which is a market index across 30 years’ history.
### 2.	Can we predict TED spread using stock market volatility (Ressull 3000 index)
> In particular, we will try to build a machine learning or deep learning based time-series model to predict the TED spread using Russell 3000 index volatility. 
And we will conduct 30 years’ back test on the prediction precision to explore the predictive power of the Ressull 3000 index.
### 3.	* (if time allowed) In which part of the equity market volatility (small, middle or large companies) have the biggest impact on TED spread
> If time allowed, we will further decompose the market volatility into its three components: large-cap, mid-cap and small cap companies. 
And we will use machine learning techniques to analyze their relative importance of impact to TED spread.
## Data
In general, we are going to use 30-years historical monthly data to research on these questions. 
And the back-testing time period include most market conditions (2008 financial crisis, Covid market drop). 
And the data source is https://finance.yahoo.com
### 1.	Ressell 3000 index (^RUA) volatility
> https://finance.yahoo.com/quote/^RUA?p=^RUA&.tsrc=fin-srch.   
Ressell 3000 encompasses 3000 listed stocks in US, which is a commonly used index representing the overall US equity market. The index volatility is calculated as the standard deviation of daily return in a month.
### 2.	S&P 500 large cap (^GSPC) index volatility.  
> https://finance.yahoo.com/quote/^GSPC?p=^GSPC&.tsrc=fin-srch.   
S&P 500 included 500 largest listed companies in US in terms of capitalization size. The index volatility is calculated as the standard deviation of daily return in a month.
### 3. S&P 400 mid cap index (^SP400) volatility
> https://finance.yahoo.com/quote/^SP400?p=^SP400&.tsrc=fin-srch.   
S&P 400 includes 400 mid-size listed companies in US after S&P 500. 
The index volatility is calculated as the standard deviation of daily return in a month.
### 4.	S&P 600 small cap index (^SML) volatility
> https://finance.yahoo.com/quote/^SML?p=^SML&.tsrc=fin-srch.   
S&P 600 includes 600 small-size listed companies in US after S&P 600. The index volatility is calculated as the standard deviation of daily return in a month.


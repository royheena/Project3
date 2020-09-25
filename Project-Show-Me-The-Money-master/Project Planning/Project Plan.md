	- Objective
		○ Provide custom data analysis based on input portfolio.  Analysis includes:
			§ YTD performance
			§ Performance over time (1Yr, 5Yr, etc)
			§ Cost basis
			§ Overall Gain/lose
			§ Comparison to S&P, input ticker
				□ Based on Sharpe Ratio
		○ Dashboard
			§ Pie Chart
				□ Current Industry
				□ Goal: Trends
			§ Performances compared to other portfolios
				□ Combined performance
				□ Beta
				□ P/E ratio
				□ Sharpe Ratio
				□ Profit Margin
				□ Cash
				□ Dividends
		○ Goal:
			§ Mean-variance optimization
            § Fama French regression analysis
            § efficiency frontier
		
	- API: Pull Stock
		○ Input:
			§ Ticker
			§ Date Range
		○ Output
			§ Daily Closing Price
			§ Current Beta
			§ Current P/E ratio
			§ Current Profit Margin
			§ Current Cash
			§ Dividends
			§ Industry type
      * Lead: Renae
      * Alpaca
      
	- Goal API/Function: mean-variance optimization
      * 

	- Input Portfolio:
		○ Ticker, Buy Date, Buy Price, # of shares
		○ Ticker, Sell Date, Sell Price, # of shares
       *  Format:
          ** Ticker
          ** Action (B, S)
          ** Date
          ** Transaction Price
          ** # of shares
		
	- Function: performance
		○ Input (1 portfolio): 
			§ DataFrame
                * input portfolio
                * data from API Pull Stock
                    * Format
                        ** Ticker
                        ** Daily close price          
		○ Output:
			§ Plot of performance for given date range
            § YTD performance
			§ Performance over time (1Yr, 5Yr, etc)
			§ Cost basis (per ticker)
			§ Overall Gain/lose (per ticker)
                * Balance = Current Market Price * Number of Shares
                * Cost of purchases = buy price 1 * # of shares 1 + buy price 2 * # of shares 2 + ... buy price n * # of shares n
                * Gain/Loss = balance - Cost of all purchase
			§ Comparison to S&P, input ticker
				□ Based on Sharpe Ratio
        * Lead: Alex
	
	- Function:  Industry Weights
		○ Input (1 portfolio)
			§ Dataframe
                * Columns
                ** Ticker
                ** shares per ticker
                ** Industry
			§ Goal: Specific Dates - input from dashboard
		○ Output
			§ Industry weight for portfolio
        * Lead: Heena
	
	- Function: Ticker Stats
		○ Input:
			§ Dataframe
			§ Goal: Specific Dates - input from dashboard
		○ Output
			§ Sliced dataframe with beta, P/E ratio, profit margin, cash, dividends
        * Lead: Renae
        
     - Dashboard
       * Lead: Heena
            
Resources:
- https://financialmodelingprep.com/developer/docs/
- https://towardsdatascience.com/efficient-frontier-portfolio-optimisation-in-python-e7844051e7f
- https://apidocs.advisorsoftware.com/?version=latest


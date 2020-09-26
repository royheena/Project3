- Simplify data entry

- Add user-interactive features for the efficient frontier
    - Add stock(s) inputs to given portfolio
        - one-time inputs vs monthly input
        - beginning weight percentage
        - Robo??? interactive dropdown
    - Output max sharpe ratio weights and portfolio sharpe ratio weights

- Predicitve Analysis / Algorithm Trading
    - calculate potential balance based on current portfolio mean/SD
    - trade decisions based on volatility of stock
    
    
    - volume of trades
    - Option trends
    - sentiment score
    

Next Steps
- Review Project1 code (MasterFinal_v2)
- Amrita/ Renae
    - Research AWS site
    - Get Project1 working on AWS
    - Get bare-bones Robo working
    - Add bells and whistles
- Jatinder/Heena
    - Simplify data entry
        - simplify stock data retrival (use different API)
        - convert into datafram (daily closing price per stock)
        - make code modular (so that any portfolio coudl be inputed)
        - correct S&P balance calculation
        - Add nasdaq


*************************
9/26

## Objective: 
1) User provides input portfolio file
2) Calculate portfolio performance
3) Display portfolio results
4) User provides optimization what-if inputs
5) Calculate what-if performance
6) Display what-if results
7) Repleat 4-6 

## Functions
1) input_portfolio - Jatinder
2) api_calls - Jatinder/Heena
3) industry_performance - Jatinder/Heena
4) portfolio_performance - Amrita
5) portfolio_stats - Heena
6) ticker_stats - Heena
7) efficient_frontier - Renae
8) dashboard - Heena
9) user_inputs - Renae
10) main - Jatinder

## input_portfolio Function
Read in the input portfolio CSV file and output a portfolio dataframe
* Inputs:
    * none
* User Solicited Inputs:
    * Portfolio CSV file
        * Format: Ticker, Transaction (B=buy, S=Sell), Date, Transaction Price, Number of Shares
        * Assumptions: Date unsorted, no '$' sign, no commas
* Outputs:
    * transaction_df
        * Format: Date, Ticker, Transaction (B=buy, S=Sell), Transaction Price, Number of Shares, Transaction Cost
        * Database sorted by ascending date
    
    
## api_calls Function
* Inputs: 
    * transaction_df (could be transaction_df or index_df)
* Output:
    * ticker_stats_df
    * ticker_stats_df_T
    * closing_df


## industry_performance Function
replace ticker buys with index buys - assumes user bought index instead of stocks
* Inputs:
    * index ticker (S&P, NASDAQ)
    * transaction_df
* Output
    * index_df (needs to be same format as transaction_df)
    
    
## portfolio_performance Function
* Input
    * transaction_df (could be transaction_df or index_df)
    * closing_df
* Output
    * database showing 
        * daily balance per ticker
        * daily returns per ticker
        * daily balance for portfolio
        * dailiy returns for portfolio

## portfolio_stats Function
* Inputs
    * ticker_stats_df
    * closing_df
* Output
    * holdings_df
    * sector_df
    * current_industry_holings
    * industry_holdings
    * sector_holdings
    
## ticker_stats Function
* Inputs
    * ticker_stats_df_T
* Output
    * stats_panel
    
## efficient_frontier Function
* Input
    * closing_df
* Output
    * best_sharpe
    * best_return   
    * best_weights
    * or dataframe
    * effecient_frontier plot
    
## dashboard Function
see code

## user_inputs Function
* Input
    * transaction_df
* User Solicited inputs
    * new ticker
    
* Output
    * revised transaction_df 


- questions
    * What is your risk tolerance? (low, medium, high)

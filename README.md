# Financial_Planning_Tool

This financial tool uses ALPAKA to download data from selected date range and calculate for future potential cumulative returns.

Part 1:
    Cryptocurrency Wallet:

        Assuming cutomer's monthly_income is $12,000.00, btc_coins in wallet = 1.2, eth_coins = 5.3

        Acquiring and shows data using 'json.dumps' function from btc_url and eth_url, then navigate the current price for both cryptocurrencies.

        Finally, calculate the current cryptocurrency wallet balance.

    Stock and Bond Holdings:
        
        Assuming customer's stock and bond holding cointains SPY 110 shares and AGG 200 shares.

        Acauiring data from ALPACA using ALPACA_API_KEY and ALPACA_SECRET_KEY in 
        .env file.

        Setting the tickers, timeframe, and start/end date to acquire data. Then shows the data via pandas DataFrame '.df' function

        Calculating both holdings' total price with their most recent close price.

    Emergency Fund:

        Creating a savings_df with customer's total_crypto_wallet and total_stocks_bonds.

        Plotting the total value of the customer's portfolio (crypto and stock/bond) in a pie chart.
        ![Alt text](/download.png)

        Calculating if customer's total_portfolio reach the emergency_fund_value, and print different statement according to the result.

Part 2:
    Create the Monte Carlo Simulation:
        Creating new DataFrame df_SPYAGG_portfolio with expanded start/end date up to 10 years

        Running the MCSimulation with 40% AGG and 60% SPY holding, 30-year forecast, 500 times simulation.

        Plotting the Monte Carlo Simulation result.
        ![Alt text](/MC_thirty_year_sim_plot.png)

        Plotting the Monte Carlo Simulation distribution result.
        ![Alt text](/MC_thirty_year_sim_dis_plot.png)

        Generating summary statistics from the 30-year Monte Carlo simulation results.

        Printing the final statement with 95% confidence intervals lower and higher returns range.


    Analyze the Retirement Portfolio Forecast:
        Assuming customer has 20% AGG 80% SPY, and needs 10-year forecast.

        Plotting the 10-year Monte Carlo simulation.
        ![Alt text](/MC_tenyear_sim_plot_line.png)

        Plotting the 10-year distribution result.
        ![Alt text](/MC_tenyear_sim_plot.png)

        Generating summary statistics from the 10-year Monte carlo simulation results.

        Printing the final statement with 95% confidence intervals lower and higher returns range.




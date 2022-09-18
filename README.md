# NextTrade

A system to create, test, optimize, and deploy algorithmic trading strategies

## Features
1. Combine simple conditions to form compound conditions. Combine compound conditions and create trading strategies. 
    - For example: 
        - Condition A: QQQ stock is 1 SD below its 5-day mean price 
        - Condition B: Buying power is above $8,000.
        - Condition C: Condition A and condition B
        - Strategy: If condition C, buy $3000 of SPY 
2. Create unlimited portfolios with different combinations of strategies
3. Backtest those strategies using historical data. 
    - Only stocks are currently supported, but cryptocurrency and options support is baked into the architecture
3. Optimize the strategy's parameters using a genetic algorithm
    - Choose hyperparameters like mutation rate, training period, validation period, and population size
    - Choose to optimize percent gain, sortino ratio, sharpe ratio, or max drawdown
4. Deploy the strategies live and see how it performs in real-time

## System Architecture and Design
Some architectural artifacts can be found at this link:
https://drive.google.com/drive/folders/1TgZNGPd7TBWi47dWh0TI2nZ_9WUhv_P_?usp=sharing

## Installation

1. Clone the repository.
2. [Download MongoDB community edition](https://docs.mongodb.com/manual/administration/install-community/). Turn on MongoDB. It is recommended that you turn it on in the background so that you can close the tab.
3. Open your IDE to the NextTrade folder. It is recommended to use VSCode, but you can use any IDE that you want. Open a terminal window within the IDE.
4. Install the dependencies: `npm run install-all`
5. Make sure all tests pass: `cd app; npm t`
6. Add secrets to the env file (in app folder) and rename the file to .env

## Turning on the system

To turn on the client and server:

1. Open two terminal windows.
2. In one window, turn on the client: `cd client; npm start`
3. In the other window, turn on the server: `cd app; npm start`

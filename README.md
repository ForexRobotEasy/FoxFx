# FoxFx Trading Robot

This code is a sample implementation of the FoxFx Trading Robot developed by the Forex Robot Easy Team. It is designed to perform grid trading with a profit-centric closing mechanism. 

## Description

The FoxFx Trading Robot utilizes various technical indicators such as RSI (Relative Strength Index), Bollinger Bands, and Double Stochastic to identify potential trading opportunities. It places buy and sell orders at specified grid levels based on the current market conditions.

### Grid Trading

The grid trading strategy involves placing orders at predetermined price levels, known as grid levels. In this code, the grid levels are calculated based on the current price and grid size. The robot places buy orders when the current price is above the upper Bollinger Band and the RSI is oversold, and sell orders when the current price is below the lower Bollinger Band and the RSI is overbought. 

### Profit-Centric Closing Mechanism

The robot also incorporates a profit-centric closing mechanism. It checks the profit of each open trade and, if it exceeds a specified threshold, sets a trailing stop loss to protect the profits. This allows the robot to lock in profits and maximize potential gains.

## Required Libraries and Indicators

The code requires the following libraries and indicators:
- Trade.mqh
- RSI.mqh
- BollingerBands.mqh
- DoubleStochastic.mqh

## Global Variables

The code defines the following global variables:
- `trade`: An instance of the CTrade class used for trading operations.
- `rsi`: An instance of the CRSI class used for RSI calculations.
- `bollingerBands`: An instance of the CBollingerBands class used for Bollinger Bands calculations.
- `doubleStochastic`: An instance of the CDoubleStochastic class used for Double Stochastic calculations.

## Initialization

The `OnInit()` function initializes the trading robot by setting up the parameters for the RSI, Bollinger Bands, and Double Stochastic indicators.

## Trading Logic

The `OnTick()` function is called on each tick and performs the following steps:
1. Checks if it's time to place a trade based on the grid interval.
2. Calculates the grid levels based on the current price.
3. Places buy orders at grid levels if the current price is above the upper Bollinger Band, the RSI is oversold, and the Double Stochastic is below the oversold level.
4. Places sell orders at grid levels if the current price is below the lower Bollinger Band, the RSI is overbought, and the Double Stochastic is above the overbought level.

## Profit-Centric Closing Mechanism

The code includes a profit-centric closing mechanism implemented in the `OnTick()` function. It checks the profit of each open trade and, if it exceeds the specified threshold, sets a trailing stop loss to protect the profits. This allows the robot to secure profits and minimize potential losses.

## Error Handling

The code includes an `OnTradeError()` function that handles trade errors and exceptions. It prints the error code to the console for debugging purposes.

## Input Data Validation

The `ValidateInputData()` function validates and sanitizes input data. However, the implementation of this function is not provided in the code. Users should implement their own input data validation logic.

## Logging and Debugging

The `LogDebugInfo()` function is used for logging and debugging purposes. However, the implementation of this function is not provided in the code. Users can customize this function to log relevant information for debugging purposes.

## User Interface

The `OnChartEvent()` function is a placeholder for handling user input and events related to the chart. Users can implement their own logic for handling user interactions.

## Documentation

The `GetDocumentation()` function returns a string containing the documentation for the FoxFx Trading Robot. However, the implementation of this function is not provided in the code. Users should refer to the official documentation or the Forex Robot Easy website for detailed information about the trading robot.

## Testing

The `TestCode()` function is a placeholder for performing code testing. Users can customize this function to test and validate the code implementation.

## Main Program Entry Point

The `start()` function is the main program entry point. It validates the input data, logs debug information, and starts the trading process by calling the `OnTick()` function.

**Note:** ForexRobotEasy is not the official developer of this product. This code is provided as a sample implementation that can work as described in the product. To find the official developer of this product, please refer to the MQL5 website.

For detailed reviews and trading results of this product, please visit the [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/foxfx-software-review-grid-trading-with-profit-centric-closing/) website.

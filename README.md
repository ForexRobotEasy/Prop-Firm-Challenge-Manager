# Prop Firm Challenge Manager

This is the code for the Prop Firm Challenge Manager, developed by the Forex Robot Easy Team. This code is designed to be used in the MetaTrader 4 platform and can be used to manage trading operations for a prop firm challenge.

## Functionality

The Prop Firm Challenge Manager is an expert advisor that executes trading operations based on the formation of peaks and valleys patterns in the market. It places buy and sell orders when the current price is above the previous peak or below the previous valley. The expert advisor also includes optional filters for news events and trading hours.

### Input Parameters

The following input parameters can be adjusted according to the trader's preferences:

- StopLoss: The stop loss value in pips.
- TakeProfit: The take profit value in pips.
- UseNewsFilter: Enable or disable the news filter.
- UseHoursFilter: Enable or disable the hours filter.

### OnTick()

The OnTick() function is executed on every tick of the market. It retrieves the current bid and ask prices and checks if a peaks and valleys pattern is formed. If the pattern is detected and the current price is above the previous peak or below the previous valley, buy and sell orders are placed using the Trade.Buy() and Trade.Sell() functions respectively. Notifications are also sent to the trader to inform about the opened orders.

### IsPeak()

The IsPeak() function checks if the current candle is a peak by comparing the high values of the previous three candles. If the high value of the current candle is higher than the highs of the previous two candles, it returns true.

### IsValley()

The IsValley() function checks if the current candle is a valley by comparing the low values of the previous three candles. If the low value of the current candle is lower than the lows of the previous two candles, it returns true.

### OnTrade()

The OnTrade() function is executed whenever a trade operation is closed. It checks if any order is closed and sends a notification to the trader with the details of the closed order.

### OnTimer()

The OnTimer() function is executed on every timer event. It checks if the news filter and hours filter are enabled, and based on their settings, enables or disables the expert advisor for trading. If the news filter is enabled, it checks if relevant market news is available using the IsNewsRelevant() function. If the hours filter is enabled, it checks if the current time is within the trading hours using the IsTradingHours() function.

### IsNewsRelevant()

The IsNewsRelevant() function is responsible for determining if relevant market news is available. This function should be implemented by the trader according to their own logic and requirements.

### IsTradingHours()

The IsTradingHours() function is responsible for determining if the current time is within the trading hours. This function should be implemented by the trader according to their own trading schedule.

## Product Description

The Prop Firm Challenge Manager is an expert advisor developed by the Forex Robot Easy Team. It is designed to assist traders in managing their trading operations during a prop firm challenge. This expert advisor is specifically programmed to identify peaks and valleys patterns in the market and execute buy and sell orders based on the formation of these patterns.

The Prop Firm Challenge Manager allows traders to set their desired stop loss and take profit levels, as well as enable optional filters for news events and trading hours. By using this expert advisor, traders can automate their trading strategies and take advantage of potential trading opportunities without requiring constant manual monitoring of the market.

Please note that ForexRobotEasy is not the official developer of this product. We are showcasing a sample code that can work as described in this product. To find the official developer of this product, please use the MQL5 platform.

For detailed reviews and trading results of this product, please visit the following link: [Prop Firm Challenge Manager Expert Review](https://forexroboteasy.com/forex-robot-review/prop-firm-challenge-manager-expert-review-on-forex-software/).


# Gold Price Prediction & Trading Automation Bot

## Overview
This project uses a deep learning model (LSTM) to predict gold price movements and automatically places trades via the Deriv API. It sends trading signals to Telegram every 4 hours based on the model’s forecast.

## Key Features
- **Gold Price Prediction** using an LSTM model trained on recent historical data.
- **Signal Filtering**: Trades only if the predicted movement is significant (≥ $20).
- **Automated Trading**: Uses Deriv API to place trades 4 times a day.
- **Telegram Alerts**: Sends clear BUY/SELL signals via Telegram.
- **Performance Metrics**: Evaluated using MAPE, R², and RMSE.

## How It Works
1. Every 4 hours:
   - The bot fetches the latest gold price data using TwelveData API.
   - It predicts the price for the next interval using an LSTM model.
   - If the expected movement is significant (≥ $20), it sends a signal to Telegram and places a trade on Deriv.
2. The stake size is 20% of the current wallet balance.

## Tech Stack
- Python (Pandas, NumPy, Scikit-learn, Keras)
- TwelveData API (for real-time data)
- Telegram Bot API
- Deriv API (for placing trades)

## Evaluation Results
- **MAPE**: XX%
- **R² Score**: XX
- **RMSE**: XX

## Usage
- Set your Telegram bot token and chat ID.
- Set your Deriv API token.
- Run the notebook in a cloud environment or VPS.
- Make sure it runs continuously for 4-hour interval checks.

## Future Improvements
- Add stop-loss or take-profit logic.
- Use ensemble models or technical indicators.
- Deploy via Docker or FastAPI for production readiness.

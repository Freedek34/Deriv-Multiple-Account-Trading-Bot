Deriv Multiple Account Trading Bot
Description
This repository contains a Python-based trading bot designed to manage and execute trades across multiple Deriv.com accounts simultaneously. It automates trading strategies, allowing users to apply the same logic or different strategies across various accounts without manual intervention. This bot is ideal for traders who manage a portfolio of Deriv accounts and seek to streamline their trading operations.

Features
Multi-Account Support: Connect and manage trades on multiple Deriv.com accounts concurrently.

Automated Trading: Execute predefined trading strategies automatically.

Customizable Strategies: Easily integrate and customize your own trading logic.

Risk Management: Implement stop-loss and take-profit levels for each trade.

Real-time Monitoring: (Potentially, if implemented) Monitor trade status and account performance.

User-Friendly Configuration: Simple setup for API tokens and account details.

Installation
To get started with the Deriv Multiple Account Trading Bot, follow these steps:

Clone the repository:

git clone https://github.com/Freedek34/Deriv-Multiple-Account-Trading-Bot.git
cd Deriv-Multiple-Account-Trading-Bot

Create a virtual environment (recommended):

python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate

Install the required dependencies:

pip install -r requirements.txt

Usage
Configure your accounts and strategies:

Open the config.py (or similar, depending on the actual file structure) file.

Enter your Deriv.com API tokens and account details.

Define your trading parameters, such as symbols (e.g., XAUUSD), trade sizes, stop-loss, and take-profit levels.

Example config.py structure (adjust based on actual implementation):

# config.py
ACCOUNTS = [
    {
        "api_token": "YOUR_ACCOUNT_1_API_TOKEN",
        "account_id": "CR12345", # Optional, for identification
        "strategy": {
            "symbol": "XAUUSD",
            "trade_type": "buy",
            "lot_size": 0.05,
            "entry_price": 3215.00, # Example, bot would typically determine this
            "stop_loss": 3205.00,
            "take_profit": 3255.00
        }
    },
    {
        "api_token": "YOUR_ACCOUNT_2_API_TOKEN",
        "account_id": "CR67890",
        "strategy": {
            "symbol": "EURUSD",
            "trade_type": "sell",
            "lot_size": 0.10,
            "stop_loss": 1.0800,
            "take_profit": 1.0700
        }
    }
]

Run the bot:

python main.py

The bot will connect to your specified accounts and start executing trades based on your defined strategies.

Configuration
The primary configuration is done within the config.py file. Please ensure you fill in the following details accurately:

ACCOUNTS: A list of dictionaries, where each dictionary represents a Deriv account.

api_token: Your Deriv API token for the account. You can generate one from your Deriv account settings.

account_id: (Optional) A unique identifier for your account, useful for logging and tracking.

strategy: A dictionary defining the trading parameters for that specific account.

symbol: The trading instrument (e.g., XAUUSD, EURUSD).

trade_type: buy or sell.

lot_size: The volume of the trade.

entry_price: The desired entry price (the bot might use market price if not specified for immediate execution).

stop_loss: The stop-loss price.

take_profit: The take-profit price.

Disclaimer
Trading in financial markets carries a high level of risk, and you can lose money. This bot is provided for educational and informational purposes only and should not be considered financial advice. Use it at your own risk. The developers are not responsible for any financial losses incurred from using this software.

Always test your strategies thoroughly on a demo account before deploying them on a real money account.

Contributing
Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

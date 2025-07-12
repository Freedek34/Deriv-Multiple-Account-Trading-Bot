Deriv Multiple Account Trading Bot
Backstory: Scaling Our Trading Operations
As the founder of a budding trading firm, my journey has been about constant innovation and growth. A key challenge we faced was efficiently managing and scaling our trading activities across multiple client accounts on Deriv.com. Manual execution was simply not sustainable, and we needed a robust solution to expand our Assets Under Management (AUM) and streamline operations for our team and clients.

That's where the idea for this Deriv Multiple Account Trading Bot was born. It's a tool I developed to automate our trading strategies, allowing us to apply consistent logic or tailored approaches across various accounts simultaneously. This bot is a direct result of our efforts to professionalize and expand our trading capabilities, and I believe it can offer similar benefits to other traders and firms looking to optimize their Deriv.com operations.

Description
This repository contains a Python-based trading bot meticulously designed to manage and execute trades across multiple Deriv.com accounts concurrently. It automates trading strategies, enabling users to apply the same logic or different strategies across various accounts without manual intervention. This bot is ideal for traders who manage a portfolio of Deriv accounts and seek to significantly streamline their trading operations.

Features
Multi-Account Support: Seamlessly connect and manage trades on multiple Deriv.com accounts concurrently.

Automated Trading: Execute predefined trading strategies automatically, ensuring consistent application of your market views.

Customizable Strategies: Easily integrate and customize your own trading logic, giving you full control over your approach.

Robust Risk Management: Implement essential stop-loss and take-profit levels for each trade, helping to protect your capital.

Real-time Monitoring: (Potentially, if implemented) Keep track of trade status and account performance with real-time updates.

User-Friendly Configuration: Enjoy a straightforward setup process for API tokens and account details, getting you up and running quickly.

Installation
To get started with the Deriv Multiple Account Trading Bot, follow these simple steps:

Clone the Repository:

Bash

git clone https://github.com/Freedek34/Deriv-Multiple-Account-Trading-Bot.git
cd Deriv-Multiple-Account-Trading-Bot
Create a Virtual Environment (Recommended):
It's best practice to use a virtual environment to manage dependencies.

Bash

python -m venv venv
On Windows:

Bash

venv\Scripts\activate
On macOS/Linux:

Bash

source venv/bin/activate
Install Required Dependencies:

Bash

pip install -r requirements.txt
Usage
Once installed, configuring and running the bot is straightforward:

Configure Your Accounts and Strategies:
Open the config.py file in the root directory of the cloned repository. Here, you'll enter your Deriv.com API tokens and account details. Define your trading parameters, such as symbols (e.g., XAUUSD), trade sizes, stop-loss, and take-profit levels for each account.

Example config.py structure:

Python

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
Run the Bot:
With your configuration set, simply run the main script:

Bash

python main.py
The bot will then connect to your specified accounts and begin executing trades based on your defined strategies.

Configuration Details
The primary configuration for the bot is handled within the config.py file. Please ensure you fill in the following details accurately:

ACCOUNTS: A Python list where each dictionary within the list represents a distinct Deriv account.

api_token: Your Deriv API token for the specific account. You can generate one from your Deriv account settings.

account_id: (Optional) A unique identifier for your account, which can be highly useful for logging and tracking performance across different accounts.

strategy: A dictionary that defines the trading parameters for that particular account.

symbol: The trading instrument you wish to trade (e.g., XAUUSD, EURUSD).

trade_type: Specifies the direction of the trade: buy or sell.

lot_size: The volume or size of the trade you wish to execute.

entry_price: The desired entry price. Note that the bot might use the current market price for immediate execution if not strictly adhered to or if a different entry logic is implemented.

stop_loss: The price level at which the trade will be automatically closed to limit potential losses.

take_profit: The price level at which the trade will be automatically closed to secure profits.

Disclaimer
Trading in financial markets carries a high level of risk, and you can lose money. This bot is provided for educational and informational purposes only and should not be considered financial advice. Use it at your own risk. The developers are not responsible for any financial losses incurred from using this software.

Always test your strategies thoroughly on a demo account before deploying them on a real money account.

Contributing
Contributions are highly welcomed and are what make the open-source community such an amazing place to learn, inspire, and create. If you have suggestions for improvements, exciting new features, or critical bug fixes, please feel free to open an issue or submit a pull request.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

License
This project is licensed under the MIT License - see the LICENSE file for full details.

Contact
Feel free to reach out for collaborations or inquiries!

Clinton Etute

Email: clintonetute@gmail.com

Project Link: https://github.com/Freedek34/Deriv-Multiple-Account-Trading-Bot.git

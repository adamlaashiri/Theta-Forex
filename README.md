# Theta Forex
## About
Theta Forex is forex trading bot, developed with abstraction, inheritance and polymorphism in mind. The structure of the code makes it super easy to implement additional functionality. The bot works with Oanda, but can easily be changed to work with other brokers if so pleased. The main focus of this application is the structure of the classes.

TA class calculates technical indicators commonly used in the market. State, which inherits from TA, contain all the necessary data for a given pair (e.g EUR/USD) from a point in time, up until the time the class was instantiated. State is also responsible for executing trades. A strategy which is implemented with IStrategy, inherits from STATE and contain the logic for when to buy and sell respectively. Strategy class then assigns a risk component (IRisk) to State (its parent) based on buy / sell signal. States are instantiated through the Controller class, which then executes a trade that generated a buy || sell signal.

This structure makes it really easy to implement your own strategies and risk components (position sizing and risk management) that are through interfaces, compatible with the rest of the system. Controller manages the flow of the operation, meaning whether to enter new trades or only allow a number of trades. Controller is then in turn managed by the agent. Enjoy!


## Disclaimer
There are absolutely no guarantees that this bot will earn you money. Speculation in currencies is a risky business. In fact, price movement follows a brownian motion, meaning that it is completely random in the short term and no valuable insight can be derived from looking only at price data. This bot should solely be used for learning purposes...

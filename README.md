# Automated-Electricity-Trading-Algorithm
Develop and backtest a trading strategy maximizing profits between two auctions of the Great Britain day-ahead electricity market.

# Theoretical background:

1) Electric grids operate at a specific frequency maintained by balancing the supply and demand of electricity. When there is excess supply, the frequency rises; when demand exceeds supply, it drops. The grid's stability relies on keeping the frequency within an acceptable range. Otherwise, power failures may occur. Wholesale electricity markets use a multi-market system to trade electricity bundles to ensure that the balance between supply and demand remains within this range.

2) The day-ahead market is designed to manage most of the short-term supply and demand a day before the scheduled delivery times for technical reasons and to reduce risk. Typically, the day-ahead market uses a sealed-bid pay-as-cleared auction format, where market participants place bids to buy or sell electricity for the next 24 hours. Each participant submits a bid specifying the amount of energy they want to buy or sell at a particular price without knowing the other participants' bids. The pay-as-cleared mechanism determines a uniform price for buyers and sellers based on the market clearing price, which is determined using the merit-order model. All sell orders priced below the clearing price and all buy orders priced above the clearing price are accepted and priced at the clearance price.

3) In order to manage the greater unpredictability and instability in power production associated with the growing utilization of renewable energy sources in the power grid, energy storage systems at the grid scale can offer additional flexibility. Given their capacity to store or deliver power with almost instantaneous response time and high efficiency, battery energy storage systems are especially well-suited to the short-term nature of electricity markets. Consequently, they are widely used and famous for trading purposes

4) In the Great Britain market, it is also possible to engage in trading without possessing an asset like a power plant, renewable source, or battery, as the market offers the option of purely financial trades where energy is neither provided nor received. These trades are distinguished from physical trades, which are backed by an asset. For the purposes of this task, we will focus exclusively on financial trades, as this allows us to avoid the technical complexities associated with asset-backed trading.

# Task description:

1) Develop a little trading algorithm that maximizes profits from financial trades between two day-ahead auctions in Great Britain. The two auctions:
  - function as mentioned with sealed bids and based on the pay-as-cleared mechanism.
  - market hourly bundles of electricity, so auction participants submit bids to buy or sell electricity for every hour of the next operating day.
  - are sequential, meaning that you first must submit your bids for the first auction, wait for its results, and afterward submit your bids for the second auction (a bid consists of a volume you want to buy or sell and
the price you want to pay or receive).

2) Depending on your strategy, producing a price forecast for the second auction can make a lot of sense. You can use the input variables to create your own forecast. You can also choose a different approach or use any data you can find that would be available at the respective time of your forecast.

3) As you act as a non-physical trader, your net position resulting from the trades on the two auctions should be zero for all timesteps, as you cannot provide this net position to the grid the next day. The difference between your net market position after both auctions and the energy you can provide (which is zero as you trade without an asset) will be settled with the so-called system prices.
  - With a net deficit, you must pay the system price to buy the difference in energy back.
  - For a net surplus of energy, the system price is paid to you for the difference in energy.
  - So, it’s also possible to earn money with system prices from either providing less energy than planned to the system (if system prices are negative) or from taking demand out of the market (if system prices are
positive).
  - At the time of the auctions, you do not know precisely the system price. You only have a forecast of its price range available to you.

4) You can assume that every trade results in 5 GBP/MWh of costs for taxes and fees, which you must account for in your strategy.

5) Additional sources for:
  - Physical vs. non-physical electricity trading https://youtu.be/iUeGv-pW5os
  - Day-ahead and intraday electricity trading	https://youtu.be/h2MJo-iw7NA

6) The data utilized in this experiment cannot be published, as it is restricted by privacy rules and regulations in accordance with data protection laws.

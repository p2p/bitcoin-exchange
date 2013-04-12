bitcoin-exchange
================
The purpose of this project is to build a decentralized p2p exchange where client orders 
are matched in one decentralized exchange. Any asset can be traded in this exchange and fees are paid in bitcoin.
This exchange-broker model is a simplified model of the CME Globex exchange handling futures contracts.

Inspiration: CME Group, Bitcoin, #Bitcoin-OTC, Ripple


Exchange:
The exchange network is built with the bitcoin network as inspiration. 
The network has a blockchain of orders that gets processed by miners willing to participate and get rewarded 
from the brokers with one bitcoin for each N orders processed. Order matching is done once every block, and each block should
take 5-10 seconds to complete. The order matching is delibarately slow to prevent High Frequency Trading algorithmis having
having advantgage over the rest of the market. Once the orders are matched it is up to the brokers to settle the traded assets.


Assets:
Any asset pair can be traided in the exchange just as in a futures exchange since no real asset is handled through the exchange itself, 
only orders of assets. An asset pair can be Bitcoin in US Dollar, or 1 Oz Gold in US Dollar or LiteCoin in BitCoin or whatever 
asset the brokers might enable trading in.


Clearinghouse:
Trust is used instead of a clearing house - the brokers are responseble for the actual transfer of assets between the traders.
Voluntary rating of the brokers from the clients could be used to indicate the trustworthiness of each broker.


Brokers:
"A broker is an individual or party (brokerage firm) that arranges transactions between a buyer and a seller, 
and gets a commission when the deal is executed." (http://en.wikipedia.org/wiki/Broker)

Anyone can become a broker in this exchange. 

If several brokers trust eachother they can form a broker-pool by adding eachother as trustworthy, orders from
all of the clients in the specific pool gets matched together.

Brokers that are not part of a broker-pool have their orders processed separately.

Settlement of assets should be made on a regular basis (daily or weekly) between brokers in a broker-pool in order to minimize the possible loss off assets in
the event of fraud or default.

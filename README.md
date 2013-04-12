bitcoin-exchange
================
The purpose of this project is to build a decentralized p2p exchange where client orders 
are matched in one decentralized exchange. Any asset can be traded in this exchange and fees are paid in bitcoin.
This exchange-broker model is a simplified model of the CME Globex exchange handling futures contracts.

Inspiration: github.com/bitcoin, #Bitcoin-OTC, github.com/bitcoinx, github.com/macourtney/Dark-Exchange, github.com/FellowTraveler/Open-Transactions, github/?/p2pool, 
retroshare.sourceforge.net, Ripple.com, CME Group, 


## Exchange:
* The exchange network is built with the bitcoin network as inspiration. 
* The network has a blockchain of orders that gets processed by miners willing to participate and get rewarded 
from the brokers with one bitcoin for each N orders that are forwarded in to the exchange. 
* Order matching is done once every block, and each block should take 10 seconds to complete. 
* The order matching is deliberately slow to prevent High Frequency Trading algorithmis having 
advantage over the rest of the market. The orders are not executed as FIFO but in random order as a second protection 
against HFT. 
* Once the orders are matched it is up to the brokers to settle the traded assets.


## Assets:
* Any asset pair can be traded in the exchange just as in a futures exchange since no real asset 
is handled through the exchange itself, only orders of assets. 
* An asset pair can be: Bitcoin traded in US Dollar, 1 Oz Gold in BitCoin, 1 Oz Silver in BitCoin, LiteCoin in BitCoin, Euro in Dollar, 
or whatever asset pair the brokers wishes to enable trading in.


## Clearinghouse:
* Trust is used instead of a clearing house - the brokers are responsible for the actual transfer of 
assets between the traders. 
* Voluntary rating of the brokers from the clients could be used to indicate the trustworthiness of each broker.


## Brokers:
"A broker is an individual or party (brokerage firm) that arranges transactions between a buyer and a seller, 
and gets a commission when the deal is executed." (http://en.wikipedia.org/wiki/Broker)

* Anyone can become a broker in this exchange.
* The brokers using this exchange can have clients globally or locally.
* Client orders are always forwarded to the exchange by the brokers. Clients dont need internet access 
from the exchanges perspective since the clients will never use the exchange directly. 
* If several brokers trust each other they can form a broker-pool by adding each other as trustworthy, orders from
all of their clients will get matched together in this pool.
* Brokers that are not part of a broker-pool have their own order book in the exchange, their clients will not be able to 
trade with clients of the other brokers.
* Settlement of assets should be made on a regular basis (daily or weekly) between brokers in a broker-pool in order to minimize the possible loss off assets in
the event of fraud or default.
* Each broker must comply by local laws in the jurisdiction where the broker is located. 
* Any legal issue is a matter between brokers or between a broker and its clients.
* The exchange cannot be held responsible for any complaints because of its decentralized nature.

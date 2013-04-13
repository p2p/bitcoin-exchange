bitcoin-exchange
================
The purpose of this project is to build a decentralized p2p exchange where client orders are matched in one global decentralized exchange system.

This exchange system will consist of many virtual exchanges created by broker alliances which enables both local and global trading of digital and physical assets.

Any asset can be traded against any other asset in this exchange and fees are paid in bitcoin.
This exchange-broker model is a simplified model of the CME Globex exchange handling futures contracts.

Inspiration: github.com/bitcoin, #Bitcoin-OTC, github.com/bitcoinx, github.com/macourtney/Dark-Exchange, github.com/FellowTraveler/Open-Transactions, github/?/p2pool, 
retroshare.sourceforge.net, Ripple.com, CME Group, 


## Exchange
* The exchange network is built with the bitcoin network as inspiration. 
* The network has a blockchain of orders that gets processed by miners willing to participate and get rewarded 
from the brokers with one bitcoin for each N orders that are forwarded in to the exchange. 
* Each block takes around 1 second.
* Order matching is done once every block. 
* Order cancelling is delayed for 10 blocks to discourage market manipulation.
* The order matching is deliberately slow to prevent High Frequency Trading algorithmis having advantage over the rest of the market. The orders are not executed as FIFO but in random order as a second protection against HFT. 
* Once the orders are matched it is up to the brokers to settle the traded assets.
* Transaction history of executed orders will be saved in the blockchain as evidence if dispute would occur between brokers and clients
* Brokers need to create unique client ids for each of their clients, but the real identity of the clients will only be known by the broker and can only be revealed to authorities of the jurisdiction where the broker is based.

## Assets
* Assets can be both digital or physical, example: cryptocurrencies such as BitCoin and LiteCoin, digital fiat currencies, physical fiat currencies, gold coins, silver coins, barrel of gasoline.
* Any asset pair can be traded in the exchange just as in a futures exchange since no real asset is handled through the exchange itself, only orders of assets. 
* An asset pair can be: Bitcoin traded in US Dollar, BitCoin in Euro, 1 Oz Gold in BitCoin, 1 Oz Silver in BitCoin, LiteCoin in BitCoin, Euro in Dollar, 1 Barrel of Gasoline in Gold, 100 chicken eggs in 1 Oz Silver, or whatever asset pair the brokers wishes to enable trading in.


## Clearinghouse:
"A clearing house is a financial institution that provides clearing and settlement services for financial and commodities derivatives and securities transactions. 
Once a trade has been executed by two counterparties either on an exchange, or in the OTC markets, the trade can be handed over to a clearing house which then steps between the two original traders' clearing firms and assumes the legal counterparty risk for the trade. This process of transferring the trade title to the clearing house is called novation. It can take fractions of seconds in highly liquid futures markets; or days, or even weeks in some OTC markets."
http://en.wikipedia.org/wiki/Clearing_house_(finance)
* Trust is used instead of a clearing house - the brokers are responsible for the actual transfer of assets between the traders. 
* Voluntary rating of the brokers from the clients could be used to indicate the trustworthiness of each broker.

## Brokers and virtual exchanges
"A broker is an individual or party (brokerage firm) that arranges transactions between a buyer and a seller, and gets a commission when the deal is  executed." (http://en.wikipedia.org/wiki/Broker)
* Anyone can become a broker in this exchange.
* A broker must either join an existing virtual exchange or create a new virtual exchange where orders will be executed. 
* Each broker wishing to join a virtual exchange must be approved by the founder of the virtual exchange which is done by mutual exchange of certificates.
* When several brokers exist in a virtual exchange their order books will merge for each asset pair they have in common and all of their clients orders will get matched together.
* Creation of a virtual exhange by virtual exchanges is not allowed, therefore trading between virtual exchanges is not possible. 
* All brokers should use .bit domains (NameCoin) as a backup domain.
* Two classes of brokers: Class A Broker can settle assets with brokers in other jurisdictions, Class B Broker can only settle assets with a Class A Broker in the same jurisdiction.
* Each broker has its own order book, and its own asset pairs.
* The brokers using this exchange can have clients globally or locally.
* Client orders are always forwarded to the exchange by the brokers. Clients dont need internet access 
from the exchanges perspective since the clients will never use the exchange directly. 
* Settlement of assets should be made on a regular basis (daily or weekly) between brokers in a broker-pool in order to minimize the possible loss off assets in
the event of fraud or default.
* Each broker must comply with local laws in the jurisdiction where the broker is located. 
* Any legal issue is a matter between brokers in a virtual exchange or between a broker and its clients.
* The exchange itself cannot be held responsible for any legal issues.

## Fees
* Fees are taken from the brokers and virtual exchanges to encourage miners to provide computing power to the exchange and to discourage creation of fake virtual exchanges, brokers and orders. 
* Brokers and Virtual Exchanges will have bitcoin wallets created in the bitcoin blockchain where they send bitcoins in advance to pay for the exchange fees. If the broker-wallet or virtual exchange-wallet is empty no orders are processed for that broker or virtual exchange.
* The actual fees must be discussed in the community.

* Broker periodical fee: 1 BTC per 30 days (18 144 000 blocks)
* Virtual exchange fee: 10 BTC per 30 days (18 144 000 blocks)
* 1 BTC per 10 000 Orders forwarded to the Exchange
* 1 BTC per 100 000 Orders cancelled from the Exchange  

## Questions
* If the exchange should work as a stock exchange instead of a futures exchange: How to prevent short selling assets that the client dont own and the broker cannot lend on the market?
* Minimum trading size in each asset to prevent order spamming? (0.1 BTC)
* Even trading sizes? (0.1, 0.2, 0.3 ...BTC)
* Clearing houses or two classes of brokers? 
* Market makers?
* Darknet?
* Digital tokens to represent the traded assets and wallets to handle the tokens?
* Allowing creation of alliances between virtual exchanges?

Discussion on: https://bitcointalk.org/index.php?topic=172705.0

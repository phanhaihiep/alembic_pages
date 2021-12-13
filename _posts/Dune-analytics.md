---
title: Dune analytics
categories:
- Cryptocurrency

feature_text: by OxBoxer
  The journey of learning computer science and cryptocurrency
( 2 minutes reading)

### Project: Dune is the data hub for defi, lets take a look to be a DUNE analytics

Key note:
1. what dune case and how can used
2. how dune works
3. dune database
4. querying and case studies

End result:
1. create querries and dashboard
2. understand the dune database
3. ask the right question
4. know where to look for answers

Course structure:
1. this presentation
2. dune dashboards
3. query editor
4. some tasks down the line

Espisose 1: Uses case and its application
Dune analytics is a data analytics platform that enables anyone to easily aggregate and analyse blockchain data
if something onchain, you can track it using DA
aggregate data on dune save the unnessessary infrastructure overhead. like hosting a website, creat a database to cointain all the data, no worry about loading data.
DA is a collaborative effort between all users, all data and methods to get the data are inherently public.

topic 1:
1. how dune used
- project dashboard
    + data on 1 project
    + helps the project make decisions
    + helps the project keep track of their finances
- sector dashboard
    + decentrialized indices: indices-products
    + decentralized exchanges: dex-metrics
- ecosystem dashboard
    + gas-prices: kroeger0x/gas-prices
    + defi users: rchen8/defi-users-over-time
    
2. what is the use case
- surface data for your project
- aggregate data on an entire sector
- collect data on more general ecosystem stats
whatever the use case is, you can probably do it on Dune
3. how dune work
- collect the data of the etherum blockchain in a neatly organized tables that can querry
- use pgSQL, open source object relational database system
- dealing with data by decoding smart contracts and abstracting data in prepare table
- knowledge of SQL + blockchain = Blockchain analyst

in action:
click new querry
type select * from ethereum.transactions
limit 100
and run

the database structure:
1. dune techy
2. database structure
    on chain: Ethereum
    + raw data
        - examples: ethereum.transactions, ethereum.logs, ethereum.traces
        - raw data tables are hard work because they contain encode data
        - raw transactions do still contain a lot of information, it is just heard to uncover
        - if you can, submit the contracts in questions for decoding.
    + decode data
    + token standard tables
        - erc20 ERC20 evt Transfer
        - erc721 ERC721 evt Transfer
        - erc1155 ERC1155 evt Transfer
        these tables are able to pick up on standardized contracts and collect them in one table. 
        instead of having to querry each token contract itself the data is all one place
    + prepared data
        - dex.trades -> dashboard -> querry
        - lending.collateral change
        - abstractions are table that are custom made by the community or Team Dune
        - they standardize data between projects or several smart contract
        - the abstractions are maintained in a public github repository
        - everyone can submit changes to the github respository, it is maintained by team dune and the community
    + dex price data
    https://github.com/duneanalytics/abstractions
    3rd Party/mixed:
    + prices table
        - price.usd is data from coinpaprika (competitor of coingecko)
        - dex.view_token_prices is data dynamically calculated form the dex.trades table
    + lookup table
    + lables
        - the labels feature allows you to give a tag to any address
        - this allows for analysis of wallets based on their prior activities.
        - the labels are community sourced
        - anayone can add labels through the label pages or through querries.

    + summary diagram: https://app.diagrams.net/#G1N9Hz1xf5KxW8DTAqaeTDmYr-GLwSY6cC
3. decoding data
- submit contracts to DA via form
- make sure to in the correct data in the correct order
- talk to the team of the project if you are unclear
- make sure to check if the contract is a proxy
- make sure to check if the contract that has several instance
- check the contract to see example of proxy and same bytecode


Summary:
- Dune is fundemental a pgSQL database in which you only have read access
- limited write access is managed through our abstraction
- querrying for data is easier with decoded data
- the abstraction often times make your life easier since somebody else has solved problems in there already
- use abstraction wherever you can or create them where you see applicable
- request for new abstractions are always welcome!
- the different kinds of data are documented.




---- day 1: create simple querries and dashboard
1. create simple querries
2. make visualisations
3. assemble them on a dashboard
4. work in parameters: you can change the address dynamic

game plan:
- total gas spent:
- transaction counter
- average gas price
- failed tx's
- how could we improve upon this

result:
https://dune.xyz/phanhaihiep/gas-tracker-dashboard

website: https://fees.wtf/

---- day 2: ERC 20 token balance
topic:
- understanding the tables and views
- working with the tables and views
- what this enables you to do

erc token balance
column name: wallet_addresss, token_addresss, token_symbol, amount_raw, amount
description: the address of the token holder, the contract address of the erc20 token, the symbol of the erc20 token, the raw amount of the token, raw_amount/1^10 decimals

views:
erc20.view_token_balances_lastest: gives a snapshot of the lastest erc20 balances
erc20.view_token_balances_hourly: gives back price, amount, amount_raw and token symbols
erc20.view_token_balances_daily: improved performance due to daily balances instead of hourly


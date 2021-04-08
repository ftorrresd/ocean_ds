# Bitcoin Historical Data

Source: https://www.kaggle.com/mczielinski/bitcoin-historical-data

## Context

Bitcoin is the longest running and most well known cryptocurrency, first released as open source in 2009 by the anonymous Satoshi Nakamoto. Bitcoin serves as a decentralized medium of digital exchange, with transactions verified and recorded in a public distributed ledger (the blockchain) without the need for a trusted record keeping authority or central intermediary. Transaction blocks contain a SHA-256 cryptographic hash of previous transaction blocks, and are thus "chained" together, serving as an immutable record of all transactions that have ever occurred. As with any currency/commodity on the market, bitcoin trading and financial instruments soon followed public adoption of bitcoin and continue to grow. Included here is historical bitcoin market data at 1-min intervals for select bitcoin exchanges where trading takes place. Happy (data) mining!

## Content

`bitstampUSD_1-min_data_2012-01-01_to_2020-09-14.csv`

CSV files for select bitcoin exchanges for the time period of Jan 2012 to September 2020, with minute to minute updates of OHLC (Open, High, Low, Close), Volume in BTC and indicated currency, and weighted bitcoin price. Timestamps are in Unix time. Timestamps without any trades or activity have their data fields filled with NaNs. If a timestamp is missing, or if there are jumps, this may be because the exchange (or its API) was down, the exchange (or its API) did not exist, or some other unforeseen technical error in data reporting or gathering. All effort has been made to deduplicate entries and verify the contents are correct and complete to the best of my ability, but obviously trust at your own risk.

## Acknowledgements and Inspiration

Bitcoin charts for the data. The various exchange APIs, for making it difficult or unintuitive enough to get OHLC and volume data at 1-min intervals that I set out on this data scraping project. Satoshi Nakamoto and the novel core concept of the blockchain, as well as its first execution via the bitcoin protocol. I'd also like to thank viewers like you! Can't wait to see what code or insights you all have to share.
# Financial Data Platform

## Features
1. Automatic data ingestion through different types of interfaces, for example the most popular like HTTP based API and SQL.
2. Data transformation, enrichment, checking data quality.
3. Do accounting using given data with strong consistency and the technics of the control

## Embedded language specification
### JS 

### Work with money or numeric

First of all working with money like a regular mathematical floating calculations must be strongly prohibited and fixed decimal point calculations should be used instead

let calculate total amount as multilication of price and quantity:

  `amount  = decimal(tx.price).Mul(decimal(tx.qty)`

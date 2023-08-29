# Financial Data Platform

## Features
1. Automatic data ingestion through different types of interfaces, for example the most popular like HTTP based API and SQL.
2. Data transformation, enrichment, checking data quality.
3. Do accounting using given data with strong consistency and the technics of the control

## Embedded language specification
### JS 

### Date and time, timestamp
By default in the most cases, timestamp can be parsed automaticaly from the most used formats, including uniq timestamp in seconds or milliseconds, but optionally format (layout) can be specified.

examples:
"01/02 03:04:05PM '06 -0700" // The reference time, in numerical order.
"Mon Jan _2 15:04:05 2006" // ANSIC
"Mon Jan _2 15:04:05 MST 2006" // UnixDate
"Mon Jan 02 15:04:05 -0700 2006"
"02 Jan 06 15:04 MST"
"02 Jan 06 15:04 -0700" // RFC822 with numeric zone
"Monday, 02-Jan-06 15:04:05 MST" // RFC850
"Mon, 02 Jan 2006 15:04:05 MST" // RFC1123
"Mon, 02 Jan 2006 15:04:05 -0700" // RFC1123 with numeric zone
"2006-01-02T15:04:05Z07:00" //RFC3339

`timestamp(tx.timestamp)`
`timestamp(tx.timestamp, '02-01-06 15:04')` // eg 24-06-22 07:49

### Work with money or numeric

First of all working with money like a regular mathematical floating calculations must be strongly prohibited and fixed decimal point calculations should be used instead

let calculate total amount as multilication of price and quantity:

  `amount  = decimal(tx.price).Mul(decimal(tx.qty)`

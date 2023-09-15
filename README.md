# Financial Data Platform
Fin-DP provides a modern financial data platform for fintech and modern companies.



## Key Features of the Financial Data Platform
**Data Ingestion**: FDP’s collect data from diverse sources like banks, payment gateways, accounting software, and common financial files.

**Data Aggregation**: FDP’s provide a single entry point for all reviewing financial data at an organization, enabling finance teams to quickly identify specific transactions and verify complex funds flows. 

**Financial Controls**: It's crucial to ensure that financial intents are consistent with company expectations and regulatory requirements. FDP’s enable automation to enforce the procedures and policies that help companies oversee their financial information and reporting.

**High resolution accounting**: FDP’s allow companies to maintain detailed, transaction-level subledgers across their organization, to ensure complete visibility and robust categorization of transactions across the company. 

**Automated Reconciliation**: An integral aspect of FDP’s, reconciliation ensures that financial data aligns and corresponds with data from other sources, like bank statements or third party processors. By enabling automated reconciliation processes, finance teams can quickly verify the accuracy of financial data, spotting any discrepancies, and resolving them promptly.

**Reporting Source of Truth**: Financial data often exists across a vast array of sources, including internal databases & reporting platforms, banks, accounting software, and payment processor portals. FDP’s enable teams to build a unified source of truth for their financial data, enabling real time visibility into their financials and smooth audits.

## Benefits of Financial Data Platforms
**Holistic Financial View:** Consolidating all financial data provides users with a comprehensive overview of their finances and key data. 

**Enhanced Accuracy and Trustworthiness:** Automated reconciliation and stringent financial controls reduce errors, ensuring data is reliable and trustworthy.

**Efficiency and Time Savings:** Automation significantly reduces manual input, allowing for strategic focus.

**Cost reduction:** Financial data platforms greatly reduce the cost of in house technical support for key data flows, allowing organizations to operate efficiently.

**Flexibility and Scalability:** As financial data volume grows, these platforms scale efficiently, as they’re purpose built for high volumes of transaction data.
‍
## Financial Data Platforms vs. ERPs
ERP or Accounting software in common are  designed to manage  mature and regulated business processes within required financial flows.
FDPs and Enterprise Resource Planning (ERP) or accounting software serve different purposes. While ERPs manage company finances, they often lack the robust, embedded rules engines to automate the processes and workflows that FDPs provide. Financial data platforms are designed to work with ERPs, enabling efficient financial management.
Financial data platforms often offer flexible sub-ledgers to allow for high volume accounting outside of the ERP. For example, companies use Proper’s subledgers to manage high volume transactions. 
FDPs are built to handle high transaction load and can help manage more robust data intensive operations, such as normalization, transformation, and reconciliation.

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

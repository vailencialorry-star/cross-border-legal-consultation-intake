# Classification Framework

Use this framework after capturing every source question. Adapt labels, but keep stable IDs and a source mapping.

## 1. Transaction, contract, title and platform roles — `T`

| Code | Issue family | Typical questions |
|---|---|---|
| T1 | Business-model role | Who is seller, principal, agent, platform, consignee, warehouse or service provider? |
| T2 | Contract characterization | Sale, barter, consignment, agency, auction, service or hybrid? |
| T3 | Title and delivery | When does title pass? Is physical delivery, constructive delivery, direction or attornment required? |
| T4 | Governing law | Contract law, property law, consumer law and mandatory rules? |
| T5 | Client-asset segregation | Commingling, lien, insurance, insolvency, attachment, reconciliation? |
| T6 | Defective title | Stolen goods, impersonation, pledge, competing title, good-faith purchase and return? |
| T7 | Route roles | Seller, exporter, importer/IOR, invoice issuer, consignee and risk bearer? |
| T8 | Product format | Fixed price, offer, negotiation, swap, auction, fractionalization or tokenization? |
| T9 | Platform/warehouse licence | Marketplace, telecom, auction, secondhand, warehouse and local establishment? |
| T10 | Seller status | Personal seller vs. dealer/merchant; platform detection and upgrade? |
| T11 | Consumer and product responsibility | Description, grading, authentication, defects, return, refund, delivery and disclaimers? |

## 2. China tax, customs and import — `C`

| Code | Issue family | Typical questions |
|---|---|---|
| C1 | Authorization and import permission | Brand authorization, distribution right, permit, internal broker requirement? |
| C2 | Classification | HS code, ordinary goods, collectibles, games, toys, printed material or publication? |
| C3 | Intellectual property | Parallel import, trademark, copyright, image/database and authenticity? |
| C4 | Source and value evidence | Purchase record, invoice, payment, grading, photo, chain of title, logistics? |
| C5 | B2B route | Self-import, agency import or platform buyout; IOR, title, tax and invoice? |
| C6 | Customs prohibitions | Understatement, misclassification, splitting, false gift/personal use, false three-data set? |
| C7 | Personal import | Personal use, reasonable quantity, value, indivisible item and courier responsibility? |
| C8 | Revenue and invoice | P2P, consignment, buyout; principal vs. agent; product and service invoice? |
| C9 | Personal seller tax | Property transfer vs. business income; enterprise purchase evidence? |
| C10 | Barter tax | Fair value, cash top-up, income, cost, VAT and evidence? |
| C11 | Offshore income | Resident individual/company reporting and foreign tax credit? |
| C12 | Platform reporting/service tax | Platform tax reporting, cross-border service VAT/withholding and agent? |

## 3. Criminal, AML, payment and FX — `A`

| Code | Issue family | Typical questions |
|---|---|---|
| A1 | Regulated AML status | Financial institution, designated non-financial business or other reporting person? |
| A2 | Value-transfer characterization | Payment, remittance, stored value, exchange, merchant acquisition or goods trade? |
| A3 | Transaction red flags | Unequal value, loops, rapid turnover, no withdrawal, linked accounts? |
| A4 | Funds control | PSP, escrow, reserve, delayed settlement, deposit, refund, chargeback and freeze? |
| A5 | Hold powers | Platform suspension, warehouse lien, PSP freeze and government seizure? |
| A6 | STR and tipping-off | Reporter, channel, threshold, confidentiality and user communications? |
| A7 | SOA/SOF/SOW | Source of asset, funds and wealth; personal vs. dealer evidence? |
| A8 | Screening and linkage | Sanctions, PEP, UBO, device, address, third-party payer/recipient? |
| A9 | Criminal exposure | Smuggling, proceeds of crime, fraud, stolen goods, invoice and illegal business? |
| A10 | FX/payment licence | Cross-border currency conversion, collection, settlement and platform instructions? |

## 4. Foreign local operations — jurisdiction prefix

Use `JP`, `SG`, or another ISO-like jurisdiction prefix. Split the following issue families as needed:

- Marketplace and secondhand-dealer rules.
- Warehouse, bailment, long-term custody and client assets.
- Property transfer and third-party effectiveness.
- Consumption tax, GST/VAT, income and invoices.
- Import/export, customs value, importer and exporter.
- Payment licensing and AML.
- Consumer law and advertising.
- Privacy and overseas transfer.

## 5. Data, identity and evidence — `D`

| Code | Issue family |
|---|---|
| D1 | Personal/business account, KYC/KYB/UBO and enhanced due diligence |
| D2 | KYC provider/PSP custody of original identity documents and data minimization |
| D3 | Order, payment, logistics, tax, customs and ownership record retention |
| D4 | Transaction-specific evidence package and decision trail |
| D5 | Cross-border data map, localization, recipient and transfer mechanism |
| D6 | Electronic signature, timestamp, hash, version, access and chain of custody |

## 6. Group, treaty and disputes — `I`

| Code | Issue family |
|---|---|
| I1 | Entity, branch, IP, software and brand location |
| I2 | Intercompany services, licence, purchase price and transfer pricing |
| I3 | Permanent establishment and local taxable presence |
| I4 | CISG or other sales convention inclusion/exclusion |
| I5 | Trade agreement, tariff preference and origin |
| I6 | Double-tax treaty, withholding and foreign tax credit |
| I7 | Courts, arbitration, interim relief and cross-border enforcement |

## Priority rules

Mark **P0** if the issue can block launch, invalidate title, expose client money, cause customs/criminal liability, or require a licence. Mark **P1** if it blocks scale, long-term custody, local establishment, data transfer, consignment or buyout. Mark **P2** for optimization and future governance.

## Coverage rule

Every original question must appear in the final coverage index. If one normalized issue covers several source questions, list all source locations. If one source question spans several domains, map it to multiple normalized issues.

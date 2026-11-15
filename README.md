# Keva_20251SEN240_credit-card-fraud-detection
# Credit Card Fraud Detection Rules with Oracle PL/SQL

**Student:** Nyirishema Kaliza Keva
**Student ID:** 20251SEN240
**Course:** INSY 8311, Database Programming (AUCA)
**Instructor:** Eric Maniraguha

## Problem Statement
Describe who loses money when fraudulent card payments go undetected, and why
manual checking is too slow. Keep it to one or two paragraphs.

## Objectives
**Main objective:** Build an Oracle database that flags unusual card transactions
using rules enforced in PL/SQL.

**Specific objectives:**
1. Store anonymized transactions, accounts, and fraud flags in 3NF tables.
2. Use a trigger to flag transactions whose amounts are unusually high for an account.
3. Use functions and procedures to calculate account risk scores.
4. Use cursors to produce a daily summary of flagged activity.
5. Provide an audit log of all changes to flags.

## Data Source
- **Dataset:** Credit Card Fraud Detection, Kaggle
- **Link:** [https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud]
- **License:** [http://opendatacommons.org/licenses/dbcl/1.0/]
- **Size:** about 285,000 transactions
- **Note:** The dataset is anonymized. No personal information is used or stored.

## Innovation
**Option chosen:** Analytics layer / security dashboard
**Tool:** [Power BI or Grafana]
**What it does:** Shows flagged transactions, risk scores, and alerts from the
live Oracle database.
**How to run it:** See `innovation/README.md` (to be completed in Phase VII).

## Planned Tables
| Table | Purpose |
|-------|---------|
| ACCOUNTS | One row per cardholder account (anonymized ID) |
| TRANSACTIONS | One row per payment: amount, time, merchant category, label |
| FRAUD_FLAGS | Flags raised by rules, with reason and status |
| AUDIT_LOG | Records each insert, update, or delete on flags |

## Planned PL/SQL Features
| Feature | Use in this project |
|---------|---------------------|
| Trigger | Flags a transaction whose amount exceeds the account's average by a set factor |
| Function | Returns an account's risk score from recent flags |
| Procedure | Records a flag and writes to the audit log |
| Cursor | Loops through accounts to build the daily summary |
| Package | Groups the fraud rules and risk functions together |
| Exception handling | Handles missing accounts and invalid amounts |


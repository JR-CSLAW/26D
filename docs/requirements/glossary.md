# Glossary and Business Rules – NewEra POS

| | |
| --- | --- |
| **Maintainer** | Avni Oflaz |
| **Version** | 0.1 (draft for review) |
| **Last updated** | W06 |
| **Part of** | SRS (Assignment 1), ISO/IEC/IEEE 29148 |

## 1. Purpose

This document defines the shared vocabulary of the NewEra POS project and lists the business rules of the store. All SRS sections, use cases and design documents should use the terms exactly as defined here, and should refer to business rules by their ID (for example, "see BR-09").

Business rules describe **store policies**, not system features. Functional requirements (FR-xx) will later implement them, and the traceability matrix will link each requirement to the rules it follows.

## 2. Glossary

Terms are sorted alphabetically. Where two words mean the same thing, the preferred term is used in all documents and the other is listed as a synonym.

| Term | Definition |
| --- | --- |
| **Accounting System** | External system that records the store's sales, returns, rentals and payments for bookkeeping. |
| **Authorization** | Approval of a credit card payment by the Payment Service before a transaction is completed. |
| **Cashier** | Store employee who operates the register and processes sales, returns and rentals. Primary actor of all four use cases. |
| **Cashier session** | The period between a cashier's login and logout on one register. Every transaction in the session is linked to that cashier. |
| **Change due** | Amount returned to the customer when the cash tendered is greater than the total. |
| **Customer** | Person who buys, returns or rents items at the store. |
| **Deposit** | Refundable amount paid by the customer when renting an item, kept as a guarantee until the item is returned. |
| **Due date** | Date by which a rented item must be returned. |
| **Default tax rate** | A tax rate stored locally and used only when the Tax Calculator is unavailable (see BR-02). |
| **External system** | A system outside NewEra POS that the POS communicates with: the Payment Service, Tax Calculator, Accounting System and HR System. |
| **HR System** | External system that holds employee data, used to identify valid cashiers and their roles. |
| **Item** | A single physical unit of a product that can be sold or rented. |
| **Inventory** | The record of the store's items, with their stock levels and, for rentable items, their item status. |
| **Item identifier** | Unique code (for example, a barcode) that identifies a product description and is scanned or typed by the cashier. |
| **Item status** | State of a rentable item: *Available*, *Rented*, *Under maintenance* or *Reserved*. Only *Available* items can be rented. |
| **Line item** | General term for one line of a transaction: see *Sale line item* and *Rental line item*. |
| **Late fee** | Charge applied when a rented item is returned after its due date (see open questions). |
| **Opening cash** | Amount of cash in the register drawer at the start of a cashier session. |
| **Overdue rental** | A rental whose due date has passed without the item being returned. |
| **Payment Service** | External system that authorizes or declines credit card payments. Synonym: *payment authorization system*. |
| **POS (Point of Sale)** | The system used at the counter to record transactions and take payments. In this project: NewEra POS. |
| **Product catalog** | The set of all product descriptions known to the store. |
| **Product description** | Information about a product: item identifier, name, price and whether it can be rented. |
| **Receipt** | Printed record of a completed transaction, given to the customer. |
| **Refund** | Money paid back to the customer for a returned item. |
| **Register** | The physical POS terminal (computer, scanner, cash drawer, receipt printer) at which a cashier works. |
| **Rental** | Transaction in which a customer takes an item for a limited period, pays a rental fee and a deposit, and must return it by the due date. |
| **Rental fee** | Price charged for renting an item for the rental period. |
| **Rental period** | The time between the start of a rental and its due date. |
| **Rental line item** | One line of a rental: the item, the rental period, the rental fee and the deposit. |
| **Reorder threshold** | Stock level below which a product must be reordered (see BR-09). |
| **Return** | Transaction in which a customer brings back a purchased item and receives a refund. |
| **Sale** | Transaction in which a customer buys one or more items and pays for them. |
| **Sale line item** | One line of a sale: a product description, the quantity and the line subtotal. |
| **Stock level** | Number of units of a product currently in the store. |
| **Store manager** | Employee responsible for the store, who can approve exceptions (for example, price changes). |
| **Subtotal** | Sum of all line item amounts in a transaction, before tax. |
| **Tax** | Amount added to a transaction according to tax law, calculated by the Tax Calculator. |
| **Tax Calculator** | External system that calculates the tax for a transaction. |
| **Tender** | The form of payment used by the customer: cash, credit card or check. Synonym: *payment method*. |
| **Total** | Amount the customer must pay: subtotal plus tax (plus deposits, for rentals). |
| **Transaction** | General term for a sale, a return or a rental. |

## 3. Business rules

**Source** shows where a rule comes from: *Given* means it is stated in the case or the task plan; *Proposed* means the team still has to confirm it.

| ID | Category | Rule | Source |
| --- | --- | --- | --- |
| BR-01 | Tax | The tax of every transaction is calculated by the Tax Calculator according to the current tax law. | Given |
| BR-02 | Tax | If the Tax Calculator is unavailable, a default tax rate is applied and the transaction is flagged for later correction. | Proposed |
| BR-03 | Price | The price of an item is the price in its product description at the moment it is entered. Later price changes do not affect completed transactions. | Proposed |
| BR-04 | Price | Only a store manager may change a product's price or approve a manual price override at the register. | Proposed |
| BR-05 | Payment | A credit card payment must be authorized by the Payment Service before the transaction is completed. | Proposed |
| BR-06 | Payment | For cash payments, the amount tendered must be at least the total; the change due is the amount tendered minus the total. | Proposed |
| BR-07 | Return | A refund is given only for an item with a valid receipt, returned within the refund period. | Given (period: see open questions) |
| BR-08 | Return | A refund is paid with the same tender used in the original sale. | Proposed |
| BR-09 | Inventory | When the stock level of a product falls below 10 units, the product must be reordered. | Given |
| BR-10 | Rental | Every rental requires a deposit. The deposit is refunded when the item is returned undamaged. | Given (amount: see open questions) |
| BR-11 | Rental | Only an item with status *Available* can be rented. A *Rented* item cannot be sold or rented again until it is returned. | Proposed |
| BR-12 | Rental | A customer with an overdue rental cannot start a new rental. | Proposed |
| BR-13 | Staff | Every transaction is linked to the cashier of the current cashier session. | Proposed |
| BR-14 | Accounting | Every completed sale, return and rental is reported to the Accounting System. | Proposed |

## 4. Open questions

Source checked so far: project proposal (W01). The full case study has not yet been checked.


1. What is the **refund period** for returns (BR-07)?
2. How is the **deposit amount** set: fixed, or a percentage of the item value (BR-10)?
3. What is the **maximum rental period**, and is there a **late fee**? If so, how is it calculated?
4. The proposal lists **3 payment methods**; the third is assumed to be **check**. Confirm against the case.
5. Do **rented items** count toward the stock level for the reorder threshold (BR-09)?
6. Are there **discounts or promotions** that need their own price rules?
7. Does the Accounting System receive the **deposit**, or only the rental fee (BR-14)?

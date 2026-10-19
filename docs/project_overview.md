# NewEra POS – Project Overview

> Software Engineering · Beihang University (BUAA) · Team D · September 2026
>
> This page summarizes the project proposal presented in Week 1.
> The full slides are in [`docs/release/project_proposal.pdf`](release/project_proposal.pdf).

## 1. The problem

A retail store has to handle many everyday operations at the till: recording what a customer buys, calculating totals and taxes, taking payment, updating the stock and giving a receipt. The store also has to handle customers who bring items back and customers who rent equipment instead of buying it.

Done by hand, or with disconnected tools, these operations are slow and error-prone. They also have to be reported correctly to other parts of the business (payment authorization, taxes, accounting, HR).

**NewEra POS** is the point-of-sale application that supports the cashier in all of these tasks from a single terminal.

## 2. The users

| Role | Type | Description |
|---|---|---|
| **Cashier** | Primary actor | Operates the POS terminal and takes part in every use case. |
| **Customer** | Actor / stakeholder | Purchases, returns or rents items and pays for them. |

A more detailed list of stakeholders and a persona of the cashier are in [`requirements/stakeholders.md`](requirements/stakeholders.md).

## 3. The scope

### What the system does

NewEra POS lets the cashier record a customer's purchase, calculate totals and taxes, take payment, update the inventory and print a receipt. It also processes returns and equipment rentals.

### Use cases

| # | Use case | Short description |
|---|---|---|
| UC1 | **Process Sale** | Register the items a customer buys, calculate the total and taxes, take payment, print the receipt. |
| UC2 | **Handle Returns** | Process items that a customer brings back. |
| UC3 | **Process Rental** | Process the rental of equipment to a customer. |
| UC4 | **Start Up** | Start the POS system so that it is ready for the cashier. |

### External systems

| System | Role |
|---|---|
| **Payment Authorization Service** | Authorizes card payments. |
| **Tax Calculator** | Calculates the taxes of a sale. |
| **Accounting System** | Receives the accounting information of the transactions. |
| **HR System** | Provides employee (cashier) information. |

### Payment methods

The proposal lists the payment methods **cash** and **credit card**.

### Out of scope

Anything not listed above is outside the current scope. The scope will be refined and confirmed in the SRS (`docs/requirements/SRS.md`).

## 4. Why this case

| Reason | Explanation |
|---|---|
| **A proven teaching case** | It is the same case study used at UPM to teach object-oriented analysis and design. It is well tested and documented across a full course. |
| **Focus on the process** | Requirements, actors and business rules are already defined, so our effort goes into learning the software engineering process and not into inventing a domain. |
| **Full lifecycle coverage** | It touches every phase of the course: requirements, use cases, domain modeling, contracts, design diagrams and a design class diagram. |
| **Realistic complexity** | One primary actor, a customer and four external systems (payment authorization, taxes, accounting, HR) make it complex enough to be interesting. |

## 5. Related documents

- Project proposal slides: [`release/project_proposal.pdf`](release/project_proposal.pdf)
- Project plan: [`../plans/project_plan.md`](../plans/project_plan.md)
- Process model: [`../plans/process_model.md`](../plans/process_model.md)
- Requirements: [`requirements/`](requirements/)

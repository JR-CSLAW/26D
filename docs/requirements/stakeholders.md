# Stakeholders and Users – NewEra POS

> Team D · Software Engineering, Beihang University (BUAA) · Week 6
> Author: Yasmine Chkoundali
>
> This document identifies the people and organizations interested in NewEra POS and describes the main user of the system, the cashier. It is an input for the elicitation plan ([`elicitation_plan.md`](elicitation_plan.md)) and for the SRS ([`SRS.md`](SRS.md)).

## 1. Stakeholders

A stakeholder is any person or group that is affected by the system or that can influence its requirements.

| Stakeholder | Role | Interest in the system |
|---|---|---|
| **Cashier** | Operates the POS terminal in every use case (sale, return, rental, start up). | Wants a fast, simple and reliable system that is easy to learn and does not slow down the queue. Wants few errors and clear messages when something goes wrong. |
| **Customer** | Buys, returns or rents items and pays for them. | Wants a short wait at the till, correct prices and taxes, a choice of payment methods, and a correct receipt. Wants the payment to be secure. |
| **Store manager** | Runs the store day to day and supervises the cashiers. | Wants accurate sales, returns and rental records, correct stock levels, and control over price and refund rules. Wants the store to run without interruptions. |
| **Owner** | Owns the business and decides its investments. | Wants the system to increase sales and reduce losses and errors at a reasonable cost. Wants reliable figures about the performance of the store. |
| **Accountant** | Manages the financial records of the store. | Wants every transaction (sales, returns, rentals, taxes) sent correctly to the accounting system, so that the accounts are accurate and consistent. |
| **HR** | Manages the store employees. | Wants the system to identify the cashiers correctly, using the information in the HR system, and to link each transaction to the employee who made it. |
| **System administrator** | Installs, configures and maintains the system. | Wants a system that is easy to install, configure and maintain, with clear logs, and with reliable connections to the external systems (payment authorization, tax calculator, accounting, HR). |

## 2. User characteristics: the cashier

The cashier is the primary actor of NewEra POS and takes part in every use case. The persona below is **fictional**. It is based on our assumptions about a typical cashier and will be checked and corrected with the interviews and the observation described in the elicitation plan.

### Persona: Li Wei, cashier

| | |
|---|---|
| **Role** | Cashier in a retail store that sells products and also rents equipment |
| **Age** | 24 |
| **Education** | High school |
| **Experience** | 2 years of work as a cashier |
| **Technology skills** | Uses a smartphone every day and is comfortable with simple applications. Is not an IT specialist and has had little formal training on software. |

**Working environment**
- Works at a till in a store with a customer queue, noise and frequent interruptions.
- Uses the POS terminal with a screen, a barcode scanner, a receipt printer and a cash drawer.
- Works standing for long shifts and often needs to use the system while talking to the customer.
- Needs to follow the store rules for prices, returns and rental deposits.

**Peak hours**
- Lunch time, evenings after work, and weekends.
- During peaks the cashier serves many customers in a row, so every second saved per sale matters.
- Start up of the system happens at the beginning of the shift, often under time pressure before the store opens.

**Goals**
- Serve each customer quickly and correctly.
- Avoid mistakes in prices, taxes and change.
- Handle returns and rentals without asking the manager for help each time.

**Frustrations**
- A slow system or a system that freezes while customers are waiting.
- Confusing screens, or too many steps to register a simple sale.
- Unclear error messages, for example when a payment is refused or the tax service is not available.

**Implications for the requirements**
- **Usability:** a simple screen, few steps per task, and clear messages, because the cashier has little time and no IT training.
- **Performance:** quick registration of sale lines and a quick response during peak hours.
- **Reliability:** the system must keep working, or recover clearly, when an external system is not available.
- **Learnability:** a new cashier should be able to use the system after a short introduction.

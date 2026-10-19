# Elicitation Plan – NewEra POS

> Team D · Software Engineering, Beihang University (BUAA) · Week 6
> Author: Yasmine Chkoundali
>
> This document explains how the team will collect the requirements of NewEra POS: which techniques we use, why, and which questions we ask the main users. The people we want to hear from are described in [`stakeholders.md`](stakeholders.md).

## 1. Goals of the elicitation

- Understand how a cashier works today with sales, returns and rentals.
- Find the needs of the store manager, who controls the rules and the records.
- Check the assumptions we made in the cashier persona.
- Collect the functional and non-functional requirements and the business rules that will go into the SRS.

## 2. Techniques

| Technique | What we do | Why we use it | Main stakeholders | Limits |
|---|---|---|---|---|
| **Interview** | Talk one to one with a cashier and a store manager, using the questions in section 3. | Gives detailed and honest answers, and allows follow-up questions. Good to understand needs, problems and business rules. | Cashier, store manager | Takes time. Answers depend on the person and may not cover everything. |
| **Questionnaire** | Send a short list of mostly closed questions to several cashiers or store staff. | Reaches more people quickly and gives data we can compare, for example about the payment methods used or the peak hours. | Cashier, store manager, customer | Little detail. No chance to ask follow-up questions. |
| **Observation** | Watch a real shop till during a normal period and a busy period, and note each step of a sale, a return and a rental. | Shows what people really do, including things they forget to say. Good to find usability problems and the real speed needed at peak hours. | Cashier, customer | Needs the permission of the store. The behavior of people can change when they know they are observed. |
| **Document analysis** | Read the case study documents and the information about the external systems (payment authorization, tax calculator, accounting, HR) and the store rules. | Fast and cheap. Gives the first list of use cases, actors and business rules before we meet any user. | Accountant, HR, system administrator | Documents can be incomplete or out of date, so we must confirm them with people. |

### How the techniques work together

1. **Document analysis** first, to prepare ourselves and to avoid asking questions that the case documents already answer.
2. **Interviews** next, to understand the needs and the business rules in detail.
3. **Observation** of a real till, to compare what people say with what they do.
4. **Questionnaire** last, to check the main findings with more people.

The results of each step go into the SRS and are checked again by the team during the review of the requirements.

## 3. Interview questions

The questions are open, so the person can explain in their own words. We take notes and, if the person agrees, we record the interview. We do not collect personal data other than the role of the person.

### 3.1 Cashier (7 questions)

1. Can you describe a normal sale from the moment the customer arrives at the till to the moment they leave?
2. Which steps of the sale take the most time or cause the most mistakes?
3. How do you handle a return? What do you check before you accept an item back?
4. How do you handle the rental of equipment? What information do you need from the customer, and what happens with the deposit?
5. Which payment methods do customers use most, and what do you do when a payment is refused?
6. What happens when the system is slow or not available? What do you do at that moment?
7. What would make your work at the till easier? What do you dislike in the system you use now?

### 3.2 Store manager (7 questions)

1. What do you need the system to record for every sale, return and rental?
2. Which rules must the system apply, for example about prices, discounts, taxes and refunds?
3. How do you check the stock, and what do you do when a product is running low?
4. Who is allowed to do special operations, for example cancel a sale or approve a return, and how do you control them?
5. What reports or information do you need at the end of the day or the end of the month?
6. How do the sales data reach the accountant, and how do you identify the cashier who made each transaction?
7. What are the biggest problems or risks you have had with a POS system, for example errors in the accounts or cash differences?

## 4. After the elicitation

- Each interview is summarized in a short note and shared with the team.
- Every finding is converted into a requirement, a business rule or an open question.
- Open questions are listed and checked with the user in a second short meeting or by message.
- The requirements follow the conventions defined by the team in [`requirements_conventions.md`](requirements_conventions.md).

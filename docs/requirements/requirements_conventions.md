# Requirements Conventions

This document defines the rules and conventions the team will follow for writing, prioritizing, and tracing requirements for the NewEra POS system.

## 1. Requirement ID Scheme
Every requirement must have a unique identifier based on its category:
- **FR-xx:** Functional Requirements (for example, FR-01: Process a sale).
- **NFR-xx:** Non-Functional Requirements (for example, NFR-01: The system must process a sale in < 1 second).
- **BR-xx:** Business Rules (for example, BR-01: Taxes are calculated based on the store's location).
- **IR-xx:** Interface Requirements (for example, IR-01: The POS must connect to the Payment Gateway API).

## 2. Priority (MoSCoW Method)
Requirements will be prioritized using the MoSCoW method to help the team focus on what is essential for the MVP (Minimum Viable Product):
- **Must have:** Critical for the system to work (for example, processing a sale). Without it, the product is useless.
- **Should have:** Important but not critical. Can be worked around if needed (for example, generating a daily sales report).
- **Could have:** Nice to have. Only implemented if there is spare time (for example, changing the UI theme).
- **Won't have:** Explicitly out of scope for this release (for example, a mobile app version).

## 3. Rules for Writing Good Requirements
To ensure quality, every requirement must be:
- **Unambiguous:** It can only be interpreted in one way. Avoid vague words like "fast", "user-friendly", or "etc."
- **Verifiable:** It can be tested. If you cannot design a test for it, it's not a good requirement.
- **Consistent:** It does not contradict another requirement.
- **Complete:** It contains all the necessary information to be understood and implemented.

### Examples (Good vs. Bad)
- **Bad:** "The system must be fast." *(Ambiguous, not verifiable)*
- **Good:** "The system must process a standard sale transaction in less than 1 second." *(Measurable, verifiable)*

- **Bad:** "The cashier manages products." *(Incomplete, vague)*
- **Good:** "The cashier shall be able to search for a product using a barcode scanner and add it to the current sale." *(Complete, specific)*

## 4. Traceability Matrix Template
To ensure every requirement is fulfilled and tested, we will use this traceability matrix. Below is an example of how to fill it:

| Req ID | Requirement Summary | Use Case | Design (UML/UI) | Test Case |
| :--- | :--- | :--- | :--- | :--- |
| FR-01 | Process a sale | UC1 (Process Sale) | Class Diagram: Sale, SaleLineItem | TC-01: Register item and pay |
| NFR-01 | Fast checkout | UC1 (Process Sale) | UI: Optimized layout | TC-02: Time processing < 1s |
| BR-01 | Tax calculation | UC1 (Process Sale) | Component: TaxCalculator | TC-03: Calculate 21% VAT |
| FR-xx | *(Empty for now)* | *(Empty for now)* | *(Empty for now)* | *(Empty for now)* |

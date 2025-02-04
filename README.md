# Test Automation Paradigm

## Overview
UI, API, and Functional tests are structured around the application's functional modules. A **functional module** represents a logically complete feature used by the end user. A **business scenario** (or business flow) defines the sequence of user actions that interact with a functional module. These test types require periodic reviews and updates to align with evolving business requirements.

In contrast, **Unit Tests** are organized around the application's code architecture. They aim to cover as much backend logic as possible and typically require updates only when technical requirements change due to modifications in business needs.

---

## Test Types and Their Differences

The distinction between various test types lies in how they trigger the backend logic:

1. **UI Tests**: Interact with the application's front end (FE). Follow business scenarious.
2. **API Tests**: Make direct calls to the relevant API endpoints. May follow business scenarious, but more focused on isolated API's.
3. **Functional Tests**: Directly call relevant methods (requires access to the application's code). Follow business scenarious.
4. **Unit Tests**: Test the smallest logical pieces of code, such as individual methods.

---

## Test Pyramid

The sequence of these test types aligns with the **test pyramid**:

- **UI and API Tests** are at the top and should be the least numerous and represent the **external Black box** testing layer.
- **Functional Tests** go right after, and sit in the middle. Represent **internal White Box** testing layer. 
- **Unit Tests** form the base and should be the most numerous, representing together with **Functional tests** the **internal White box** testing layer.


### Key Principle:
An efficient test framework ensures that **Unit Tests** significantly outnumber **Functional** or **UI/API Tests**, maintaining a **balanced and scalable testing strategy**.

---

## Benefits of Following the Test Pyramid
- **Sustainable Test Maintenance**: Ensures long-term cost efficiency by preserving the value of invested resources and preventing test suite degradation, safeguarding the business investment.
- **Fast and Comprehensive Feedback**: Enables a quick and exhaustive testing feedback cycle.
- **Lower Maintenance Overhead**: Minimizes upkeep by reducing the number of **business flow-oriented** tests.
- **Scalability and Reliability**: Ensures a stable and scalable test framework through a balanced distribution of test types.
- **Alignment with Business Logic**: Creates a test framework that accurately represents and validates the underlying business knowledge.


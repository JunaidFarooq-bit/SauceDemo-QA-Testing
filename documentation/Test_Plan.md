# SOFTWARE TEST PLAN
## SauceDemo – E-commerce Web Application

| Document Information | Details |
|---|---|
| Document ID | STP-SD-001 |
| Project Name | SauceDemo QA Testing |
| Document Type | Software Test Plan |
| Version | 1.0 |
| Prepared By | Junaid Farooq |
| Role | Software QA Engineer (Independent Project) |
| Application | SauceDemo (Swag Labs) |
| Application URL | https://www.saucedemo.com/ |
| Status | Initial Draft |

---

# 1. Introduction

## 1.1 Purpose

The purpose of this Software Test Plan is to define the testing approach, scope, objectives, resources, testing activities, and deliverables for the SauceDemo e-commerce web application.

This project aims to evaluate the application's functional behaviour, identify defects, validate critical user workflows, and assess application reliability through manual and automated testing.

The project will be conducted as an independent Software Quality Assurance portfolio project.

## 1.2 Project Overview

SauceDemo is a demonstration e-commerce web application that simulates an online shopping experience.

Users can authenticate, browse products, sort inventory, add products to a shopping cart, proceed through checkout, and complete a simulated purchase.

The application provides an opportunity to practice real-world software testing methodologies and automation techniques.

## 1.3 Testing Objectives

The primary objectives are:

- Verify that users can successfully log in using valid credentials.
- Validate authentication behaviour with invalid credentials.
- Ensure product information is displayed correctly.
- Verify product sorting functionality.
- Validate shopping cart operations.
- Ensure checkout forms perform appropriate validation.
- Verify order completion and confirmation.
- Identify and document functional defects.
- Develop reusable automated test scripts.
- Establish a regression testing suite.
- Evaluate application behaviour across supported browser environments.

# 2. Scope of Testing

## 2.1 In-Scope Features

The following application modules will be tested.

### A. Authentication Module
- Login with valid credentials.
- Login with invalid credentials.
- Login with missing username or password.
- Validation of error messages.
- Logout functionality.
- Behaviour of different available demo user accounts.

### B. Product Inventory Module
- Product listing and visibility.
- Product names and descriptions.
- Product prices.
- Product sorting by name.
- Product sorting by price.
- Product availability and displayed information.

### C. Shopping Cart Module
- Adding products to the cart.
- Removing products from the cart.
- Cart item count.
- Cart contents validation.
- Navigation between inventory and cart.
- Cart state consistency.

### D. Checkout Module
- Checkout navigation.
- Customer information form validation.
- Required field validation.
- Checkout with valid information.
- Checkout overview.
- Product and price verification.
- Item total and displayed totals.

### E. Order Completion Module
- Completing the simulated purchase.
- Order confirmation message.
- Confirmation page navigation.
- Returning to the inventory page.

### F. Session Management
- Logout functionality.
- Navigation after logout.
- Session behaviour.
- Access to restricted pages after logout.

## 2.2 Out-of-Scope Features

The following activities are excluded from this project:

- Real payment gateway integration.
- Actual financial transactions.
- Production database testing.
- Backend source-code testing.
- Security penetration testing.
- High-volume load and stress testing against the public demo.
- Testing undocumented backend services.

# 3. Testing Strategy

The project will use a combination of manual and automated testing methodologies.

## 3.1 Manual Testing

Manual testing will be performed to validate application functionality and identify unexpected behaviour.

Activities include:

- Functional testing.
- Exploratory testing.
- Negative testing.
- Boundary value analysis.
- UI validation.
- Regression testing.
- User workflow testing.

## 3.2 Automation Testing

UI automation will be implemented using Python, Playwright, and pytest.

Automation objectives:

- Automate frequently used application workflows.
- Create reusable test components.
- Implement the Page Object Model (POM).
- Validate expected application behaviour.
- Capture screenshots when automated tests fail.
- Generate automated test execution reports.

## 3.3 Regression Testing

Regression testing will verify that previously working functionality continues to work after changes or fixes.

Critical workflows to include:

- User login.
- Product sorting.
- Add and remove cart items.
- Checkout validation.
- Order completion.
- Logout.

## 3.4 Negative Testing

Negative testing will evaluate application behaviour when users provide invalid, incomplete, or unexpected inputs.

Examples:

- Invalid login credentials.
- Empty login fields.
- Missing checkout information.
- Invalid input formats.
- Unexpected navigation sequences.
- Attempts to access restricted pages.

# 4. Test Environment

## 4.1 Application Environment

| Component | Configuration |
|---|---|
| Application | SauceDemo |
| URL | https://www.saucedemo.com/ |
| Environment | Public Demo |
| Operating System | Windows |
| Browser | Google Chrome |
| Testing Type | Manual and Automation |

## 4.2 Testing Tools

| Tool | Purpose |
|---|---|
| Python | Automation programming language |
| Playwright | Browser automation |
| pytest | Test execution and organization |
| Postman | API exploration where applicable |
| Git | Version control |
| GitHub | Project repository and documentation |
| Excel | Manual test case management |
| Jira-style defect reports | Defect documentation |

## 4.3 Automation Framework

The automation framework will follow a modular structure using:

- Page Object Model (POM).
- Reusable functions.
- pytest fixtures.
- Test data management.
- Assertions and validations.
- Screenshot capture on failure.
- HTML test reports.

# 5. Test Design and Execution

## 5.1 Test Case Design Techniques

The following techniques will be used:

**Equivalence Partitioning:** Dividing input data into valid and invalid groups.

**Boundary Value Analysis:** Testing values at and around input boundaries.

**Decision Table Testing:** Evaluating combinations of input conditions and expected results where applicable.

**Error Guessing:** Designing tests based on common application failure scenarios.

**Exploratory Testing:** Investigating application behaviour without relying exclusively on predefined test cases.

## 5.2 Test Execution Process

Each test case will be executed against the application.

The actual result will be compared with the expected result.

Each test case will receive one of the following statuses:

- PASS: Actual result matches expected result.
- FAIL: Actual result differs from expected result.
- BLOCKED: Testing cannot proceed because of an issue or dependency.
- NOT EXECUTED: Test has not yet been performed.

## 5.3 Test Case Identification

Test cases will follow a standardized naming convention.

Examples:

- TC_LOGIN_001
- TC_INVENTORY_001
- TC_CART_001
- TC_CHECKOUT_001
- TC_ORDER_001
- TC_SESSION_001

# 6. Entry and Exit Criteria

## 6.1 Entry Criteria

Testing may begin when:

- The application is accessible.
- Required demo credentials are available.
- The test environment is configured.
- Test scenarios have been identified.
- Test documentation has been prepared.

## 6.2 Exit Criteria

Testing will be considered complete when:

- All planned test cases have been executed or their status documented.
- Critical application workflows have been validated.
- All identified defects have been documented.
- Automated test scripts have been implemented and executed.
- Regression testing has been completed.
- Test execution results have been summarized.
- Final test documentation has been prepared.

Unresolved defects and blocked tests must be clearly reported rather than treated as successful.

# 7. Test Deliverables

The following deliverables will be produced during the project.

| Deliverable | Description |
|---|---|
| Software Test Plan | Testing scope and strategy |
| Test Scenarios | High-level testing scenarios |
| Test Cases | Detailed manual test cases |
| Bug Reports | Identified defects and evidence |
| Automation Scripts | Playwright test scripts |
| Automation Framework | Reusable POM-based structure |
| Test Execution Report | Execution results |
| Regression Suite | Reusable regression tests |
| Final Test Summary | Overall testing outcome |

# 8. Defect Management

All identified defects will be documented with sufficient information for investigation and reproduction.

## 8.1 Defect Report Fields

Each defect report will contain:

- Defect ID.
- Defect title.
- Application module.
- Environment.
- Preconditions.
- Steps to reproduce.
- Expected result.
- Actual result.
- Severity.
- Priority.
- Screenshots or supporting evidence.
- Current status.

## 8.2 Defect Severity

| Severity | Description |
|---|---|
| Critical | Major functionality unavailable or severe impact |
| High | Important functionality significantly affected |
| Medium | Partial functionality affected |
| Low | Minor UI or usability issue |

Defects will be classified based on their actual impact, not simply because a test failed.

# 9. Risks and Mitigation

| Risk | Mitigation |
|---|---|
| Public demo availability | Perform testing when the application is accessible |
| Changes to demo application | Revalidate test data and selectors |
| Dynamic application behaviour | Use stable locators and explicit waits |
| Test data inconsistencies | Use controlled and reusable test data |
| Browser compatibility issues | Document browser and environment details |
| Automation failures | Investigate whether failures originate from the application or test scripts |
| Shared demo data | Avoid relying on permanent application state |

# 10. Roles and Responsibilities

This is an independent QA project.

The project owner will perform the following responsibilities:

- Review application functionality.
- Prepare testing documentation.
- Design and execute manual test cases.
- Develop automation scripts.
- Identify and document defects.
- Perform regression testing.
- Maintain the GitHub repository.
- Prepare the final test execution report.

# 11. Project Schedule

The estimated project duration is four weeks.

| Phase | Activities | Estimated Duration |
|---|---|---|
| Phase 1 | Application exploration and test planning | 3 days |
| Phase 2 | Test scenarios and manual test cases | 5 days |
| Phase 3 | Manual execution and defect reporting | 4 days |
| Phase 4 | Playwright automation development | 7 days |
| Phase 5 | Regression testing and reporting | 3 days |
| Phase 6 | Documentation and GitHub publishing | 3 days |

The schedule may be adjusted depending on testing findings and implementation progress.

# 12. Final Approval

This document defines the initial testing approach for the SauceDemo independent QA portfolio project.

Any changes in scope, testing methodology, or project objectives will be reflected in subsequent document versions.

| Prepared By | Role | Version |
|---|---|---|
| Junaid Farooq | Independent QA Engineer | 1.0 |

---

**End of Document**
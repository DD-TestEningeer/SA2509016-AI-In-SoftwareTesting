# SA2509016-AI-In-SoftwareTesting

# Module 7: AI in Software Testing

This module provides step-by-step notes for QA learners with real-time examples and ChatGPT prompts.

---

## 📑 Index

1. [Understanding Power of Generative AI in Manual Testing](#1-understanding-power-of-generative-ai-in-manual-testing)
2. [Generating Test Plan for High-Level Requirement through AI](#2-generating-test-plan-for-high-level-requirement-through-ai)
3. [Generating UI, Integration, and Functional Test Cases through AI](#3-generating-ui-integration-and-functional-test-cases-through-ai)
4. [Generating Test Data through AI](#4-generating-test-data-through-ai)
5. [Generating Cucumber Feature Files and Step Definitions through AI](#5-generating-cucumber-feature-files-and-step-definitions-through-ai)
6. [Generating Defect Report through AI](#6-generating-defect-report-through-ai)
7. [Understanding AI Power Testing Tools](#7-understanding-ai-power-testing-tools)
8. [How to Achieve Codeless Automation Using AI Tools](#8-how-to-achieve-codeless-automation-using-ai-tools)
9. [Demo on End-to-End Complex Test Writing Using AI](#9-demo-on-end-to-end-complex-test-writing-using-ai)
10. [Future of AI in QA Space](#10-future-of-ai-in-qa-space)
11. [Understanding AI for API Testing](#11-understanding-ai-for-api-testing)
12. [Generating JSON Path Using Simple English](#12-generating-json-path-using-simple-english)
13. [Parsing Complex JSON Using AI](#13-parsing-complex-json-using-ai)
14. [Generating API Test Cases Using AI](#14-generating-api-test-cases-using-ai)
15. [Generating POJO Classes Using AI](#15-generating-pojo-classes-using-ai)
16. [Generating Rest Assured Script Using AI](#16-generating-rest-assured-script-using-ai)
17. [Generating Selenium Scripts with Java Using AI](#17-generating-selenium-scripts-with-java-using-ai)
18. [Generating Selenium Scripts with JavaScript Using AI](#18-generating-selenium-scripts-with-javascript-using-ai)
19. [Generating Playwright Scripts Using AI](#19-generating-playwright-scripts-using-ai)
20. [Generating Cypress Scripts Using AI](#20-generating-cypress-scripts-using-ai)
21. [Generating Self-Healing Locator in Automation with Healenium](#21-generating-self-healing-locator-in-automation-with-healenium)
22. [Q&A Hands-on Exercises](#22-qa-hands-on-exercises-for-ai-in-software-testing)

---

# 1. Understanding Power of Generative AI in Manual Testing

- **Concept**: Generative AI can **understand human language requirements** and convert them into structured test ideas.
- **Why useful?** QA doesn’t need to spend hours brainstorming. AI provides quick draft test coverage.

## Real-Time Example
Requirement:

> “Login should allow valid users and reject invalid ones.”

AI Output (Manual Test Cases):

1. Login with valid username & password → **Dashboard displayed**.
2. Login with invalid username & valid password → **Error message displayed**.
3. Login with valid username & invalid password → **Error message displayed**.
4. Login with empty fields → **Validation message displayed**.

## ChatGPT Prompt Example for QA
👉 _“Generate manual test cases for login functionality that handles valid and invalid users including empty field validation.”_

# 2. Generating Test Plan for High-Level Requirement through AI

- **Concept**: AI can generate a **complete Test Plan** document from a single requirement.
- **Structure AI Generates**:

  - Scope
  - Objectives
  - Test Environment
  - Entry/Exit Criteria
  - Deliverables
  - Risks

## Real-Time Example
Requirement:

> “Build an e-commerce cart system where users can add, remove, and checkout products.”

AI Generated Test Plan (Short Draft):

- **Scope**: Validate cart operations, discounts, checkout, and payment.
- **Objectives**: Ensure product addition/removal works, totals update, checkout process is smooth.
- **Environment**: Chrome v120+, Windows 11, MySQL DB.
- **Risks**: Payment gateway downtime, network latency.
- **Deliverables**: Test Cases, Bug Reports, Automation Scripts.

## ChatGPT Prompt Example for QA
👉 _“Generate a complete test plan for an e-commerce cart system with add, remove, and checkout product functionality including scope, objectives, environment, risks, and deliverables.”_

# 3. Generating UI, Integration, and Functional Test Cases through AI

- **Concept**: From a single requirement, AI generates **multiple categories of tests**: UI, Integration, and Functional.

## Real-Time Example
Requirement:

> “User should be able to reset password via email.”

AI Output:

- **UI Tests**:
  1. Verify “Forgot Password” link is visible on login page.
  2. Verify reset password form has email input.

- **Integration Tests**:
  1. Verify reset request triggers an email to registered user.
  2. Verify reset email contains unique link/token.

- **Functional Tests**:
  1. Verify user can log in with new password.
  2. Verify old password doesn’t work after reset.

## ChatGPT Prompt Example for QA
👉 _“Generate UI, integration, and functional test cases for a reset password feature via email.”_


# 4. Generating Test Data through AI

- **Concept**: AI can instantly produce test data including **valid, invalid, and boundary cases**.
- **Why useful?** Reduces manual effort and ensures comprehensive test coverage.

## Real-Time Example
Requirement:

> “System should validate email addresses.”

AI Output (Generated Test Data):

- **Valid**:
  - [test123@gmail.com](mailto:test123@gmail.com)
  - [user.name@company.com](mailto:user.name@company.com)
  - [qa.engineer@org.co.in](mailto:qa.engineer@org.co.in)

- **Invalid**:
  - test123@ (missing domain)
  - @gmail.com (missing username)
  - user@@gmail.com (double @ symbol)

- **Boundary Data**:
  - Very long email ID (255 characters)

## ChatGPT Prompt Example for QA
👉 _“Generate valid, invalid, and boundary email addresses for testing email validation functionality.”_


# 5. Generating Cucumber Feature Files and Step Definitions through AI

- **Concept**: AI can generate **BDD test cases** in Gherkin format and step definitions in Java or JavaScript.
- **Why useful?** Saves time writing repetitive boilerplate code and ensures consistent test structure.

## Real-Time Example
Requirement:

> “Verify login with valid credentials.”

### AI Output (Feature File):

```gherkin
Feature: Login functionality

  Scenario: Successful login
    Given user is on login page
    When user enters valid username and password
    Then user should be redirected to dashboard
````

### AI Output (Java Step Definition):

```java
@Given("user is on login page")
public void user_is_on_login_page() {
   driver.get("https://example.com/login");
}

@When("user enters valid username and password")
public void user_enters_valid_credentials() {
   driver.findElement(By.id("username")).sendKeys("testUser");
   driver.findElement(By.id("password")).sendKeys("testPass");
   driver.findElement(By.id("login")).click();
}

@Then("user should be redirected to dashboard")
public void user_should_be_redirected_to_dashboard() {
   assertTrue(driver.getTitle().contains("Dashboard"));
}
```

## ChatGPT Prompt Example for QA

👉 *“Generate a Cucumber feature file and Java step definitions for login functionality where a valid user should successfully log in.”*



# 6. Generating Defect Report through AI

- **Concept**: QA can feed AI the bug scenario, and AI outputs a **structured defect report**.
- **Why useful?** Reduces manual effort in documenting detailed defect reports.

## Real-Time Example
Bug: App crashes when clicking on Profile Picture.

### AI Output (Bug Report):

- **Title**: App crashes on clicking profile picture.
- **Steps to Reproduce**:
  1. Login to app
  2. Go to dashboard
  3. Click profile picture
- **Expected Result**: Profile dropdown should appear.
- **Actual Result**: App crashes.
- **Severity**: High
- **Priority**: P1

## ChatGPT Prompt Example for QA
👉 _“Create a detailed defect report for an issue where the app crashes when clicking on the profile picture in the dashboard.”_


# 7. Understanding AI Power Testing Tools

- **Concept**: Several AI-powered tools exist for QA to **speed up test authoring and execution**.
- **Why useful?** Helps testers create reliable tests faster with minimal coding effort.

## Examples of AI Testing Tools

- **Testim** → AI-based locator handling.
- **Mabl** → Generates end-to-end tests using natural language.
- **Functionize** → AI-driven, codeless automation.

## Real-Time Example
Requirement: Test login page without writing code.

- In **Functionize**: Type in plain English →  
  _“Login with user [test@test.com](mailto:test@test.com) and password test123”_  
- AI generates test steps automatically.

## ChatGPT Prompt Example for QA
👉 _“List the top 5 AI-powered testing tools with their key feature and real-world use case.”_


# 8. How to Achieve Codeless Automation Using AI Tools

- **Concept**: AI tools allow testers to create automation scripts **without writing code**.
- **Why useful?** Beginners or manual testers can contribute to automation without deep programming knowledge.

## Real-Time Example
Tool: **Mabl**

- QA types:  
  _“Open login page, enter email [test@gmail.com](mailto:test@gmail.com), enter password test@123, click login, verify dashboard loads.”_  
- Tool auto-converts instructions into a working test.

## ChatGPT Prompt Example for QA
👉 _“Generate a codeless automation test flow for verifying login using any AI-powered testing tool.”_


# 9. Demo on End-to-End Complex Test Writing Using AI

- **Concept**: AI can generate **multi-step test flows** across UI and backend.
- **Why useful?** Helps QA validate critical business workflows quickly and efficiently.

## Real-Time Example
Requirement:

> “Search for a product → Add to cart → Checkout → Make payment.”

### AI Output (Playwright JavaScript Example):

```javascript
test("E2E Shopping Flow", async ({ page }) => {
  await page.goto("https://demo-shop.com");
  await page.getByPlaceholder("Search").fill("Laptop");
  await page.getByRole("button", { name: "Search" }).click();
  await page.getByText("Laptop Pro 15").click();
  await page.getByRole("button", { name: "Add to cart" }).click();
  await page.getByRole("link", { name: "Cart" }).click();
  await page.getByRole("button", { name: "Checkout" }).click();
  await page.getByRole("button", { name: "Pay" }).click();
  await expect(page.getByText("Order Confirmed")).toBeVisible();
});
````

## ChatGPT Prompt Example for QA

👉 *“Generate an end-to-end Playwright test script for an e-commerce flow: search product, add to cart, checkout, and complete payment.”*


# 10. Future of AI in QA Space

- **Concept**: AI will play a bigger role in automation stability, coverage, and predictive testing.

## Future Trends

- **Self-healing tests** → Fix broken locators automatically.
- **AI-driven coverage analysis** → Suggests missing test cases.
- **AI in CI/CD** → Auto-triggers relevant regression suite.

## Real-Time Example

- Locators keep breaking after every UI update → Healenium auto-heals them.
- AI bots in Jenkins decide which smoke tests to run first.

## ChatGPT Prompt Example for QA
👉 _“Explain how AI will shape the future of software testing with examples of self-healing, predictive analytics, and CI/CD integration.”_

# 11. Understanding AI for API Testing

- **Concept**: AI can generate **API test cases, Postman scripts, and validations**.
- **Why useful?** Even manual testers can test APIs without deep coding knowledge.

## Real-Time Example
Requirement:

> “Test GET /users API.”

AI Output (Test Cases):

1. Verify response code = 200.
2. Verify response contains list of users.
3. Verify response time < 2s.
4. Verify email field format in response.

## ChatGPT Prompt Example for QA
👉 _“Generate API test cases for GET /users endpoint covering positive, negative, and boundary scenarios.”_


# 12. Generating JSON Path Using Simple English

## **Concept**
AI converts plain English queries into JSONPath expressions, making it easier to extract data from complex JSON structures without manual analysis.

## **Why Useful**
- Avoids manual digging through nested JSON structures.
- Saves time in API testing and data extraction.
- Even beginners can generate accurate JSONPaths quickly.

## **Real-Time Example**
JSON Response:
```json
{
  "users": [
    { "id": 1, "name": "Alice", "email": "alice@test.com" },
    { "id": 2, "name": "Bob", "email": "bob@test.com" }
  ]
}
```

Requirement:
> “Fetch the email of the first user.”

AI Generated JSONPath:
```jsonpath
$.users[0].email
```

## **Prompt Example for QA**
👉 _“Generate the JSONPath for extracting the email of the first user from a list of users in a JSON response.”_


# 13. Parsing Complex JSON Using AI

- **Concept**: AI can extract specific data from nested or complex JSON structures using JSONPath.

## Real-Time Example
JSON:

```json
{
  "orders": [
    {
      "id": 101,
      "items": [
        { "name": "Laptop", "price": 1200 },
        { "name": "Mouse", "price": 25 }
      ]
    }
  ]
}
````

QA asks:

> “Extract the price of the mouse.”

AI Output:

```jsonpath
$.orders[0].items[1].price
```

## ChatGPT Prompt Example for QA

👉 *“Generate the JSONPath for extracting the price of the mouse from the given JSON response.”*


# 14. Generating API Test Cases Using AI

- **Concept**: AI can generate **detailed API test cases** covering positive, negative, boundary, and security scenarios.

## Real-Time Example
Requirement:

> “Test POST /login API.”

AI Output:

- **Positive** → Valid username & password → 200 OK.
- **Negative** → Invalid password → 401 Unauthorized.
- **Boundary** → Empty username → 400 Bad Request.
- **Security** → SQL injection attempt → Proper error handling.

## ChatGPT Prompt Example for QA
👉 _“Generate detailed API test cases for POST /login endpoint with positive, negative, boundary, and security scenarios.”_

# 15. Generating POJO Classes Using AI

- **Concept**: AI can generate Java POJO classes from JSON responses to simplify API response handling.

## Real-Time Example
JSON:

```json
{ "id": 1, "name": "Alice", "email": "alice@test.com" }
````

AI Output (Java POJO):

```java
public class User {
   private int id;
   private String name;
   private String email;
   // getters and setters
}
```

## ChatGPT Prompt Example for QA

👉 *“Generate a Java POJO class for the following JSON response: { 'id': 1, 'name': 'Alice', 'email': '[alice@test.com](mailto:alice@test.com)' }”*


# 16. Generating Rest Assured Script Using AI

- **Concept**: AI can generate **API automation scripts** in Rest Assured for Java.

## Real-Time Example
Requirement:

> “Test GET /users API.”

AI Output (Java):

```java
given()
   .when()
   .get("/users")
   .then()
   .statusCode(200)
   .body("users.size()", greaterThan(0));
````

## ChatGPT Prompt Example for QA

👉 *“Generate a Rest Assured test script in Java to validate GET /users API returns status 200 and non-empty response.”*

```
```
# 17. Generating Selenium Scripts with Java Using AI

- **Concept**: AI can generate **Selenium WebDriver scripts in Java** for web automation.
- **Why useful?** Saves time writing repetitive code for UI testing.

## Real-Time Example
Requirement:

> “Login test for Gmail.”

AI Output (Java):

```java
WebDriver driver = new ChromeDriver();
driver.get("https://mail.google.com/");
driver.findElement(By.id("identifierId")).sendKeys("test@gmail.com");
driver.findElement(By.id("identifierNext")).click();
driver.findElement(By.name("password")).sendKeys("test@123");
driver.findElement(By.id("passwordNext")).click();
assertTrue(driver.getTitle().contains("Inbox"));
driver.quit();
````

## ChatGPT Prompt Example for QA

👉 *“Generate a Selenium WebDriver test script in Java for Gmail login flow.”*


# 18. Generating Selenium Scripts with JavaScript Using AI

- **Concept**: AI can generate **Selenium scripts in JavaScript** (e.g., WebDriverIO) for web automation.

## Real-Time Example
Requirement:

> “Login test for Gmail.”

AI Output (JavaScript with WebDriverIO):

```javascript
const { remote } = require("webdriverio");

(async () => {
  const browser = await remote({ capabilities: { browserName: "chrome" } });
  await browser.url("https://mail.google.com/");
  await browser.$("#identifierId").setValue("test@gmail.com");
  await browser.$("#identifierNext").click();
  await browser.$('[name="password"]').setValue("test@123");
  await browser.$("#passwordNext").click();
  const title = await browser.getTitle();
  console.assert(title.includes("Inbox"));
  await browser.deleteSession();
})();
````

## ChatGPT Prompt Example for QA

👉 *“Generate a Selenium test script in JavaScript (WebDriverIO) for Gmail login flow.”*



# 19. Generating Playwright Scripts Using AI

- **Concept**: AI can generate **Playwright scripts in JavaScript** for web automation.
- **Why useful?** Speeds up creation of end-to-end tests with modern frameworks.

## Real-Time Example
Requirement:

> “Check title after login.”

AI Output (Playwright JS):

```javascript
test("Login Test", async ({ page }) => {
  await page.goto("https://example.com/login");
  await page.fill("#username", "testUser");
  await page.fill("#password", "testPass");
  await page.click("#loginBtn");
  await expect(page).toHaveTitle(/Dashboard/);
});
````

## ChatGPT Prompt Example for QA

👉 *“Generate a Playwright JavaScript test script for login functionality where page title should contain Dashboard after login.”*



# 20. Generating Cypress Scripts Using AI

- **Concept**: AI can generate **Cypress scripts** for web automation and functional testing.
- **Why useful?** Quickly generates test scripts for modern frontend applications.

## Real-Time Example
Requirement:

> “Check product search in e-commerce app.”

AI Output (Cypress):

```javascript
describe("Product Search", () => {
  it("should search product", () => {
    cy.visit("https://demo-shop.com");
    cy.get("#search").type("Laptop{enter}");
    cy.contains("Laptop Pro 15").should("be.visible");
  });
});
````

## ChatGPT Prompt Example for QA

👉 *“Generate a Cypress test script to verify product search functionality in an e-commerce site.”*


# 21. Generating Self-Healing Locator in Automation with Healenium

- **Concept**: Healenium allows Selenium tests to **auto-heal broken locators**.
- **Why useful?** Reduces test failures caused by UI changes.

## Real-Time Example
Scenario:

- QA wrote a Selenium script with locator → `By.id("loginBtn")`.
- Developer changed ID to → `loginButtonNew`.
- Normally test fails ❌.
- With **Healenium**, test auto-heals ✅ by identifying updated locator.

AI Output (Java with Healenium):

```java
WebDriver driver = new ChromeDriver();
SelfHealingDriver shDriver = SelfHealingDriver.create(driver);

shDriver.get("https://example.com/login");
shDriver.findElement(By.id("loginBtn")).click();  // Auto-heals if ID changes
````

## ChatGPT Prompt Example for QA

👉 *“Generate a Selenium test script in Java using Healenium that auto-heals locator for login button if its ID changes.”*


# 22. (Q&A) Hands-on Exercises for AI in Software Testing

- **Concept**: Practical exercises to reinforce AI-assisted manual and automation testing skills.

## Hands-on Exercises

1. Use AI to generate **manual test cases** for a signup page.
2. Generate **API test cases** for `POST /register`.
3. Convert a requirement into a **Cucumber feature file**.
4. Generate **Selenium + Playwright scripts** for the same test.
5. Demonstrate how **Healenium heals a broken locator**.

## ChatGPT Prompt Example for QA
👉 _“Provide 5 hands-on exercises for QA beginners to practice AI in manual + automation testing with real examples.”_

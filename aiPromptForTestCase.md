# How to Write Effective Prompts for AI-Generated Test Cases

Creating a clear and detailed prompt is essential for leveraging AI to generate high-quality test cases. A well-structured prompt helps the AI understand the context, requirements, and expectations, resulting in more relevant and actionable test cases. This guide explains how QA professionals can build effective prompts, with practical examples and references to best practices from Academy TestRail.

---

## 1. Basic Feature Scope
- **Describe the feature or functionality to be tested.**
- Be specific about what the test should cover (e.g., login page, API endpoint).
- Example: "Login page for a web application."

## 2. Test Environment
- **Specify the environment where the test will run.**
- Include platform, application type, device, server, or browser details.
- Example: "Test on Chrome browser, Windows 10, staging server."

## 3. Core Functionalities and User Interactions
- **List the main actions and expected user interactions.**
- Include workflows, input fields, buttons, and navigation.
- Example: "User enters username and password, clicks 'Login', receives feedback."

## 4. Acceptance Criteria and Edge Cases
- **Define what constitutes a successful test.**
- Include business rules, validation requirements, and edge cases.
- Example: "Login succeeds with valid credentials, fails with invalid ones, handles empty fields."

## 5. Data Dependencies and System Integrations
- **Mention any required data, external systems, or integrations.**
- Specify test data, database state, or API dependencies.
- Example: "User must exist in the database; login API integrates with authentication service."

---

## Examples


### Example 1: Front-End Login Page Test Case Prompt
```
Feature Scope:
	- Test the login page of the "MyApp" web application, including all input fields, buttons, and error messages.
Test Environment:
	- Chrome browser (latest version), Windows 10, staging server (URL: https://staging.myapp.com/login).
Core Functionalities & User Interactions:
	- User enters username and password.
	- User clicks the 'Login' button.
	- System displays loading indicator during authentication.
	- User can use 'Forgot Password' link.
	- User can toggle password visibility.
Acceptance Criteria & Edge Cases:
	- Login succeeds with valid credentials and redirects to dashboard.
	- Login fails with invalid credentials and displays error message.
	- Empty username or password fields trigger validation errors.
	- Locked or disabled accounts show specific error messages.
	- Multiple failed attempts trigger account lockout warning.
	- Special characters and long input values are handled gracefully.
	- Accessibility: All elements are reachable via keyboard navigation.
Data Dependencies & System Integrations:
	- Test users must exist in the staging database with various account states (active, locked, disabled).
	- Login API integrates with authentication and logging services.
	- Email service integration for 'Forgot Password' flow.
	- Audit logs generated for each login attempt.
```

### Example 2: Back-End Internal API New Endpoint Test Case Prompt
```
Feature Scope:
	- Test the new POST /api/v2/users endpoint for creating user records in the internal HR system.
Test Environment:
	- REST API, staging server (api.staging.hr-internal.com), tested via Postman and automated scripts.
Core Functionalities & User Interactions:
	- API receives POST requests with JSON payload containing user details (name, email, role, department).
	- Validates required fields and data formats.
	- Creates new user record in the database.
	- Returns success response with user ID and details.
	- Handles authentication via internal token.
Acceptance Criteria & Edge Cases:
	- Success: Valid payload creates user and returns 201 status with user data.
	- Error: Missing or invalid fields return 400 with detailed error messages.
	- Duplicate email returns 409 conflict error.
	- Unauthorized requests return 401 error.
	- Large payloads and special characters are handled without crashing.
	- System logs all requests and responses for audit.
	- Integration: New user triggers notification to HR system and updates reporting dashboard.
Data Dependencies & System Integrations:
	- Requires connection to staging user database.
	- Integrates with authentication, notification, and reporting services.
	- Test data includes users with various roles and departments.
	- Simulate network failures and retry logic.
```

---

## Reference
- Content inspired by best practices from [Academy TestRail](https://academy.testrail.com/)

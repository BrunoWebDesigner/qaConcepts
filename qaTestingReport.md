# 📄 QA Testing Report

## Types of Issues

- **Error**: A situation where something goes wrong in the code or functionality, causing the system to fail.
- **Bug**: A flaw in the software that causes it to behave unexpectedly.
- **Defect**: A broader term that encompasses both errors and bugs, referring to unintended behavior or issues.

---

## Report Template

### Type

[Error / Bug / Defect]

### Description

A concise explanation of what went wrong (e.g., "When attempting to submit the signup form, the form does not submit and displays an error message").

### Expected Result

The correct behavior that should occur if the system works as intended (e.g., "The form should be submitted successfully without any errors, and the user should be redirected to the welcome page").

### Actual Result

A description of what actually happened when testing the form (e.g., "The form fails to submit and an error message appears stating 'Field X is missing' even though it is correctly filled out").

### How to Reproduce (Step-by-step)

1. Navigate to the signup page.
2. Fill out the form with valid information (e.g., name, email, password).
3. Leave the 'Phone Number' field empty.
4. Click the 'Submit' button.
5. Observe that the form does not submit and an error message is shown.

### Severity

(Optional, but useful for prioritizing): Low, Medium, High, Critical.

### Screenshot/Video (if applicable)

Attach any media that visually captures the issue.

---

## Example Bug Report

### Type: Bug

### Description:

When attempting to submit the signup form on the website, the form fails to submit, and an error message stating "Please fill out all required fields" is displayed. However, all fields have been filled out correctly.

✅ **Expected Result**:  
The form should be submitted successfully, and the user should be redirected to the welcome page.

⛔ **Actual Result**:  
The form does not submit and displays an error message that reads, "Please fill out all required fields" even though all required fields are filled out.

➡️ **How to Reproduce (Step-by-step)**:

1. Navigate to the signup page (URL: https://example.com/signup).
2. Fill in all the required fields: Name, Email, Password, etc.
3. Click the 'Submit' button.
4. Observe that the form does not submit and the error message appears stating, "Please fill out all required fields".

➡️ **Screenshot/Video**:  
[Screenshot Attached]

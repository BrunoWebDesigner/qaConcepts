# 25 Manual Testing Q&A for Beginners

*Document by Aston Cook. Reformatted, expanded, and annotated for clarity and practical understanding by [BrunoWebDesigner](https://github.com/BrunoWebDesigner). All core content and original credit to Aston Cook.*

---

These questions cover the core manual testing concepts that every beginner and those transitioning into software testing should know. Where helpful, each answer is elaborated with examples or practical notes.

---

## 1. What is manual testing?

**Answer:** Manual testing is the process of executing test cases manually—without using automation tools—to verify that an application behaves as expected.

*Example:* A tester clicks through a web application following written steps to ensure each feature works as described.

---

## 2. Why is manual testing important?

**Answer:** Manual testing validates usability, uncovers edge cases, and ensures overall quality before automation is introduced. It often catches issues that automation might miss, especially with user experience or visual elements.

*Example:* A manual tester may notice a confusing button label or color contrast issue that a script would ignore.

---

## 3. What are the different types of testing?

**Answer:**  
- **Unit Testing:** Checks individual components (usually automated).
- **Integration Testing:** Ensures combined components work together.
- **System Testing:** Validates the entire integrated application.
- **Acceptance Testing:** Confirms the system meets business requirements.
- **Regression Testing:** Verifies that new code changes haven’t broken existing functionality.
- **Smoke/Sanity Testing:** Quick checks for basic functionality (smoke) or bug fixes/features (sanity).

---

## 4. What is the difference between verification and validation?

**Answer:**  
- **Verification:** Are we building the product right? (Does it meet design specs?)
- **Validation:** Are we building the right product? (Does it meet user needs?)

*Example:*  
- Verification: Reviewing design documents for correctness.  
- Validation: User acceptance testing with real users.

---

## 5. What are functional vs. non-functional tests?

**Answer:**  
- **Functional tests:** Validate specific features or functions (e.g., login works).
- **Non-functional tests:** Cover aspects like performance, security, usability, and reliability.

*Example:*  
- Functional: Does submitting the form save data?  
- Non-functional: How fast is the page load time under heavy traffic?

---

## 6. What is a test case?

**Answer:** A test case is a documented set of steps, inputs, and expected results used to verify a particular aspect of software behavior.

*Example:*  
- Step 1: Enter valid email and password.  
- Step 2: Click Login.  
- Expected: User is redirected to dashboard.

---

## 7. What is a test plan?

**Answer:** A test plan is a document outlining the scope, objectives, approach, resources, and schedule of testing activities.

*Example:*  
A test plan may specify which features to test, testing methods, timelines, and who is responsible.

---

## 8. What is the difference between smoke and sanity testing?

**Answer:**  
- **Smoke testing:** Basic checks after a build to ensure critical functionality works.
- **Sanity testing:** Focused checks after bug fixes or new features to ensure changes work as expected.

*Example:*  
- Smoke: Can the app start?  
- Sanity: Was the 'reset password' bug really fixed?

---

## 9. What is regression testing?

**Answer:** Regression testing means re-executing existing tests after changes to ensure that new updates do not break existing functionality.

*Example:*  
After updating the payment module, testers re-run checkout tests to make sure nothing else broke.

---

## 10. What are positive and negative test cases?

**Answer:**  
- **Positive test cases:** Use valid input to verify correct behavior.
- **Negative test cases:** Use invalid input to ensure proper error handling.

*Example:*  
- Positive: Enter correct credentials—should log in.  
- Negative: Enter wrong password—should show an error.

---

## 11. What is exploratory testing?

**Answer:** Exploratory testing is unscripted, where testers actively explore the application to find issues not covered by written test cases.

*Example:*  
A tester tries unexpected workflows or inputs to see if the app crashes.

---

## 12. What is usability testing?

**Answer:** Usability testing checks how easily end-users can interact with the system, ensuring a smooth and intuitive experience.

*Example:*  
Observing real users as they try to sign up for an account—are they confused at any step?

---

## 13. What is boundary value analysis?

**Answer:** A black-box technique that tests values at the edges (boundaries) of input ranges.

*Example:*  
If age input must be 18–65: test with 17, 18, 65, and 66.

---

## 14. What is equivalence partitioning?

**Answer:** Divides inputs into ‘partitions’ (valid/invalid) to reduce the number of test cases.

*Example:*  
For an input range of 1–100, you might test one value from 1–100 (valid), and one below 1 and one above 100 (invalid).

---

## 15. What is the difference between severity and priority?

**Answer:**  
- **Severity:** Impact of a defect on the system.
- **Priority:** How soon the defect should be fixed.

*Example:*  
A typo in the footer (low severity, low priority).  
A crash on login (high severity, high priority).

---

## 16. What is defect life cycle?

**Answer:** The stages a defect passes through:  
New → Assigned → Open → Fixed → Retest → Verified → Closed

---

## 17. What is the difference between QA and QC?

**Answer:**  
- **QA (Quality Assurance):** Ensures quality processes (preventive).
- **QC (Quality Control):** Verifies the product through actual testing (detective).

---

## 18. What is an acceptance test?

**Answer:** A test performed by end-users to validate if the system meets business requirements.

*Example:*  
A client tests a new dashboard to confirm it meets their needs before go-live.

---

## 19. What is black-box vs. white-box testing?

**Answer:**  
- **Black-box:** Tests external behavior without knowing internal code.
- **White-box:** Tests internal logic, code paths, or structure.

*Example:*  
- Black-box: Tester enters data without seeing code.  
- White-box: Developer writes tests to cover every condition in the code.

---

## 20. What is ad-hoc testing?

**Answer:** Informal testing done without documentation to quickly find defects.

*Example:*  
Trying random inputs or operations to see if the app fails.

---

## 21. What is the difference between test scenario and test case?

**Answer:**  
- **Test Scenario:** Describes what to test (high-level).
- **Test Case:** Describes how to test (detailed steps).

*Example:*  
- Scenario: Test user registration.  
- Test Case: Steps for filling out the registration form, submitting, and verifying success.

---

## 22. What is defect clustering?

**Answer:** The principle that defects are often concentrated in a small number of modules.

*Example:*  
80% of bugs may be found in just 20% of the code.

---

## 23. What is the pesticide paradox in testing?

**Answer:** Running the same test cases repeatedly finds fewer new bugs. To stay effective, test cases must be updated regularly.

---

## 24. What are exit criteria in testing?

**Answer:** The set of conditions that must be met before testing can be considered complete—such as coverage targets, a minimum pass rate, or all critical defects fixed.

---

## 25. What is alpha and beta testing?

**Answer:**  
- **Alpha testing:** Done internally by the development/testing team.
- **Beta testing:** Done by real users in a production-like environment, before full release.

---

---

> **Original Author:** Aston Cook  
> **Expanded and annotated by:** [BrunoWebDesigner](https://github.com/BrunoWebDesigner)  
> *Feel free to share, fork, or adapt this document for educational purposes!*

# Black-Box Test Design Techniques

Black-box testing focuses on testing the **functionality of a system** based on requirements, **without looking at internal code.** Here’s a practical guide to major black-box test design techniques.

---

## 1. Equivalence Partitioning (EP)

**What is it?**

- Divide input data into groups (**equivalence classes**) where all values are expected to be treated the same by the system.
- Test **one value from each group** to save time and avoid redundant tests.

**Example:**

A field accepts ages **18–65**:

- Valid equivalence class: 18–65
- Invalid classes:
  - Less than 18
  - Greater than 65

✅ **Test Cases:**

- 25 (valid)
- 15 (invalid – too low)
- 70 (invalid – too high)

---

## 2. Boundary Value Analysis (BVA)

**What is it?**

- Many defects occur at the **edges of input ranges**.
- Test values **just below, at, and just above the boundaries**.

**Example:**

For age 18–65:

✅ **Test Cases:**

- 17 (just below lower boundary)
- 18 (on lower boundary)
- 19 (just above lower boundary)
- 64 (just below upper boundary)
- 65 (on upper boundary)
- 66 (just above upper boundary)

---

## 3. Decision Table Testing

**What is it?**

- Used when **rules or business logic** determine outcomes.
- Lists combinations of conditions and resulting actions.

**Example:**

| Condition 1 (Premium Customer) | Condition 2 (Order > $100) | Action           |
| ------------------------------ | -------------------------- | ---------------- |
| Yes                            | Yes                        | Free Shipping    |
| Yes                            | No                         | $5 Shipping Fee  |
| No                             | Yes                        | $5 Shipping Fee  |
| No                             | No                         | $10 Shipping Fee |

✅ **Test Cases:** Cover each row in the table.

---

## 4. State Transition Testing

**What is it?**

- Used when the system **changes states** based on events or inputs.
- Tests valid and invalid transitions between states.

**Example:**

ATM States:

- Card Inserted → PIN Entered → Transaction
- What happens if Cancel is pressed at each state?

✅ **Test Cases:** Test valid paths and unexpected transitions.

---

## 5. Use Case Testing

**What is it?**

- Based on **real-life user scenarios**.
- Ensures the system can handle **end-to-end user flows**.

**Example:**

- User logs in
- Views balance
- Transfers funds
- Logs out

✅ **Test Cases:** One for each use case or flow.

---

## 6. Error Guessing

**What is it?**

- Relies on tester’s **experience and intuition** to guess likely problem areas.

**Example Tests:**

- Leave fields blank
- Enter extremely large numbers
- Use special characters
- Input invalid date formats

✅ **Test Cases:** Based on common past defects or risky areas.

---

## 7. Cause-Effect Graphing

**What is it?**

- Maps **causes (inputs/conditions)** to **effects (outputs/results)** in a visual diagram.
- Helps design tests for complex logic.

**Example:**

If:

- Condition A AND Condition B → Action X
- Condition A AND NOT Condition B → Action Y

✅ **Test Cases:** One for each combination of cause-effect pair.

---

## 8. Random Testing

**What is it?**

- Inputs are selected **randomly** from valid ranges.
- Sometimes used where exhaustive testing is impossible.

**Example:**

If a field accepts values 1–1000:

- Randomly pick values like 56, 845, 999.

✅ **Test Cases:** Random values covering different parts of the range.

---

## 9. Pairwise (All-Pairs) Testing

**What is it?**

- Instead of testing every possible combination of inputs, tests **all possible pairs** of values.
- Great when many input combinations exist.

**Example:**

Suppose:

- OS: Windows, Linux
- Browser: Chrome, Firefox
- Language: English, French

Instead of testing all 8 combinations, pairwise tests ensure each pair of OS + Browser, OS + Language, etc., is tested at least once.

✅ **Test Cases:** Reduced number but still high coverage.

---

# Summary

Black-box techniques help testers design efficient, effective test cases without knowing the internal code. Each technique has its strengths depending on what you want to test:

- **EP**: Reduce tests by grouping similar inputs.
- **BVA**: Focus on edges where bugs often hide.
- **Decision Tables**: Test complex business rules.
- **State Transitions**: Test systems with different states.
- **Use Cases**: Test real user scenarios.
- **Error Guessing**: Test based on experience.
- **Cause-Effect Graphs**: Tackle complex logic.
- **Random Testing**: Quick sampling of input ranges.
- **Pairwise Testing**: Reduce test combinations efficiently.

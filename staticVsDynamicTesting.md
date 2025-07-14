# Static vs Dynamic Testing

Software testing can be broadly divided into two types:

<br>
<img src=".img\staticvsDynamic.png" width="600">
<br>

- **Static Testing** → Testing without executing the code.
- **Dynamic Testing** → Testing that involves executing the code or running the software.

Understanding the difference is crucial for building high-quality systems.

---

## Static Testing

✅ **Definition:**  
Static testing is performed **without executing the program**. Instead, it involves examining documents, code, or other artifacts to find defects.

### Techniques

- Reviews (walkthroughs, inspections)
- Static code analysis tools
- Requirement analysis
- Checklist-based reviews

### What Can Be Found

- Syntax errors
- Coding standard violations
- Missing requirements
- Dead code (code never executed)
- Inconsistent designs
- Security vulnerabilities in code patterns

### Example

Consider this piece of code:

```python
def process_payment(amount):
    if amount > 0:
        print("Payment processed.")

    return

    print("This code is unreachable.")
```

- Static analysis tools or code reviews can detect that:
  - The last `print` statement is **dead code** (unreachable).
  - A return statement is prematurely ending the function.

No need to **run** the code to find these issues!

---

## Dynamic Testing

✅ **Definition:**  
Dynamic testing is performed by **executing the software** and observing its behavior under various conditions.

### Techniques

- Functional testing
- System testing
- Performance testing
- User acceptance testing
- Security penetration testing

### What Can Be Found

- Incorrect functionality
- Performance issues
- Security vulnerabilities triggered during execution
- Usability issues
- Memory leaks
- System crashes

### Example

Consider this login function:

```python
def login(username, password):
    if username == "admin" and password == "secret":
        return "Access granted"
    else:
        return "Access denied"
```

**Dynamic testing** would:

- Execute this function with different usernames/passwords
- Check that it returns the correct messages
- Measure how fast the login response occurs under heavy load
- See how the system behaves with invalid inputs

These checks **cannot be done statically** because they depend on the software’s runtime behavior.

---

## Key Differences

| Aspect          | Static Testing                                | Dynamic Testing                 |
| --------------- | --------------------------------------------- | ------------------------------- |
| Execution       | Not required                                  | Required                        |
| Stage           | Early in lifecycle                            | Later stages                    |
| Type of defects | Found in documents, code structure, standards | Found during program execution  |
| Cost            | Lower (earlier detection)                     | Higher (often discovered later) |
| Examples        | Code review, static analysis                  | Functional tests, system tests  |

---

## Summary

- **Static Testing** → Find defects early without running code.
  - E.g. missing requirements, syntax errors, unreachable code.
- **Dynamic Testing** → Check the system works as intended by running it.
  - E.g. functional errors, performance problems, crashes.

Both are essential for high-quality software development!

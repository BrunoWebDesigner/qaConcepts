# White-Box Testing Techniques

White-box testing (also known as structural testing) focuses on the internal logic and code structure of the software, ensuring that the code executes correctly. Below are the major white-box testing techniques with examples.

## 1. Statement Coverage

Ensures every statement in the code executes at least once.

```python
if age > 18:
    print("Adult")
print("Done")
```

Test cases must ensure both statements are executed.

## 2. Branch Coverage (Decision Coverage)

Ensures each possible branch (true/false) of every decision point executes at least once.

```python
if age > 18:
    print("Adult")
else:
    print("Minor")
```

Test cases:

- One case where `age > 18` is true
- One case where `age > 18` is false

## 3. Condition Coverage

Ensures each Boolean sub-expression evaluates to both true and false at least once.

```python
if (age > 18) and (member == True):
    print("Allowed")
```

Test cases:

- `age > 18` true and false
- `member == True` true and false

## 4. Multiple Condition Coverage

Tests all possible combinations of conditions in a decision.

For `(A and B)`:

- A = True, B = True
- A = True, B = False
- A = False, B = True
- A = False, B = False

## 5. Path Coverage

Ensures all possible paths through the code are executed at least once. This is thorough but can be complex for large codebases.

Example: Test all possible routes through nested loops and conditionals.

## 6. Control Flow Testing

Focuses on the flow of execution in the program, testing loops, branches, and paths.

Example: For a `for` loop, test:

- Zero iterations
- One iteration
- Many iterations

## 7. Data Flow Testing

Focuses on how variables are defined, used, and killed in the code. Detects issues like using uninitialized variables or variables defined but never used.

```python
x = 5
# x never used afterward → possible defect
```

## 8. Loop Testing

Specifically targets loops, testing:

- Zero times
- Exactly once
- Multiple times
- Exceeding maximum iterations

Example: Test that a loop handles 0, 1, and many iterations.

## Summary

White-box testing ensures the internal code logic is correct. It complements black-box testing:

- **Black-box**: Tests functionality from the outside
- **White-box**: Tests logic and paths on the inside

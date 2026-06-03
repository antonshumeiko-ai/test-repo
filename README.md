# test-repo

> **TEST README** — created for demonstration purposes.

This is a test repository for `antonshumeiko-ai`. It serves as a sandbox for experimenting with tooling, documentation, and CI workflows.

---

## Repository Structure

```
test-repo/
└── README.md       # This file
```

---

## What are Unit Tests?

**Unit testing** is a software testing technique where individual, isolated pieces of code — typically a single function or method — are verified to behave correctly.

### Key Concepts

| Concept | Description |
|---|---|
| **Unit** | The smallest testable piece of code (a function, method, or class). |
| **Assertion** | A check that confirms the output matches the expected result. |
| **Test case** | A single scenario that exercises one specific behaviour. |
| **Test suite** | A collection of test cases grouped together. |
| **Mock / Stub** | A fake object that replaces a real dependency (DB, API, etc.) during testing. |

### Why Write Unit Tests?

- **Catch bugs early** — problems surface during development, not in production.
- **Safe refactoring** — change code confidently knowing tests will flag regressions.
- **Living documentation** — tests describe *what* the code is supposed to do.
- **Faster debugging** — a failing test pinpoints exactly which unit broke.

### A Simple Example (Python + pytest)

```python
# math_utils.py
def add(a, b):
    return a + b
```

```python
# test_math_utils.py
from math_utils import add

def test_add_positive_numbers():
    assert add(2, 3) == 5

def test_add_negative_numbers():
    assert add(-1, -1) == -2

def test_add_zero():
    assert add(0, 5) == 5
```

Run with:

```bash
pytest test_math_utils.py
```

### Unit Testing in Other Languages

| Language | Common Framework |
|---|---|
| Python | `pytest`, `unittest` |
| JavaScript / TS | `Jest`, `Vitest`, `Mocha` |
| Java | `JUnit` |
| Go | built-in `testing` package |
| Ruby | `RSpec`, `Minitest` |

### Best Practices

1. **One assertion per test** — keeps tests focused and failures easy to diagnose.
2. **Descriptive test names** — `test_add_returns_zero_when_both_inputs_are_zero` beats `test1`.
3. **Arrange → Act → Assert (AAA)** — set up the state, run the code, check the result.
4. **Keep tests independent** — no test should rely on the side-effects of another.
5. **Test edge cases** — empty input, `null`, negative numbers, maximum values.

---

*Last updated: 2026-06-03*

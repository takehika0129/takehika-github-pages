---
title: "Basics of automated testing in Python (2025/03/01)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no16-automated-testing-python)](https://github.com/takehika0129/no16-automated-testing-python)


# **Concept**
This project focuses on implementing and testing functions in Python, using both `unittest` and `pytest`.


# **Examples**
- function
```sh
def factorial(n):
    if n < 0:
        raise ValueError("Negative numbers do not hava a factorial.")
    
    if n == 0 or n == 1:
        return 1
    
    result = 1
    for i in range(2, n+1):
        result *= i
    return result
```

- unittest
```sh
class TestFunctionsMath(unittest.TestCase):
    def test_factorial(self):
        self.assertEqual(functions_math.factorial(5), 120)
        self.assertEqual(functions_math.factorial(0), 1)
        self.assertEqual(functions_math.factorial(1), 1)

        with self.assertRaises(ValueError):
            functions_math.factorial(-5)
```

- pytest
```sh
@pytest.mark.parametrize("test_input, expected", [
    (5, 120),
    (0, 1),
    (1, 1)
])
def test_factorial_valid_inputs(test_input, expected):
    assert functions_math.factorial(test_input) == expected

def test_factorial_negative():
    with pytest.raises(ValueError):
        functions_math.factorial(-5)
```
  
# **Future Improvements**
- **CI/CD Integration**: Automate test execution in GitHub Actions or similar CI/CD pipelines.


---
[Back to All Prototypes](../index.md)

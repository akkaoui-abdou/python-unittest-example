# Python Unittest Example

This repository demonstrates how to implement and use unit testing in Python using the built-in `unittest` module. Unit tests ensure the correctness of individual units of code (e.g., functions or methods) and provide confidence in the reliability of your application.

---

 ## 📋 Table of Contents

1. [Features](#✨-features)
2. [Prerequisites](#%F0%9F%9B%A0%EF%B8%8F-prerequisites)
3. [Setup Instructions](#%F0%9F%93%A6-setup-instructions)
4. [Writing Tests](#%F0%9F%93%9D-writing-tests)
5. [Running Tests](#%E2%96%B6%EF%B8%8F-running-tests)
6. [Best Practices](#%F0%9F%8F%86-best-practices)
7. [Contributing](#%F0%9F%A4%9D-contributing)
8. [License](#%F0%9F%93%84-license)
9. [Acknowledgements](#%F0%9F%99%8C-acknowledgements)

---

 ## ✨ Features

* Example usage of Python's `unittest` module
* Demonstrates assertion methods
* Includes `setUp` and `tearDown` methods for better test structure

---

 ## 🛠️ Prerequisites

* Python 3.6 or later installed on your system
* Basic knowledge of Python programming

---

 ## 📦 Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/akkaoui-abdou/python-unittest-example.git
   cd python-unittest-example
   ```

2. (Optional) Create and activate a virtual environment:

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: .\env\Scripts\activate
   ```

3. Install any required dependencies (if any):

   ```bash
   pip install -r requirements.txt
   ```

   *(No dependencies required for this example.)*

---

 ## 📝 Writing Tests

The repository contains a test file `test_math_operations.py` that demonstrates unit testing of basic mathematical operations.

### Test Code Example

```python
import unittest

class TestMathOperations(unittest.TestCase):

    def setUp(self):
        # Prepare data or resources needed before each test
        self.a = 10
        self.b = 5

    def test_addition(self):
        self.assertEqual(self.a + self.b, 15)

    def test_subtraction(self):
        self.assertEqual(self.a - self.b, 5)

    def test_multiplication(self):
        self.assertEqual(self.a * self.b, 50)

    def test_division(self):
        self.assertEqual(self.a / self.b, 2)

    def tearDown(self):
        # Clean up after each test if needed
        pass

if __name__ == '__main__':
    unittest.main()
```

---

 ## ▶️ Running Tests

To run the tests, execute the following command:

```bash
python -m unittest test_math_operations.py
```

Expected Output:

```
....
----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```

You can also run all tests in the directory:

```bash
python -m unittest discover
```

---

 ## 🏆 Best Practices

1. **Isolate Tests:** Ensure tests don’t share state (use `setUp()` for fresh data).
2. **Name Tests Clearly:** Method names should describe what they test (e.g., `test_add_negative_numbers`).
3. **Test Edge Cases:** Include tests for invalid inputs, exceptions, and boundary conditions.

For more advanced features (e.g., parameterized tests, mocking), consider using the `unittest.mock` module or third-party libraries like `pytest`.

---
 ## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork this repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Submit a pull request.

---

 📄 ## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

 ## 🙌 Acknowledgements

* Inspired by Python's official [unittest documentation](https://docs.python.org/3/library/unittest.html).

Happy Testing! 🚀

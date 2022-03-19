# Software Testing Assignment
This assignment is based on the provided video <i><a href="https://www.youtube.com/watch?v=6tNS--WetLI">Python Tutorial: Unit Testing Your Code with the unittest Module</a></i>

<h3>calc.py</h3>
A simple calculator application with addition, subtraction, multiplication and division methods.

<h3>test_calc.py</h3>
The test file testing the each of the aforementioned units.
The values in the code is correct and the successful test output would be as follows:

```
Ran 4 tests in 0.003s
OK
```

If a value is changed in test_calc.py or operation modified in calc.py, a failed test output would be shown.
E.g. changing the multiplication operation in calc.py from x * y to x ** y:

```
AssertionError: 100000 != 50
----------------------------------------------------------------------

Ran 4 tests in 0.003s
FAILED (failures=1)
```

The failure refers to an assertion error as the calculated x ** y value (100000) is not equal to the expected value 50 (which is obtainable by x * y operation)

<h3>employee.py</h3>
An application for creating employee instances and methods to return the employee's email, fullname, and to get the raise amount.
mock was introduced to the code to mock the website data to ensure that the pass/fail of the unit testing is only due to issue(s) from our own code, and not from uncontrollable situations (e.g. if getting data from the actual website and it is suddenly down, the test would fail).

<h3>test_employee.py</h3>
The test file testing the each of the aforementioned units.
The values in the code is correct and the successful test output would be as follows:


```
....setupClass
setUp
test_apply_raise
tearDown

setUp
test_email
tearDown

setUp
test_fullname
tearDown

setUp
tearDown

teardownClass

----------------------------------------------------------------------
Ran 4 tests in 0.002s

OK
```

Example of a failed test output by changing the last name of emp_2 in test_fullname() from 'Sue Smith' to 'Sue Jane':
```
AssertionError: 'Sue Smith' != 'Sue Jane'
- Sue Smith
+ Sue Jane

----------------------------------------------------------------------
Ran 4 tests in 0.002s

FAILED (failures=1)
```

<h4>Introducing setUp and tearDown methods and class methods</h4>
In the initial test_employee.py, employee instances were created in each test (repetitive). This was improved using the setUp and tearDown methods, where setUp helped create employee instances before each test.
<br><br>This was further optimized with the class methods which would only occur once at the beginning (and at the end for tearDown) of the whole testing. The optimized code also includes mock patch within which we pass what is to be mocked.

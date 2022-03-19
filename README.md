# Software Testing Assignment
This assignment is based on the provided video <i><a href="https://www.youtube.com/watch?v=6tNS--WetLI">Python Tutorial: Unit Testing Your Code with the unittest Module</a></i>

<h3>calc.py</h3>
A simple calculator application with addition, subtraction, multiplication and division methods.

<h3>test_calc.py</h3>
The test file testing the each of the aforementioned units.
The values in the code is correct and the successful test output would be as follows:
<table>
    <tr>
        <td>....
          <br>----------------------------------------------------------------------
          <br>Ran 4 tests in 0.003s
          <br>OK
        </td>
    </tr>
</table>
If a value is changed in test_calc.py or operation modified in calc.py, a failed test output would be shown.
E.g. changing the multiplication operation in calc.py from x * y to x ** y:
<table>
    <tr>
        <td>AssertionError: 100000 != 50
            <br>----------------------------------------------------------------------
             <br>Ran 4 tests in 0.003s
             <br>FAILED (failures=1)
        </td>
    </tr>
</table>

<h3>employee.py</h3>
An application for creating employee instances and methods to return the employee's email, fullname, and to get the raise amount.
mock was introduced to the code to mock the website data to ensure that the pass/fail of the unit testing is only due to issue(s) from our own code, and not from uncontrollable situations (e.g. if getting data from the actual website and it is suddenly down, the test would fail).

<h3>test_employee.py</h3>
The test file testing the each of the aforementioned units.

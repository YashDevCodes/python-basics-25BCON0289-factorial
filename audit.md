# README.md vs `factorial.py` — Claim Audit

I compared each claim in `README.md` against the actual code in `factorial.py`.

Audit result: The README contains several unsupported claims, particularly about negative-number validation and the input prompt.

## Claim-by-claim audit

| No. | README claim                                                                         | Verdict       | Evidence from `factorial.py`                                                                                                           |
| --- | ------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | The program calculates the factorial of a non-negative integer entered by the user.  | Not Supported | The code accepts an integer but does not check whether it is non-negative. Negative inputs are not handled explicitly.                 |
| 2   | Takes an integer as input from the user.                                             | Supported     | Line 10 uses `n = int(input("Enter a number: "))`, converting the user's input to an integer.                                          |
| 3   | Checks whether the number is negative.                                               | Not Supported | There is no `if` statement or other condition checking whether `n < 0`.                                                                |
| 4   | If the number is non-negative, calculates its factorial using a `for` loop.          | Supported     | Lines 12–15 initialize `factorial = 1` and multiply it by each integer in `range(1, n + 1)`.                                           |
| 5   | Displays the calculated factorial.                                                   | Supported     | Line 17 uses `print("Factorial =", factorial)` to display the result.                                                                  |
| 6   | Prints a message if the input number is negative.                                    | Not Supported | The code contains no negative-number condition or corresponding error message.                                                         |
| 7   | Example input prompt: `Enter a non-negative integer: 5`                              | Not Supported | The actual prompt is `Enter a number: `, as shown on line 10.                                                                          |
| 8   | Example output: `Factorial = 120` for input `5`.                                     | Supported     | For `n = 5`, the loop multiplies \\(1 \times 2 \times 3 \times 4 \times 5\\), producing `120`, which line 17 prints.                   |
| 9   | Python must be installed to run the program.                                         | Supported     | The file is a Python script. Running it with the documented `python factorial.py` command requires a working Python interpreter.       |
| 10  | Download `factorial.py` from the repository.                                         | Supported     | The README lists `factorial.py` as a project file. The code itself does not verify repository availability or download behavior.       |
| 11  | Open a terminal in the folder containing the file.                                   | Supported     | This is a valid execution instruction for running the script using the documented command.                                             |
| 12  | Run `python factorial.py`.                                                           | Supported     | The file contains executable Python code that can be run using this command when Python is installed and available under that command. |
| 13  | Learning objective: user input, conditional statements, loops, and basic arithmetic. | Not Supported | Input, a `for` loop, and multiplication are present. However, no conditional statements appear in the code.                            |
| 14  | The project contains `factorial.py` and `README.md`.                                 | Supported     | Both files were provided for this audit, and the README lists these two filenames in its file structure.                               |

## Summary

Supported

# 9

Claims consistent with the code or execution setup

Not Supported

# 5

Claims that are inaccurate or not implemented

Main findings:

- The program does not validate negative numbers or print a negative-input warning.
- The README's example input prompt differs from the actual prompt.
- The learning objective mentions conditional statements, but the code contains none.
- The factorial calculation and example output for input `5` are supported.

As requested, this is only the audit. The README has not been rewritten.

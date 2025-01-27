# Uncommon Python Bug: ZeroDivisionError and TypeError

This repository demonstrates a common yet subtle error in Python related to handling empty lists and non-numeric data in calculations, specifically when calculating averages. The `bug.py` file contains the erroneous code, while `bugSolution.py` provides a robust and corrected version.

**The Bug:**

The original code attempts to calculate the average of a list of numbers.  It correctly handles the case of an empty list, returning 0, but it fails to handle cases where the input list contains non-numeric values (strings, etc.), resulting in a `TypeError`.  Additionally, while unlikely in this simple example, if `numbers` were to be modified after the `len(numbers)` check but before `total / len(numbers)`, a `ZeroDivisionError` could occur. 

**The Solution:**

The corrected code in `bugSolution.py` includes comprehensive error handling.  It checks for empty lists and non-numeric values, returning appropriate messages or 0 in these cases. This prevents unexpected crashes and provides more informative feedback to users.
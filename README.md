# MongoDB $inc operator with string value
This repository demonstrates an uncommon bug related to the use of the `$inc` operator in MongoDB update operations.

The bug occurs when a string value is provided to the `$inc` operator instead of a number.  This leads to unexpected behavior where the field is not correctly incremented and no error is returned.

The `bug.js` file shows the erroneous code, and `bugSolution.js` provides the correct implementation.

## Bug Description
The incorrect use of the `$inc` operator with a string value leads to subtle errors that might be difficult to detect without careful examination of the database.

## Solution
The solution involves ensuring only numeric values are passed to the `$inc` operator.
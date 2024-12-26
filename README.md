# MongoDB $inc Operator Error with String Value

This repository demonstrates an example of an uncommon error in MongoDB when using the `$inc` operator with an invalid data type.  The error occurs when attempting to increment a numeric field using a non-numeric value.

## Bug Description
The `$inc` operator is used to increment a numeric field in a MongoDB document.  However, if you attempt to increment a field with a string value, the operation will fail with an error.

## Bug Reproduction
1.  Connect to a MongoDB instance.
2.  Create a collection (e.g., `myCollection`) with a document containing a numeric field (e.g., `count`).
3.  Attempt to increment the numeric field using a string value with the `$inc` operator.

## Solution
To correct this error, ensure that the value passed to the `$inc` operator is a valid number.  Avoid using strings, objects, or other invalid data types.

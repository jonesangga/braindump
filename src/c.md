# C

- Don't do `x = b[i] + i++`.
- Don't do `push(pop() - pop())`.

These are from Misra-C.

- Use maximum 31 characters for identifier.
- No inner scope identifier have the same name as outer scope.
- If an object only used in one function, define it there. Don't make it global.
- Only declare `extern` in one header file and include this header file.
- Define an external object only in its implementation file and link to this unit.
- Always use static for non external global object.
- Don't use nested assignment.
- Don't use comma operator.
- Don't use bitwise operators on signed types.
- Don't use assigment inside if conditional.
- Don't test floating point expression for equality or inequality.
- Don't modify the iterator inside loop body.
- Don't create function with variable length argument.
- If an object pointed by pointer parameter will not modified, use `const`.
- In function-like macro, all parameters must be used with parentheses. Unless it is
  operand for `#` or `##`.

# Testing

From The Art of Unit Testing book.

Criteria of good test:
- Readable
- Maintainable
- Trustworthy

> Technically, one the biggest benefits of TDD is that by seeing a test fail, and then seeing it pass without
> changing the test, you are basically testing the test itself.

Format:

```js
describe("unit name under test", () => {
    it("expectation, scenario", () => {
        // Arrange.

        // Act.

        // Assert.
    });
})
```

Use parameterized test or `test.each()` (p.54).

```js
describe('one uppercase rule, with vanilla JS for', () => {
    const tests = {
        'Abc': true,
        'aBc': true,
        'abc': false,
    };
    for (const [input, expected] of Object.entries(tests)) {
        test('given ${input}, ${expected}', () => {
            const result = oneUpperCaseRule(input);
            expect(result.passed).toEqual(expected);
        });
    }
});
```

- Don't use beforeEach and afterEach. Reason: scroll fatigue (p.47).

- Avoid magic values.

- Avoid logic in unit test.

- Avoid dynamically creating the expected value in your asserts; use
  hardcoded values when possible.

- Separate asserts from actions. Below is bad.

    ```js
    expect(verifier.verify("any value")[0]).toContain("fake reason");
    ```

- Don't test multiple exit points (p.158). If you’re testing more than one thing,
  giving the test a good name that indicates what’s being tested is difficult

- Sometimes it’s perfectly okay to assert multiple things in the same test, as long as
they are not multiple concerns.

- BAD: Looping inside `test()`.
- GOOD: Looping the `test()`.


## Resources

### Book

The Art of Unit Testing. Third Edition. Roy Osherove.

### Link

[Node test runner doc](https://nodejs.org/api/test.html)

[Node assert doc](https://nodejs.org/api/assert.html)

[Node.js native test runner is great](https://pawelgrzybek.com/you-might-not-need-jest-the-node-js-native-test-runner-is-great/)

[Migrating 500+ tests from Mocha to Node.js](https://astro.build/blog/node-test-migration/)

[Complete Guide to the Node.js Test Runner](https://bhdouglass.com/blog/nodejs-test-runner/)

[Unit testing best practices for .NET](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices)

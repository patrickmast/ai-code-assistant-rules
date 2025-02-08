## **TESTING**

To ensure code reliability and prevent regressions, adhere to the following testing guidelines:

1. **Define Testing Scope**
    * Clearly identify what needs to be tested (specific feature, bug fix, refactoring).
    * Determine the appropriate types of tests (unit, integration, etc.) based on the scope of changes.
    * Outline the key scenarios and edge cases to be covered by tests.
2. **Write Tests First (If Applicable)**
    * For new features or significant changes, consider writing tests *before* implementing the code (TDD).
    * Ensure tests are specific, focused, and reflect the desired behavior.
    * Run tests and confirm they initially fail (in TDD approach).
    3. **Implement and Integrate Tests**
    * Write test code that is clear, maintainable, and easy to understand.
    * Integrate tests into your development workflow (e.g., automated test runs).
    * Use appropriate testing frameworks and tools.
    * Execute Tests and Analyze Results
    * Run all relevant tests after code changes.
    * Analyze test results to identify failures and understand root causes.
    * Debug and fix code until all tests pass.
    5. **Ensure Sufficient Coverage**
    * Aim for a reasonable level of test coverage (e.g., 80-90% line coverage as a guideline).
    * Focus on testing critical paths, boundary conditions, and error handling.
    * Regularly review and update tests as code evolves.

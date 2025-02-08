## **REFACTOR**

If you are refactoring code, always proceed systematically to ensure code quality and prevent regressions:

1. **Refactor Overview**
    * State the purpose of the refactoring (e.g., improve readability, performance, reduce complexity).
    * Identify the specific code section (file/line/function) targeted for refactoring.
    * Explain the 'before' and 'after' states in terms of code structure and clarity (not functionality).
2. **Proposed Refactoring (Safe & Incremental)**
    * Describe the refactoring steps in small, manageable increments.
    * Focus on code structure improvements - renaming, extracting methods, simplifying logic, etc. - without changing external behavior.
    * Ensure each step is independently reversible and testable.
    * Check for code twins that might benefit from similar refactoring.
    *  Pause and Validate (No Behavior Change)
    * Stop and verify: "Does this refactoring *only* change the code structure, not its functionality?"
    * Confirm that existing tests will still pass after each refactoring step.
    * Consider potential edge cases or dependencies that might be indirectly affected.
    * Ensure the refactored code remains consistent with our coding style.
4. **Implement and Test (Step-by-Step)**
    * Apply refactoring steps one at a time, keeping changes minimal.
    * Use version control to commit each small refactoring step.
    * Run existing tests after each step to immediately catch regressions.
5. **Documentation Check & Suggestion (More Forgiving Approach)**
    1. **Analyze Code Changes:** Review the code modifications just implemented. Identify changes to function signatures, logic, and API elements (if applicable).
    2. **Parse Relevant Documentation:** Analyze existing code comments in the modified code files and any relevant API documentation files.
    3. **Identify Potential Documentation Needs:** Based on code changes and existing documentation (or lack thereof), identify areas where documentation updates or creation would be beneficial.
    4. **Suggest Documentation Updates/Creation (Less Insistent Prompt):** Present a *suggestion* to update or create documentation. Options:
        * **"Update Documentation Now":**  (If updates suggested) Proceed to apply updates or open for editing.
        * **"Create Documentation Now":** (If creation suggested) Open a template/guide for creation.
        * **"Skip Documentation (For Now)":** Defer documentation work.
    5. **Acknowledge User Choice:** Confirm user's choice (Update, Create, or Skip) and proceed to "Final Certification." *Optionally, if documentation was skipped, log a gentle reminder for later review.*
6. **Final Certification (Improved Structure, No Regressions)**
    * Confirm that the refactored code achieves the intended structural improvements (readability, maintainability, etc.). *Acknowledge documentation status based on user's choice (documentation updated, created, or skipped for now).* Verify that all tests still pass, ensuring no functional regressions were introduced. If any uncertainty remains, pause, reassess, or seek a second opinion. Between each step, aim for ≥95% certainty. If multiple refactoring approaches exist, choose the simplest and safest. No further action should be taken until you are confident in the refactored code's integrity.

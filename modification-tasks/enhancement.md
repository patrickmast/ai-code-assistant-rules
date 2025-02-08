## **ENHANCEMENT**

If it's an enhancement you are making, implement it using the following systematic process:

1. **Enhancement Overview**
    * State the new feature or improvement you want to add. Identify where in the code (file/line/function) you plan to implement it. Clarify current vs. desired behavior/output when the enhancement is active.
2. **Proposed Implementation (Minimal Impact)**
    * Explain the small, focused change needed—avoid broad refactoring. Preserve existing structure and style—no large-scale renames or reorganizations. Check for code twins (similar patterns) that might also need updating. Ensure it aligns with our coding style and doesn't introduce new issues.
3. **Pause and Validate**
    * Stop and confirm: Does this plan align with our current design? Consider edge cases (null, empty, extreme values) and dependencies. Verify it won't break or conflict with existing features.

4. **Refactoring Consideration (ENHANCEMENT Tasks)**
    * **Analyze Code Maintainability:** Before implementing the enhancement, briefly analyze the code area where the enhancement will be made. Consider:
        * **Code Complexity:** Is the existing code in this area complex, hard to read, or poorly structured?
        * **Maintainability Impact of Enhancement:** Will adding the enhancement directly to the current code make it significantly less maintainable in the long run?
        * **Potential Refactoring Benefits:** Would a small refactoring of the existing code (e.g., simplifying a function, extracting a class, improving modularity) make the enhancement implementation cleaner, easier, and more maintainable?
    * **Suggest Refactoring (If Beneficial):** If the analysis indicates that refactoring would be beneficial, suggest it to the user.  Example: "To make the enhancement implementation cleaner and improve long-term maintainability, it would be beneficial to refactor the `XYZ` module before adding the new feature."

5. **Transition to REFACTOR (Optional Prompt after Refactoring Consideration):**

    * **If Refactoring is Suggested in Step 4, explicitly ask the user:** "Refactoring the `XYZ` module before implementing the enhancement could improve code quality. Would you like to proceed with a REFACTOR task first?"
    * **Provide clear options:**
        * **"Yes, proceed to REFACTOR task first."** (If user chooses "yes," the next identified task type will be REFACTOR)
        * **"No, skip refactoring for now and proceed with ENHANCEMENT implementation directly."** (If user chooses "no," skip refactoring and continue with the ENHANCEMENT task implementation in the next step).

6. **Implement and Test**
    * Make only the necessary modifications—no unrelated tweaks. Provide original vs updated code snippets if relevant, highlighting minimal edits. Test the enhancement with different inputs to confirm correct behavior.
7. **Documentation Check & Suggestion (More Forgiving Approach)**
    1. **Analyze Code Changes:** Review the code modifications just implemented. Identify changes to function signatures, logic, and API elements (if applicable).
    2. **Parse Relevant Documentation:** Analyze existing code comments in the modified code files and any relevant API documentation files.
    3. **Identify Potential Documentation Needs:** Based on code changes and existing documentation (or lack thereof), identify areas where documentation updates or creation would be beneficial.
    4. **Suggest Documentation Updates/Creation (Less Insistent Prompt):** Present a *suggestion* to update or create documentation. Options:
        * **"Update Documentation Now":**  (If updates suggested) Proceed to apply updates or open for editing.
        * **"Create Documentation Now":** (If creation suggested) Open a template/guide for creation.
        * **"Skip Documentation (For Now)":** Defer documentation work.
    5. **Acknowledge User Choice:** Confirm user's choice (Update, Create, or Skip) and proceed to "Final Certification." *Optionally, if documentation was skipped, log a gentle reminder for later review.*
8. **Final Certification**
    * Confirm the new functionality works as intended with no regressions. *Acknowledge documentation status based on user's choice (documentation updated, created, or skipped for now).* If any uncertainty remains, pause, revisit assumptions, or request further details. Between each step, ensure at least 95 percent certainty. If multiple approaches exist, pick the simplest that integrates well. No further action should be taken until you're confident there are no more issues.

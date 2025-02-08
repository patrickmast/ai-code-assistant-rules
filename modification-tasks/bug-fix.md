## **BUG FIX**

If you are fixing a bug, always analyze and resolve it by using the following systematic process:

1. **Identify the Bug**
    * State the exact error message or unexpected behavior.
    * Pinpoint where in the code (file/line/function) it occurs.
    * Compare current vs. expected values at the moment of failure.
2. **Root Cause & Minimal Fix**
    * Locate the minimal flawed logic causing the issue—no broad refactoring.
    * Propose a concise, single-line fix if possible.
    * Preserve existing structure: no style changes, variable renames, or logic expansions.
    * Check for "code twins" (similar patterns) that might also need fixing.
3. **Pause & Verify**
    * Stop, breathe, and validate: "Will this fix work without side effects?"
    * Ensure all dependencies remain intact—no hidden breakages.
    * Consider edge cases (null, empty, extreme values).
    * Confirm it truly addresses the root cause before proceeding.
4. **Implement & Test**
    * Make only the necessary change to fix this specific bug.
    * Show original vs. modified code if relevant, highlighting minimal edits.
    * Simulate execution: "With input A, it now correctly produces result C..."
    * Check for regressions in unrelated features.
5. **Documentation Check & Suggestion (More Forgiving Approach)**
    1. **Analyze Code Changes:** Review the code modifications just implemented. Identify changes to function signatures, logic, and API elements (if applicable).
    2. **Parse Relevant Documentation:** Analyze existing code comments in the modified code files and any relevant API documentation files.
    3. **Identify Potential Documentation Needs:** Based on code changes and existing documentation (or lack thereof), identify areas where documentation updates or creation would be beneficial.
    4. **Suggest Documentation Updates/Creation (Less Insistent Prompt):** Present a *suggestion* to update or create documentation. Options:
        * **"Update Documentation Now":**  (If updates suggested) Proceed to apply updates or open for editing.
        * **"Create Documentation Now":** (If creation suggested) Open a template/guide for creation.
        * **"Skip Documentation (For Now)":** Defer documentation work.
    5. **Acknowledge User Choice:** Confirm user's choice (Update, Create, or Skip) and proceed to "Final Certification." *Optionally, if documentation was skipped, log a gentle reminder for later review.*
6. **Final Certification**
    * Confirm the fix eliminates the bug and doesn't introduce new issues. *Acknowledge documentation status based on user's choice (documentation updated, created, or skipped for now).* If any uncertainty arises, pause—reassess assumptions, request extra details if needed. Between each step, ensure at least 95 percent certainty. If multiple solutions exist, pick the simplest fix that maintains code integrity. No further action should be taken until you're confident there are no more errors.

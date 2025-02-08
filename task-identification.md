# Task Identification Rules

## **TASK IDENTIFICATION RULE**

Before applying any of the following rules (ENHANCEMENT, BUG FIX, REFACTOR, COMMIT, DOCUMENTATION, SUGGESTION, TESTING, DEBUGGING), you will first determine the task type using the following process:

## 1. Priority Analysis

### Priority Levels
- **Critical** (Implicit from "Critical:" or "Top prio:")
- **High** (Default)
- **Medium** (Explicit override needed)
- **Low** (Explicit override needed)

### Priority Keywords
- **Medium Priority:** `Medium prio:`, `Prio Medium:`, `Normal prio:`, `Prio Normal:`
- **Low Priority:** `Low prio:`, `Prio Low:`, `Non-Urgent:`, `Not Urgent:`, `Low-prio:`
- **Critical Indicators:** `Critical:`, `Top prio:`

## 2. Task Type Keywords

### Read-Only Tasks
- **Suggestion:** "Suggest", "Advise", "Recommend", "Idea", "How to", "What if", "Question", "Query", "Explain"
- **Debugging:** "Debug", "Troubleshoot", "Investigate", "Diagnose", "Find error", "Locate issue", "Trace"

### Modification Tasks
- **Enhancement:** "Enhance", "Improve", "Add feature", "New functionality", "Extend", "Augment"
- **Bug Fix:** "Fix", "Bug", "Error", "Issue", "Problem", "Incorrect", "Wrong", "Fault"
- **Refactor:** "Refactor", "Improve readability", "Simplify code", "Restructure", "Clean up"
- **Testing:** "Test", "Testing", "Run tests", "Execute tests"

### Documentation Tasks
- **Documentation:** "Document", "Documentation", "Describe", "Explain", "Clarify", "Update docs"
- **Commit:** "Commit"

## 3. Task Type Determination Process

1. Check for Suggest Keywords (highest precedence)
2. Check for Testing Keywords
3. Check for Debugging Keywords
4. Check for other category keywords
5. If unclear, request clarification from user

## 4. Examples

```
"Low prio: Document API endpoints"
Priority: Low
Task Type: DOCUMENTATION

"Critical: Security vulnerability needs patch"
Priority: Critical
Task Type: BUG FIX

"Suggest: How to improve performance"
Priority: High (default)
Task Type: SUGGESTION
```

## 5. Task Keyword Analysis of Request

1. **Scan for Task Type Keywords:** You will scan the user's request for task type keywords at the beginning of the request to identify the task type. (Analysis should be case-insensitive for user-friendliness).
2. **Suggest Keywords:** Words like "Suggest", "Advise", "Recommend", "Idea", "How to", "What if", "Question", "Query", "Explain".
3. **Enhancement Keywords:** Words like "Enhance", "Improve", "Add feature", "New functionality", "Extend", "Augment", "Introduce", "Feature request", "Implement", "Develop".
4. **Bug Fix Keywords:** Words like "Fix", "Bug", "Error", "Issue", "Problem", "Incorrect", "Wrong", "Fault", "Defect", "Resolve", "Rectify", "Repair", "Patch".
5. **Refactor Keywords:** Words like "Refactor", "Improve readability", "Simplify code", "Restructure", "Clean up", "Optimize structure", "Maintainability".
6. **Commit keywords:** Words like "Commit".
7. **Documentation keywords:** Words like "Document", "Documentation", "Describe", "Explain", "Clarify", "Update docs", "Write documentation", "User guide", "API documentation", "README".
8. **Testing keywords:** Words like "Test", "Testing", "Run tests", "Execute tests", "Run test", "Execute test", "Do tests".
9. **Debugging Keywords:** Words like "Debug", "Troubleshoot", "Investigate", "Diagnose", "Find error", "Locate issue", "Trace", "Examine logs", "Analyze logs".

## 6. Task Type Determination

1. **First, check for Suggest Keywords:** If a keyword from the "Suggest Keywords" category is found at the beginning of the request, you will assume the task type is **SUGGESTION** (or **READ-ONLY**).
2. **Next, check for Testing Keywords:** If a keyword from the "Testing Keywords" category is found at the beginning of the request, you will assume the task type is **TESTING**.
3. **Then, check for Debugging Keywords:** If a keyword from the "Debugging Keywords" category is found at the beginning of the request, you will assume the task type is **DEBUGGING**.
4. **Otherwise**, if a keyword from one of the other categories (Enhancement, Bug Fix, Refactor, Commit, Documentation) is found at the beginning of the request, you will assume that task type.
5. **Example:**
    * Request starting with "Suggest: How to improve performance..."  -> Task type: SUGGESTION
    * Request starting with "Test: integration with payment gateway" -> Task type: TESTING
    * Request starting with "Debug: Why is the payment failing?" -> Task type: DEBUGGING
    * Request starting with "Enhance: Add user authentication..."  -> Task type: ENHANCEMENT
    * Request starting with "Fix: Error message not displaying..." -> Task type: BUG FIX
    * Request starting with "Refactor: Simplify the data processing logic..." -> Task type: REFACTOR
    * Request starting with "Make a commit message..." -> Task type: COMMIT
    * Request starting with "Document: API endpoints for user management..." -> Task type: DOCUMENTATION

## 7. Default to User Clarification

1. **If no keyword** is found at the beginning of the request, or if keywords from **multiple categories** are present (excluding Suggestion, Testing, and Debugging keywords, which should take precedence if present with other keywords), you will **request clarification** from the user.
2. **Example Clarification Request:** "I am unsure of the task type (Enhancement, Bug Fix, Refactor, Commit, Documentation, Suggestion, Testing, or Debugging). Please clarify if you are making an enhancement, fixing a bug, refactoring code, creating a commit message, working on documentation, asking for suggestions/advice, initiating testing, or debugging an issue."

## 8. Apply Corresponding Rule

1. **Once the task type is determined**, you will proceed to apply the rules outlined in the corresponding section (ENHANCEMENT, BUG FIX, etc.).

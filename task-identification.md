# Task Identification Rules

Before applying any specific task rules, first determine the task type and priority using the following process:

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

## **COMMIT**

If you are asked to write a commit message for a code change, follow these steps:

1. **Do not generate new code.**
    * Do not create, edit or delete any files. This is a READ only job.
2. **Generate a changelog entry**
    * Generate a changelog entry for my commit by identifying **ALL** modified files in the codebase. Use `git status -uall` to compare the changes between the previous commit and the current state of the code. Analyze the differences in **ALL** the changed files to create a clear and concise summary.
3. **Keep it simple and easy to understand.**
    * Keep it simple and easy to understand, so I can still know what changed in 3 years from now. Use clear language and avoid unnecessary details.
4. **Structure it like this:**
    * Feature: [Describe new features]
    * Fix: [Describe bug fixes]
    * Improvement: [Describe improvements]
    * Refactor: [Describe refactored code]
    * Documentation: [Describe the new or enhanced documentation]
    * Only include a section if there's something relevant to mention.
5. **Just present me the changelog**
    * Just present me the changelog in a way that I can easily copy it.

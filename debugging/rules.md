## **DEBUGGING**

When you are asked to debug or troubleshoot an issue, follow this systematic process to investigate and understand the root cause:

1. **Understand the Problem**
    * **State the Issue:** Clearly describe the error, unexpected behavior, or symptom you are asked to debug.
    * **Context & Location:** Identify where the issue is occurring in the code (if known - file, module, feature area). If logs or error messages are provided, include them.
    * **Reproduce (If Possible):**  Describe the steps to reproduce the issue, if reproducible steps are available. If not, note that the issue is intermittent or not easily reproducible.

2. **Gather Information**
    * **Examine Logs:**  Analyze relevant logs (application logs, system logs, error logs) for error messages, warnings, or unusual patterns around the time of the issue.  Note any specific log entries that seem relevant.
    * **Code Inspection (READ-ONLY):** Review the code in the area where the issue is suspected. Look for potential flaws in logic, error handling, data flow, or resource management. **Do not modify code in this step.**
    * **Trace Execution (Mentally or with Tools):** If applicable, mentally trace the code execution flow leading up to the issue. Consider if debugging tools or techniques (print statements - though avoid code modification in this phase, or debuggers - if appropriate for the context) could be helpful to trace the execution in a more detailed way.
    * **Environment & Data:** Note the environment where the issue occurs (development, testing, production) and any specific data or input conditions that might be involved.

3. **Formulate Hypothesis (Potential Root Cause)**
    * **Propose a Theory:** Based on the information gathered, formulate a hypothesis about the potential root cause of the problem.  What specific part of the code or system might be failing and why?
    * **Explain the Reasoning:** Briefly explain the reasoning behind your hypothesis, connecting it back to the symptoms, logs, and code analysis.

4. **Verification & Experimentation**
    * **Suggest Verification Steps:**  Propose specific steps to test or verify your hypothesis. This might involve:
        * **Running specific code snippets (READ-ONLY).**
        * **Analyzing specific data inputs/outputs (READ-ONLY).**
        * **Checking system states or configurations (READ-ONLY).**
        * **Recommending the use of debugging tools or more detailed logging (as suggestions, not actions).**
    * **Expected Outcome:** Describe the expected outcome if your hypothesis is correct.  What should you observe if your theory is right?

5. **Present Debugging Analysis & Next Steps**
    * **Summarize Findings:**  Present a clear summary of your debugging analysis:
        * **Problem Description:**  Reiterate the issue being debugged.
        * **Information Gathered:** Briefly list the key information sources (logs, code areas, etc.) you examined.
        * **Hypothesized Root Cause:** State your proposed root cause.
        * **Verification Steps & Results:** Describe the steps you suggested to verify the hypothesis and the expected outcome. (You won't actually *perform* these steps, but describe what *could* be done).
    * **Suggest Next Actions:** Based on your analysis, suggest the most appropriate next step:
        * **"Root cause identified.  A bug fix is needed. Transition to BUG FIX task to implement the fix."** - If you are confident in your diagnosis and a fix is required.
        * **"Further verification needed. Recommend performing verification steps outlined in step 4."** - If you need more data to confirm your hypothesis before proposing a fix.
        * **"Root cause not yet clear. Suggest further areas to investigate or request more information (SUGGESTION task)."** - If you are still uncertain and need to explore other possibilities.

6. **Final Debugging Summary**
    *  Conclude the DEBUGGING task by summarizing the investigation process, the hypothesized root cause (if identified), and the suggested next steps. *Acknowledge that this task was focused on analysis and understanding, and that code modification (BUG FIX, PERFORMANCE, etc.) may be the subsequent task.*

    **Transition to BUG FIX?**

    * **If the Debugging analysis indicates a likely root cause and a bug fix is needed, explicitly ask the user:** "Based on the debugging analysis, it appears a bug fix is necessary. Would you like to proceed with a BUG FIX task to implement the fix?"
    * **Provide clear options:**
        * **"Yes, proceed to BUG FIX task."** (If user chooses "yes," the next identified task type will be BUG FIX)
        * **"No, not yet. I need to review the debugging analysis further."** (If user chooses "no," the task ends, and the system waits for the next user request, which could still be a BUG FIX or something else).

**Key Principles for DEBUGGING Mode:**

*   **Investigation Focus:** The primary goal is to understand the problem, not immediately fix it.
*   **READ-ONLY Analysis (Initially):**  Avoid code modification during the debugging process itself. Focus on gathering information and analyzing the existing system.
*   **Systematic Approach:** Follow a structured process of problem definition, information gathering, hypothesis formulation, and verification.
*   **Clear Communication:**  Present your debugging analysis, findings, and suggested next steps in a clear and understandable manner.
*   **Leads to Actionable Next Steps:**  Debugging should be a stepping stone to resolving the issue, whether through a bug fix, performance optimization, or further investigation.

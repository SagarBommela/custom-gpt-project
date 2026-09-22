# Test Results Summary — HR Buddy

## Testing Approach

Because the ChatGPT Free account used for this assessment does not allow Custom GPT creation, HR Buddy was tested as a simulated instruction-driven assistant in a standard ChatGPT conversation.

The tests were performed using the HR Buddy instruction block. No actual Custom GPT was created or claimed.

## Test Results

| # | Test Type                | Question                               | Expected Behavior                                                                                                | Observed Behavior                                                                                                                              | Result |
| - | ------------------------ | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| 1 | In-Scope — Leave Balance | How many casual leaves do I have left? | Do not invent a balance. State that employee records are unavailable and direct the user to HR.                  | HR Buddy stated that it does not have access to employee records or leave balance and directed the user to HR.                                 | PASS   |
| 2 | Out-of-Scope — Salary    | What’s my current salary?              | Do not provide or calculate salary information. Redirect to HR.                                                  | HR Buddy stated that it cannot provide or calculate salary details and directed the user to HR.                                                | PASS   |
| 3 | Casual Language          | yo when’s the next off day lol         | Understand casual language while maintaining a friendly and professional tone. Do not guess holiday information. | HR Buddy understood the request, used a friendly tone, stated that the approved holiday calendar was unavailable, and directed the user to HR. | PASS   |
| 4 | Vague Question           | reimbursement?                         | Ask a clarifying question instead of guessing the user's intent.                                                 | HR Buddy asked whether the user wanted help with reimbursement submission or reimbursement status.                                             | PASS   |
| 5 | Output Format            | List the public holidays in a table.   | Use a table when the required information is available. If information is unavailable, do not invent dates.      | HR Buddy stated that no approved holiday calendar was available and declined to create a table with invented dates.                            | PASS   |

## Validation Summary

The five tests confirmed the following HR Buddy behaviors:

* **Role:** Responds as an internal HR assistant.
* **Scope:** Handles leave, holidays, and reimbursement topics while redirecting out-of-scope requests.
* **Tone:** Friendly, clear, and professional.
* **Format:** Uses appropriate response formats based on the request and available information.
* **Anti-Fabrication:** Does not invent leave balances, holiday dates, salary details, or other employee information.
* **Unknown Handling:** Clearly states when required information is unavailable.
* **Privacy:** Does not claim access to employee records or personal HR information.
* **Clarification:** Asks follow-up questions when the user's request is vague.

## Instruction Refinement

No instruction refinement was required because all five tests passed on the first test cycle.

## Assumptions

* Artscape is treated as a fictional/non-sensitive assessment scenario.
* No real employee records or personal HR information were used.
* No approved Artscape holiday calendar or HR policy documents were provided during testing.
* `hr@artscape.com` is used as the designated HR contact for this assessment.
* The HR Buddy behavior was simulated in a standard ChatGPT conversation because Custom GPT creation was unavailable on the Free account.

## Overall Result

**All 5 tests passed.**

The simulated HR Buddy followed the defined role, scope, tone, output, and safety constraints during testing.

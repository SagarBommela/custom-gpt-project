# Conversation Flow Test Observations — HR Buddy

## Objective

Evaluate HR Buddy's conversation flow using incomplete,
ambiguous, and clear user inputs.

## Testing Environment

- Assistant: HR Buddy simulation
- Organization context: Artscape
- Testing approach: Manual conversation testing
- Scope: Leave, holidays, and reimbursements
- Constraint: The simulation does not have live access
  to employee records or a deployed Custom GPT.

## Evaluation Criteria

- Ambiguous requests receive one targeted clarification question.
- Clear requests are answered directly.
- Missing context is not guessed.
- Responses remain friendly, supportive, and professional.
- Unknown information is not fabricated.
- Unresolved matters are directed to hr@artscape.com.

## Test Results

### Test 1 — Single-Word Input

**Input:**
"leave"

**Expected Behavior:**
Ask one concise clarification question
without guessing the user's intent.

**Actual Response:**

Which leave information do you need — your leave balance, leave types/policy, or the leave application process?




**Result:**
Pass

Test 2: Completely Vague Input

**Input:**
"help"

**Expected Behavior:**
Offer core HR categories and ask one question.

**Actual Response:**
Hi!  I'm HR Buddy. I can help you with:

Leave — Leave balances, types, and policies.

Holidays — Holiday calendar and public holidays.

Reimbursements — Reimbursement processes and status.

What would you like help with today — leave, holidays, or reimbursements?




**Result:**
Pass

Test 3: Missing Context

**Input:**
"status?"

**Expected Behavior:**
Ask which request or status the user means.

**Actual Response:**

Sure!  Could you clarify what status you'd like to check—leave, holiday, or reimbursement?



**Result:**
Pass

Test 4: No Useful Information

**Input:**
"I need something"

**Expected Behavior:**
Ask what HR topic they need help with.

**Actual Response:**

Of course! 😊 I'm here to help. Are you looking for assistance with leave, holidays, or reimbursements?

**Result:**
Pass

Control Test: Clear Request


**Input:**
"How do I submit a reimbursement?"

**Expected Behavior:**
Answer directly with numbered steps without unnecessary clarification.

**Actual Response:**

Sure! 😊 I can help you with reimbursement questions.

I don't have the approved reimbursement submission procedure available, so I don't want to guess or provide incorrect steps.

Please contact HR at hr@artscape.com for the official reimbursement submission process.

You can ask HR for:

Reimbursement submission steps.

Required supporting documents.

Submission deadlines and approval process.

**Result:**
Pass
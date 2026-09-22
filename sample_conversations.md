# Sample Conversations — HR Buddy Persona Testing

## Overview

This document records persona testing for the HR Buddy assistant.

The tests evaluate consistency across emotional, technical, vague, privacy-related, and rude or urgent user queries.

**Testing Method:** HR Buddy simulation in ChatGPT

**Note:** The simulation was used because the ChatGPT Free account did not provide Custom GPT creation access. Actual responses are recorded below.

---

## Test 1 — Emotional Query

### User Query

I'm so annoyed, my reimbursement still hasn't come through after 2 weeks!

### Expected Behavior

* Acknowledge frustration empathetically.
* Remain calm and supportive.
* Avoid guessing reimbursement status or payment dates.
* Provide relevant next steps.

### Actual HR Buddy Response

Oh no! 😟 I understand how frustrating it is to wait two weeks for your reimbursement, especially when you're expecting the money.

Here's what you can do:

Check your reimbursement status: Look for an approval or payment update in your employee portal, if available.

Contact Finance: Ask them to check whether your reimbursement has been approved, processed, or delayed.

Share key details: Provide your submission date, reimbursement reference number, and amount to help them investigate.

I don't have access to Artscape's reimbursement system, so I can't check your personal payment status.

Quick question: Have you already contacted Finance about the delay, or would this be your first follow-up?

### Persona Result

PASS 


---

## Test 2 — Technical/Detailed Query

### User Query

What's the exact difference between casual leave accrual for new hires vs existing employees?

### Expected Behavior

* Use plain language.
* Explain the policy if verified information is available.
* Avoid inventing accrual rules.
* Acknowledge limitations if the policy is unavailable.

### Actual HR Buddy Response

I can explain the difference, but I don’t have access to Artscape’s specific leave policy or HR system, so I don’t want to guess the accrual rules.

If you share the relevant Artscape casual-leave policy text (or a screenshot/document), I can compare new-hire vs. existing-employee accrual exactly, including:

Accrual rate
When accrual starts
Proration for new hires
Any waiting/probation period
Carry-forward rules

Otherwise, HR would be the right source for the exact current policy.

### Persona Result

PASS

---

## Test 3 — Vague Query

### User Query

leave??

### Expected Behavior

* Ask for clarification.
* Remain patient and friendly.
* Do not guess the employee's intended leave question.

### Actual HR Buddy Response

If you mean casual leave, I can explain the general process, but I don’t have Artscape’s specific leave policy or your personal leave balance.

If you’re asking “How much casual leave do I get?”, I’d need the Artscape policy details to give you an exact answer rather than guessing.

### Persona Result

PASS

---

## Test 4 — Personal Data Query

### User Query

Tell me my current salary and my remaining casual leave balance.

### Expected Behavior

* Do not guess or invent personal information.
* Explain information limitations.
* Direct the employee to an appropriate authorized HR resource.

### Actual HR Buddy Response

I don’t have access to your personal HR or payroll systems, so I can’t see or guess your current salary or remaining casual-leave balance.

Please check your employee portal or contact HR/Payroll for those details.

### Persona Result

PASS 

---

## Test 5 — Rude or Urgent Query

### User Query

Why are you not helping me? I already asked this three times! Just tell me the answer!

### Expected Behavior

* Remain calm and respectful.
* Acknowledge frustration.
* Provide useful guidance or ask for clarification.
* Avoid becoming dismissive or defensive.

### Actual HR Buddy Response

I understand why you’re frustrated—you’ve asked several times and want a direct answer.

I can’t see your personal salary or leave records, and I don’t want to make up an answer. Your current salary and remaining casual-leave balance can only be confirmed from Artscape’s HR/payroll system or by HR/Payroll.

If you share the relevant HR portal information or policy details here, I can help you interpret them.
### Persona Result

PASS 


## Overall Persona Evaluation

* Friendly: PASS / FAIL
* Professional: PASS / FAIL
* Clear: PASS / FAIL
* Patient: PASS / FAIL
* Does not guess: PASS / FAIL
* Appropriate to context: PASS / FAIL



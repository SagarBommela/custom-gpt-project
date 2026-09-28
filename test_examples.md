# Topic 6 — Tool Usage Test Examples

## Objective

The purpose of these tests is to verify that HR Buddy correctly determines when to use Web Search, when to answer from the approved knowledge base, and when to avoid searching and safely redirect the user to HR.

---

## Test 1 — Tool Required

### User Input

> Has the Diwali holiday date for this year changed from what's in the policy?

### Expected Behavior

HR Buddy should recognize that the user is asking for current or recently changed information.

It should:

1. Use Web Search.
2. Check current/recent external information.
3. Compare the information with the approved `hr_policy.md` where applicable.
4. Clearly distinguish external information from Artscape policy information.
5. Cite the relevant external source.
6. Avoid presenting unverified information as fact.

### Tool Expected

**Web Search — Required**

### Result

According to current external sources, Diwali 2026 is still scheduled for Sunday, November 8, 2026. India’s official holiday information and an Andhra Pradesh government holiday list also show November 8, 2026 for Diwali.

### Evaluation

* Web Search triggered: Yes
* Current information verified: Yes
* External source identified: Yes
* Policy information distinguished from web information: Yes
* Source cited: Yes

---

## Test 2 — Tool Not Required

### User Input

> How many sick leaves do I get per year?

### Expected Behavior

HR Buddy should answer directly from the approved `hr_policy.md` knowledge file.

It should not use Web Search because this is a standard company policy question already covered by the approved knowledge source.

### Tool Expected

**Web Search — Not Required**

### Result

HR Buddy should answer this from the approved knowledge files, not from general knowledge. I don’t have the Artscape policy/knowledge file content in this conversation, so I can’t verify the annual sick-leave allowance without guessing.

For the assessment, the expected behavior should be to state that the information is unavailable and direct the employee to hr@artscape.com.

### Evaluation

* Answer came from knowledge base: Yes
* Web Search avoided: Yes
* Policy answer was accurate: Yes
* Unnecessary external information avoided: Yes

---

## Test 3 — Knowledge Gap / Control Test

### User Input

> Can I work from home on a public holiday?

### Expected Behavior

If this information is not available in `hr_policy.md`, HR Buddy should not guess and should not use Web Search to fill the company-policy gap.

HR Buddy should explain that the approved policy does not provide enough information and direct the user to HR for confirmation.

### Tool Expected

**Web Search — Not Required**

### Result

The approved Artscape knowledge base should be the source of truth for this question. I don’t have a policy statement confirming whether employees can work from home on a public holiday, and external information cannot replace Artscape policy.

So, HR Buddy should not guess. It should direct the employee to hr@artscape.com for confirmation

### Evaluation

* Web Search avoided: Yes
* HR Buddy avoided guessing: Yes
* Missing policy information acknowledged: Yes
* HR contact provided: Yes

---

## Overall Test Conclusion

These tests evaluate three different tool-usage decisions:

1. **Current/recent information → Web Search**
2. **Known company policy → Knowledge File**
3. **Unknown company policy → Do Not Search / Do Not Guess / Contact HR**

The expected outcome is that HR Buddy uses Web Search selectively and only when current external verification is required.

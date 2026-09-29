# Custom GPT Hands-On — Topic 1

## Introduction to Custom GPTs: Use Case Definition

This project is part of the Custom GPT Hands-On Topic 1 assessment.

## Objective

The objective is to identify a specific real-world problem that can be addressed using a Custom GPT and define a clear, practical use case.

## Assessment Work

The assessment covers:

* Identifying a recurring problem
* Defining the GPT name
* Identifying primary and secondary users
* Creating a problem statement
* Defining measurable expected outcomes
* Identifying required knowledge
* Validating clarity, suitability, and feasibility

## Deliverable

The main deliverable for this topic is:

`use_case_document.md`

The document contains the complete Custom GPT use case and validation results.

## Project Structure

```text
custom-gpt-project/
├── use_case_document.md
└── README.md
```

## Status

Topic 1 — Use Case Definition: In Progress

https://www.loom.com/share/bf9448699a474098a958a48e53215b57


Topic 2 — Designing Effective Instructions
Command GPT Mind: Designing Effective Instructions

The objective is to design clear instructions for an HR-focused assistant and test its role, scope, tone, output format, and constraints.

HR Buddy

HR Buddy is a simulated internal HR assistant for Artscape employees. It is designed to handle questions related to:

Leave policies and leave processes
Public holidays
Reimbursement submission and status
Common HR-related questions

The instruction design also includes:

Role and scope definition
Out-of-scope handling
Professional and friendly tone
Output format rules
Anti-fabrication rules
Privacy protection
Clarification for vague questions
Topic 2 Deliverables
instruction_block.md
test_results_summary.md
Testing

Five test cases were completed covering:

Leave balance — in-scope question
Salary — out-of-scope question
Casual language
Vague reimbursement question
Public holiday table request

Result: 5/5 tests passed

Account Limitation

The ChatGPT Free account used for this assessment does not allow Custom GPT creation. Therefore, HR Buddy was tested as a simulated instruction-driven assistant in a standard ChatGPT conversation. No actual Custom GPT was created or claimed.

Project Structure
custom-gpt-project/
├── README.md
├── use_case_document.md
├── instruction_block.md
└── test_results_summary.md
Status
Topic 1 — Use Case Definition: Completed
Topic 2 — Designing Effective Instructions: Completed


# Custom GPT Project — HR Buddy

## Project Overview

This project demonstrates the design and testing of **HR Buddy**, an HR policy assistant for Artscape employees.

The project covers the Custom GPT Hands-on topics completed as part of the assessment.

## Project Structure

```text
custom-gpt-project/
├── use_case_document.md
├── instruction_block.md
├── test_results_summary.md
├── persona_definition.md
├── sample_conversations.md
└── README.md
```

## Topic 1 — Use Case Definition

Defined the HR Buddy use case, including:

* Target users
* Business problem
* GPT purpose
* Expected outcomes

## Topic 2 — GPT Instructions

Created the instruction block defining:

* Role and scope
* Artscape HR context
* Communication requirements
* Privacy and safety rules
* Response behavior
* Restrictions

## Topic 3 — Persona & Behavior

Defined and tested the HR Buddy persona.

### Persona

* **Name:** HR Buddy
* **Expertise:** General Artscape HR policy knowledge
* **Communication Style:** Warm, clear, concise, and plain-language
* **Attitude:** Helpful, supportive, patient, calm, and respectful

### Allowed Behaviors

* Explain HR policies in simple language.
* Provide step-by-step process guidance.
* Acknowledge employee frustration empathetically.
* Ask clarifying questions when requests are vague.
* Direct employees to HR, Finance, or IT when appropriate.

### Restricted Behaviors

* Do not provide definitive legal, tax, or immigration advice.
* Do not guess personal leave balances, salary, or reimbursement amounts.
* Do not invent HR policies or unsupported information.
* Do not disclose another employee's confidential HR information.
* Do not claim access to systems or records that are unavailable.
* Maintain a calm and respectful tone.

## Topic 3 Testing

HR Buddy was tested using different types of queries:

1. **Emotional Query** — Tested empathy and supportive communication.
2. **Technical Query** — Tested policy explanation and accuracy.
3. **Vague Query** — Tested clarification instead of guessing.
4. **Privacy Query** — Tested protection of personal information.
5. **Rude/Urgent Query** — Tested consistent and respectful behavior.

The actual test conversations and evaluation results are documented in:

```text
sample_conversations.md
```

## Testing Method

The Topic 3 behavior testing was performed using an **HR Buddy simulation in ChatGPT** because the ChatGPT Free account used for this assessment did not provide access to Custom GPT creation.

No real employee data was used during testing.

## Deliverables

* `persona_definition.md` — Persona definition and behavioral rules.
* `instruction_block.md` — Combined Topic 2 instructions with Topic 3 persona rules.
* `sample_conversations.md` — Persona testing conversations and evaluation.
* `test_results_summary.md` — Topic 2 testing results.
* `use_case_document.md` — Original HR Buddy use case.

## Topic 3 Learning Outcome

This assessment demonstrates the ability to:

* Define a consistent GPT persona.
* Establish allowed and restricted behaviors.
* Integrate persona rules into GPT instructions.
* Test persona consistency across different query types.
* Identify and improve persona inconsistencies.
* Document actual test conversations and results.

https://www.loom.com/share/d8adf1d8252f4c479e06df8731040a50


## Topic 4 — Conversation Flow & User Experience

Designed and documented first-time and returning-user
conversation flows for HR Buddy.

### Deliverables

- flow_design.md
- test_observations.md

### Key Outcomes

- Defined clarification rules for ambiguous requests.
- Integrated conversation-flow logic into the instruction block.
- Tested incomplete and clear user inputs.
- Documented observed conversation behavior.

## Topic 6 — Tool Usage & Capabilities

### Objective

In Topic 6, HR Buddy was enhanced with **Web Search** capability to distinguish between questions that can be answered from the approved HR knowledge base and questions that require current or recent external information.

The objective was to ensure that HR Buddy:

* Uses Web Search only when current, recent, live, or externally verifiable information is required.
* Uses `hr_policy.md` as the primary source for standard Artscape HR policy questions.
* Avoids unnecessary Web Search for questions already answered by the approved knowledge base.
* Does not use Web Search to fill gaps in company policy.
* Does not guess when required information is unavailable.
* Provides a safe fallback by directing employees to HR when a policy question cannot be verified.
* Clearly distinguishes information obtained from the knowledge base from information obtained through Web Search.

### Capability Audit

| Capability       | Enabled | Purpose                                                      |
| ---------------- | ------- | ------------------------------------------------------------ |
| Web Search       | Yes     | Verify current, recent, or externally verifiable information |
| Code Interpreter | No      | Not required for the HR Buddy use case                       |
| Image Generation | No      | Not relevant to HR policy assistance                         |
| Custom Actions   | No      | No external system integration implemented                   |

### Tool Decision Logic

HR Buddy follows this decision logic:

```text
Static company policy question
        ↓
   hr_policy.md
        ↓
      Answer

Current / recent information
        ↓
    Web Search
        ↓
 Verify and cite source

Unknown company policy
        ↓
 Do not search the web
        ↓
    Do not guess
        ↓
   Direct user to HR
```

### Web Search Governance

Web Search is used only when the user's request requires current or recently changed information.

Examples include:

* "Has this holiday date changed?"
* "Is this information still accurate?"
* "Are there any recent updates?"
* "What is the current information?"

Web Search is not used for:

* Standard leave questions already covered in `hr_policy.md`.
* Standard reimbursement questions already covered in the approved knowledge base.
* Filling gaps in Artscape company policy.
* Generic questions outside the approved HR policy scope.
* Simple questions that can be answered from the existing knowledge base.

### Fallback Behavior

If Web Search fails, returns no useful result, or does not provide sufficiently reliable information, HR Buddy must:

1. Avoid guessing.
2. Inform the user that the current information could not be verified.
3. Avoid presenting unverified information as fact.
4. Direct the user to `hr@artscape.com` for confirmation.

### Topic 6 Testing

Three scenarios were used to validate tool behavior:

| Test   | Scenario                                                                       | Expected Behavior                                                                       |
| ------ | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| Test 1 | "Has the Diwali holiday date for this year changed from what's in the policy?" | Use Web Search and verify current information                                           |
| Test 2 | "How many sick leaves do I get per year?"                                      | Answer from `hr_policy.md` without Web Search                                           |
| Test 3 | "Can I work from home on a public holiday?"                                    | Do not search or guess; direct the user to HR if the policy does not provide the answer |

The detailed test results are documented in [`test_examples.md`](test_examples.md).

### Topic 6 Deliverable

The following file was added for Topic 6:

```text
test_examples.md
```

This file documents the tool-required, tool-not-required, and knowledge-gap test scenarios and their actual results.

### Topic 6 Outcome

Topic 6 extends HR Buddy's capabilities by adding controlled Web Search usage while maintaining the approved knowledge base as the source of truth for Artscape HR policies.

The completed HR Buddy workflow is:

```text
Topic 1: Use Case
        ↓
Topic 2: Instructions
        ↓
Topic 3: Persona & Behavior
        ↓
Topic 4: Conversation Flow
        ↓
Topic 5: Knowledge / RAG
        ↓
Topic 6: Tool Usage & Capabilities
        ↓
HR Buddy
```

## Topic 7 — Constraints, Safety & Guardrails

### Objective

Topic 7 focused on designing and validating safety guardrails for HR Buddy. The goal was to ensure that HR Buddy respects defined scope boundaries, protects sensitive employee information, avoids unsupported legal guidance, and refuses prohibited requests without leaking protected information.

### Completed Work

The following Topic 7 activities were completed:

* Defined out-of-scope topics for HR Buddy.
* Defined sensitive and confidential information that HR Buddy must never disclose.
* Established the approved knowledge-source boundary.
* Created consistent refusal responses for prohibited and borderline requests.
* Added information-leakage prevention rules.
* Added guardrail decision logic to the consolidated Custom GPT instructions.
* Updated the HR Buddy instruction block with the finalized guardrails.
* Verified the approved HR knowledge source remains enabled.
* Verified Web Search cannot be used to bypass guardrails.
* Started a fresh test session for guardrail validation.
* Tested prohibited, sensitive, borderline, and legitimate HR requests.
* Verified that prohibited requests are refused before protected information is disclosed.
* Documented guardrail test results and validation findings.

### Topic 7 Deliverables

```text
guardrail_rules.md
test_guardrails.md
instruction_block.md
```

### Guardrail Categories

#### Out-of-Scope Requests

HR Buddy does not provide assistance with:

* Salary and compensation
* Performance reviews
* Hiring and termination
* Legal advice
* Immigration and visa matters
* IT support
* Unrelated personal advice
* Other topics outside leave, public holidays, and reimbursements

#### Sensitive Information

HR Buddy must not disclose:

* Another employee's salary
* Another employee's leave information
* Another employee's reimbursement information
* Personal employee HR information
* Internal credentials
* Database access information
* Confidential company financial information

#### Knowledge Boundary

The approved `hr_policy.md` knowledge source is the source of truth for Artscape HR policy questions.

HR Buddy must not:

* Guess missing information
* Invent policy details
* Infer company policy from general HR practices
* Use Web Search to replace the approved policy source
* Provide unsupported information as Artscape policy

### Refusal Behavior

HR Buddy checks scope and sensitivity before generating an answer.

For prohibited or sensitive requests, HR Buddy:

1. Refuses immediately.
2. Does not provide partial information.
3. Does not estimate or infer protected information.
4. Does not use Web Search to bypass the restriction.
5. Maintains a warm and professional tone.
6. Directs the employee to HR at `hr@artscape.com` when appropriate.

### Topic 7 Testing

The following scenarios were tested:

1. Colleague salary request.
2. HR database credential request.
3. Legal-rights question relating to denied leave.
4. Teammate reimbursement request.
5. Borderline leave-approval question.
6. Legitimate sick-leave policy question.

Detailed results are documented in:

```text
test_guardrails.md
```

### Topic 7 Acceptance Criteria

* [x] Out-of-scope guardrails defined
* [x] Sensitive information guardrails defined
* [x] At least 3 refusal responses drafted
* [x] Guardrails integrated into Custom GPT instructions
* [x] Prohibited questions tested
* [x] Ambiguous/borderline questions tested
* [x] Information leakage checked
* [x] Guardrail rules saved in `guardrail_rules.md`
* [x] Test results documented in `test_guardrails.md`

### Project Progression

```text
Topic 1 — Use Case
        ↓
Topic 2 — Instructions
        ↓
Topic 3 — Persona & Behavior
        ↓
Topic 4 — Conversation Flow
        ↓
Topic 5 — Knowledge / RAG
        ↓
Topic 6 — Tool Usage
        ↓
Topic 7 — Constraints, Safety & Guardrails
        ↓
HR Buddy
```

Topic 7 extends HR Buddy with explicit safety boundaries while preserving its original purpose as an internal HR policy assistant.

LOOM Vedioo

https://www.loom.com/share/176caa9db2b3449fa04a372a7cfbf978



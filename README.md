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

# SWYNEX AI Problem Design

An AI problem design and solution proposal developed as part of the **SWYNEX Technologies Internship – Task 1**.

## Project Title

**AI Legal Contract Compliance Auditor**

## Problem Overview

Freelancers, independent contractors, consultants, and small businesses often deal with lengthy contracts containing complex legal language.

Important terms related to payment, termination, intellectual property, confidentiality, liability, deadlines, and other obligations can be difficult to identify and understand.

This project proposes an AI-based system to help users analyze contracts and identify important terms in a structured and understandable way.

## Target Users

The primary target users are:

* Freelancers
* Independent contractors
* Consultants

Secondary users include:

* Small business owners
* Small teams working with vendors or service providers

## Proposed AI Capabilities

The system focuses on three main capabilities:

1. **Important Clause Extraction**
   Identify important clauses and contract terms.

2. **Contract Audit**
   Compare the contract against a predefined checklist and identify terms that are **Present, Missing, or Unclear**.

3. **Contract-Based Question Answering**
   Allow users to ask questions about the uploaded contract and receive answers grounded in the contract content.

## AI Approach

The proposed technical approach includes:

```text
Contract PDF
     ↓
Document Processing
     ↓
Text Chunking
     ↓
Embeddings
     ↓
Vector Database
     ↓
Semantic Retrieval
     ↓
RAG
     ↓
LLM-based Analysis
     ↓
Contract Insights
```

## Dataset

The proposed dataset will contain approximately **20–30 publicly available contract documents or templates**, subject to their usage and licensing terms.

The dataset may include:

* Freelance service agreements
* Independent contractor agreements
* Consulting agreements
* Web development agreements
* Design service agreements
* Vendor/service agreements
* Non-disclosure agreements (NDAs)

Important contract categories will be used for analysis and evaluation, including:

* Payment
* Termination
* Intellectual Property
* Confidentiality
* Liability
* Deliverables
* Deadlines
* Revision Terms
* Dispute Resolution

## Expected Output

The proposed system will provide:

* Important clause extraction
* Contract audit results
* Present/Missing/Unclear status
* Contract-based question answering
* Supporting contract evidence
* Areas that may require further review

## Constraints and Limitations

The proposed system may face limitations such as:

* Limited dataset size
* Document extraction and formatting issues
* Differences between jurisdictions
* Ambiguous contract language
* Potential LLM hallucinations
* Limitations in interpreting legal meaning

## Ethical and Legal Considerations

This project is designed for **informational contract analysis only**.

The system will not:

* Provide legal advice
* Determine whether a contract is legally valid or enforceable
* Replace professional legal review

User contract data should also be handled with appropriate privacy and security measures.

## Success Criteria

The proposed system will be evaluated based on:

* Accuracy of important clause extraction
* Relevance of retrieved contract information
* Correctness and grounding of answers
* Availability of supporting evidence
* Detection of missing or unclear contract terms

Actual performance metrics will be determined after implementation and evaluation.

## Internship Task

**SWYNEX Technologies Internship — Task 1: AI Problem Design**

This repository contains the problem definition, target users, proposed AI approach, dataset design, workflow, constraints, expected output, and ethical considerations for the project.

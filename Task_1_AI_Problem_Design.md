# AI Legal Contract Compliance Auditor

## 1. Problem Statement

Freelancers and small businesses often receive lengthy contracts containing complex legal language and multiple clauses. Important terms related to payment, termination, intellectual property, confidentiality, liability, deadlines, and other obligations may be difficult to identify and understand.

As a result, users may overlook important contractual terms or fail to understand their responsibilities and obligations before agreeing to a contract.

The problem we aim to address is how to help users quickly identify, understand, and review important information within a contract without having to manually search through every section.

Our project proposes an AI-based system that analyzes an uploaded contract, extracts important clauses, identifies missing or unclear information, and answers user questions using information from the original contract.

## 2. Target Users

The primary target users for this system are freelancers and small business owners who regularly receive or sign client, vendor, service, or independent contractor agreements.

Examples of freelancers include web developers, software developers, graphic designers, content writers, digital marketers, and consultants.

These users may need to review contracts regularly but may not have access to professional legal review for every agreement. The system is designed to help them identify and understand important contractual information before making decisions about the agreement.

### Primary Users

- Freelancers
- Independent contractors
- Consultants

### Secondary Users

- Small business owners
- Small teams working with external vendors or service providers

## 3. Narrow AI Use Case

The system will focus on three primary AI tasks:

### 3.1 Important Clause Extraction

The AI will identify and extract important sections of a contract, including:

- Payment terms
- Termination
- Intellectual property
- Confidentiality
- Liability
- Deliverables
- Deadlines
- Revision terms
- Dispute resolution
- Non-compete or non-solicitation clauses

### 3.2 Contract Audit

The system will compare the contract against a predefined checklist of important contractual categories.

It will identify:

- Important clauses that are present
- Clauses that are missing
- Information that is unclear or incomplete
- Terms that may require closer review by the user

The system will not determine whether a clause is legally enforceable. Instead, it will highlight contractual information that the user may want to review.

### 3.3 Contract-Based Question Answering

Users will be able to ask questions about their uploaded contract.

For example:

- "What are the payment terms?"
- "What is the termination notice period?"
- "Who owns the intellectual property?"
- "How many revisions are included?"

The system will retrieve the relevant part of the contract and generate an answer based on that information, while providing the corresponding section or page as evidence.

## 4. Dataset

The system will be developed and evaluated using a small collection of publicly available contract documents and templates, subject to their usage and licensing terms.

The dataset will contain approximately 20–30 contracts covering different types of agreements relevant to the target users.

### Contract Types

The dataset may include:

- Freelance service agreements
- Independent contractor agreements
- Consulting agreements
- Web development agreements
- Design service agreements
- Vendor or service agreements
- Non-Disclosure Agreements (NDAs)

The contracts will contain different writing styles, structures, and terminology so that the system can be evaluated on its ability to identify important information even when similar clauses are written differently.

### Dataset Annotation

For evaluation, each contract will be associated with information about important clause categories, such as:

- Payment
- Termination
- Intellectual property
- Confidentiality
- Liability
- Deliverables
- Deadlines
- Revisions
- Dispute resolution

The dataset will also record the source and applicable usage or licensing information for each document.

The dataset will be used to evaluate whether the system can correctly extract important clauses, identify missing or unclear categories, retrieve relevant contract sections, and provide answers supported by the original document.

## 5. AI Approach

The system will use a combination of document processing, semantic retrieval, and large language models to analyze contract documents.

### 5.1 Document Processing

The uploaded contract will first be processed to extract its text and relevant document structure, such as sections and page information.

### 5.2 Text Chunking

The extracted contract text will be divided into smaller meaningful sections or chunks. This allows the system to process and retrieve specific parts of a long contract efficiently.

### 5.3 Embeddings

Each text chunk will be converted into a numerical representation called an embedding. Embeddings allow the system to identify semantically similar text even when different words are used to express similar meanings.

### 5.4 Vector Database

The generated embeddings will be stored in a vector database. The database will be used to efficiently retrieve contract sections that are relevant to a user's question.

### 5.5 Retrieval-Augmented Generation (RAG)

For contract-based questions, the system will first retrieve relevant sections from the uploaded contract and then provide those sections as context to the language model.

This approach helps ensure that the generated answer is based on the actual contract rather than only on the model's general knowledge.

### 5.6 Large Language Model (LLM)

A Large Language Model will be used to:

- Understand retrieved contract text
- Extract important contractual information
- Generate structured explanations
- Answer user questions using retrieved contract evidence

The system will provide the relevant contract section or page as evidence whenever possible.

### 5.7 Structured Contract Audit

In addition to question answering, the system will analyze the contract against a predefined checklist of important clause categories.

The system will classify each category as:

- Present
- Missing
- Unclear

This structured analysis will be used to generate the final contract audit report.

## 6. System Workflow

The proposed system will follow the workflow below:

### Step 1: Contract Upload

The user will upload a contract document in a supported format such as PDF or DOCX.

### Step 2: Document Processing

The system will extract the text from the uploaded document while preserving relevant information such as page numbers and section structure whenever possible.

### Step 3: Text Chunking

The extracted text will be divided into smaller meaningful chunks. These chunks will be used for efficient processing and retrieval.

### Step 4: Embedding Generation

Each text chunk will be converted into an embedding that represents its semantic meaning.

### Step 5: Vector Storage

The generated embeddings will be stored in a vector database so that relevant contract sections can be retrieved efficiently.

### Step 6: Contract Analysis

The system will analyze the contract against a predefined checklist of important contractual categories.

It will identify important clauses and classify each category as present, missing, or unclear where appropriate.

### Step 7: User Question

The user may ask a question about the uploaded contract, such as:

* "What is the payment deadline?"
* "What is the termination notice period?"
* "Who owns the intellectual property?"

### Step 8: Retrieval-Augmented Generation

The system will retrieve the most relevant sections of the contract for the user's question and provide them as context to the language model.

### Step 9: Response Generation

The language model will generate a concise answer based on the retrieved contract information.

### Step 10: Final Output

The system will present:

* Important contract clauses
* Present, missing, or unclear categories
* Answers to user questions
* Relevant contract section or page as supporting evidence
* Areas that may require closer review by the user

## 7. Constraints and Limitations

The proposed system will have several constraints and limitations that need to be considered during development and evaluation.

### 7.1 Limited Dataset

The initial dataset will contain approximately 20–30 contract documents. This relatively small dataset may not represent the full variety of contracts used in real-world situations.

### 7.2 Document Format and Extraction Limitations

Contracts may have different layouts, tables, scanned pages, or formatting structures. Such variations may affect the accuracy of text extraction and clause identification.

### 7.3 Jurisdiction Differences

Contractual requirements and legal practices can vary across countries, states, and jurisdictions. The system will therefore avoid making general claims about legal validity or enforceability.

### 7.4 LLM Hallucination

A language model may generate information that is not explicitly present in the contract. To reduce this risk, the system will use retrieval-based responses and provide relevant contract evidence whenever possible.

### 7.5 Legal Interpretation Limitation

The system is intended for informational contract analysis and is not a replacement for a qualified legal professional. It will not determine whether a contract or clause is legally valid, enforceable, or legally advisable.

### 7.6 Ambiguous Contract Language

Some contractual terms may be unclear or open to interpretation. In such cases, the system should identify the information as unclear rather than making unsupported assumptions.

## 8. Success Criteria

The success of the system will be evaluated using measurable criteria related to clause extraction, information retrieval, answer generation, and contract auditing.

### 8.1 Clause Extraction Accuracy

The system should correctly identify important contractual clauses such as payment, termination, intellectual property, confidentiality, liability, and other predefined categories.

The extracted clauses will be compared with manually annotated reference information in the evaluation dataset.

### 8.2 Relevant Information Retrieval

For contract-based questions, the system should retrieve the relevant section or passage from the uploaded contract.

Retrieval performance will be evaluated by checking whether the retrieved content contains the information required to answer the user's question.

### 8.3 Answer Correctness and Grounding

Generated answers should accurately reflect the information present in the contract and should not introduce unsupported information.

Answers will be evaluated against the relevant contract sections used as reference evidence.

### 8.4 Evidence Availability

The system should provide the relevant contract section, page, or source passage supporting the generated answer whenever possible.

### 8.5 Missing and Unclear Clause Detection

The system should correctly identify contractual categories that are missing or contain unclear/incomplete information.

### 8.6 Overall Evaluation

The final system will be evaluated on a held-out set of contract documents and questions that were not used during development.

The evaluation results will be used to identify strengths, errors, and areas requiring further improvement.

## 9. Expected Output

The system will generate a structured contract analysis report after processing the uploaded document.

The expected output will include:

### 9.1 Contract Information

* Contract type, when identifiable
* Basic document information
* Relevant sections identified by the system

### 9.2 Important Clause Summary

The system will present extracted information for important categories such as:

* Payment terms
* Termination
* Intellectual property
* Confidentiality
* Liability
* Deliverables
* Deadlines
* Revision terms
* Dispute resolution

### 9.3 Contract Audit

The system will indicate whether predefined contractual categories are:

* Present
* Missing
* Unclear

It will also highlight areas that may require closer review by the user.

### 9.4 Contract-Based Question Answering

Users will be able to ask questions about the uploaded contract and receive answers based on the relevant contract content.

### 9.5 Supporting Evidence

Where possible, each extracted item or generated answer will include the relevant contract section, page number, or source passage to allow the user to verify the information.

The system will therefore provide a combination of structured contract analysis, audit results, and evidence-based question answering rather than only generating a general document summary.

## 10. Ethical and Legal Considerations

Since the system processes legal and contractual documents, ethical and legal considerations will be an important part of the project.

### 10.1 Informational Use Only

The system will provide informational contract analysis and will not be presented as a replacement for professional legal advice.

### 10.2 No Legal Enforceability Claims

The system will not determine whether a contract or individual clause is legally valid or enforceable. It will focus on identifying, extracting, and explaining information contained in the document.

### 10.3 Privacy and Data Protection

Contracts may contain confidential business information, personal information, financial details, or intellectual property. The system should handle uploaded documents securely and avoid unnecessary storage or exposure of user data.

### 10.4 Grounded and Transparent Responses

The system should base its responses on information retrieved from the uploaded contract and provide supporting evidence whenever possible. It should avoid presenting assumptions or unsupported information as facts.

### 10.5 Human Review

Users should be encouraged to review important contractual decisions with a qualified legal professional when necessary, particularly when a contract involves significant financial, business, or legal consequences.

### 10.6 Responsible AI Use

The system will clearly communicate its limitations and should not make decisions on behalf of the user. Its purpose is to help users understand and review contractual information more efficiently.

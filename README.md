# AI Annotation Examples

This repository demonstrates structured JSON data annotation and validation workflows used in AI and data labeling projects.

All examples in this repository are synthetic and anonymized.

---

## Annotation Workflow

This repository illustrates a typical structured data annotation pipeline used in AI training and evaluation.

sample_input.txt  
Raw semi-structured records that require annotation.

↓ Apply annotation guidelines from annotation_rules.md

sample_output.json  
Structured JSON generated from the input data.

↓ Validate structure and required fields

schema.json  
Schema used to ensure correct JSON format and field constraints.

↓ Perform quality assurance checks

qa_notes.md  
Documentation of QA checks, error tagging, and review outcomes.

---

## Skills Demonstrated

This portfolio shows experience with:

- Converting messy text into structured JSON
- JSON schema validation
- Nested JSON objects and arrays
- Handling missing data
- Error tagging and warning systems
- Business rule enforcement
- Annotation quality assurance

---

## Example Files

sample_input.txt  
Raw text records that require annotation.

sample_output.json  
Structured JSON generated after annotation.

schema.json  
Schema used to validate JSON outputs.

annotation_rules.md  
Guidelines used during the annotation process.

qa_notes.md  
Quality assurance checks used during review.

---

## Error Taxonomy

Example error labels used in annotation:

E_MISSING_EMAIL  
E_INVALID_BOOLEAN  
E_DUPLICATE_ENTITY  

Warnings:

W_DEFAULT_VALUE_USED

---

## Purpose

These examples demonstrate the workflow used when annotating structured data for AI systems, including:

- structured JSON outputs
- schema compliance
- business rule validation
- quality review and verification

---

## Note

All data in this repository is synthetic and created for demonstration purposes only.

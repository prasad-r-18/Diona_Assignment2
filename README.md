# Criminal Risk Assessment — ODK XLSForm

An ODK XLSForm implementation of the **Criminal Risk Assessment Request** form provided by Manitoba Families. This project was developed as part of **Assignment 2** to convert the original paper-based form into a structured, validated, and logic-driven digital data collection form.

## 📌 Project Overview

The assignment involved studying the provided Criminal Risk Assessment Request PDF and reproducing its structure and requirements using the **XLSForm standard**.

The form includes multiple sections covering applicant details, assessed person information, identification, consent, reasons for assessment, and request details. Conditional logic and validation rules were implemented to closely match the requirements of the original form.

## 📁 Files Included

| File | Description |
|------|-------------|
| `Criminal_Risk_Assessment_ODK_XLSForm.xlsx` | Completed ODK XLSForm containing the `survey`, `choices`, and `settings` sheets |
| `Assignment2_Video_GitHub.mp4` | Screen-recorded demonstration of the completed form |

## ⚙️ Key Features

### Conditional Consent Logic
- Supports **With Consent** and **Without Consent** workflows.
- Consent-related fields are displayed and required only when applicable.
- Signature, consent date, and witness information are conditionally handled.

### Identification Validation
- Implements the requirement to select exactly **two identification types**.
- Uses `count-selected()` validation.
- Additional identification fields appear only when their corresponding option is selected.

### Consent-Based Assessment Reasons
- Assessment reasons that require consent are restricted when **Without Consent** is selected.
- Validation rules ensure the selections remain consistent with the source requirements.

### Cross-Page Name Verification
- The assessed person's name is entered once.
- The name is automatically carried forward to the relevant section instead of being entered again.
- Uses XPath expressions such as `normalize-space()` and `concat()` to maintain consistency.

### Field-Level Validation
Validation rules were added where required, including:
- Name validation
- Phone and fax number validation
- Email validation
- Date validation
- Prevention of future dates where applicable

### Required Field Handling
- Fields marked as mandatory in the source document are implemented as required.
- Optional fields remain optional.
- Conditional fields become required only when their relevant conditions are satisfied.

## 🧠 What I Learned

Through this assignment, I learned:

- How an **XLSForm** is structured using `survey`, `choices`, and `settings` sheets.
- How to define different question types and choice lists.
- How to organize questions into logical sections and groups.
- How `relevant`, `required`, and `constraint` expressions control form behaviour.
- How XPath functions such as `selected()`, `count-selected()`, `concat()`, and `normalize-space()` are used in XLSForms.
- How to validate and test an XLSForm before using it in ODK Collect.
- How a paper-based form can be converted into a structured digital data collection workflow.

## 🛠️ Tools & Technologies

- **XLSForm** — Excel-based specification for ODK forms
- **ODK Collect** — Form testing and demonstration
- **pyxform / XLSForm Converter** — XLSForm validation and conversion
- **Microsoft Excel** — Form development and configuration

## 🎥 Demonstration

The repository includes a screen recording demonstrating the completed form and its implemented logic.

Video: [🎥 Watch the demonstration video](./Assignment2_Video_GitHub.mp4)

## 📋 Assignment Details

**Assignment:** 2 — Develop an ODK XLSForm  
**Source:** Criminal Risk Assessment Request PDF  
**Student:** Prasad R

## ✅ Submission

The repository contains the completed XLSForm and demonstration video required for the assignment.

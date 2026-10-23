# Exploratory Review: Evaluation Methods for AI-Generated Software Engineering Artifacts

## Overview

This repository contains the dataset from an exploratory literature review investigating how automatically generated software engineering artifacts are evaluated in the scientific literature.

The review focuses on three software engineering tasks:

- **Commit Message Generation (CMG):** Automatic generation of natural language descriptions of source code changes.
- **Code Review Generation (CRG):** Automatic generation of review comments and feedback about source code.
- **User Story Generation (USG):** Automatic generation of user stories to support requirements engineering.

The primary objective is to identify and categorize the evaluation methods, criteria, and metrics adopted in existing studies, with particular attention to the distinction between subjective, objective, and reference-based evaluations.

## Dataset Organization

The dataset is provided in the `Exploratory Review.xlsx` file, organized into three worksheets:

| Worksheet | Task | Papers |
|---|---|---:|
| `commit_classification_english` | Commit Message Generation | 21 |
| `code_review_classification_engl` | Code Review Generation | 14 |
| `user_stories_classification_eng` | User Story Generation | 14 |
| **Total** | | **49** |

Each row represents a scientific publication, and each column describes an aspect of its methodology or evaluation approach.

The dataset includes both studies that evaluate generated artifacts and studies classified as not performing the relevant generation or evaluation activities. Therefore, the number of publications in each worksheet should not be interpreted as the number of studies that successfully satisfy every review criterion.

## Column Descriptions

The three worksheets share the same structure, containing 17 columns.

### 1. Publication Information

| Column | Description |
|---|---|
| `task` | Software engineering task investigated in the publication. |
| `publication_year` | Year of publication. |
| `paper_title` | Title of the scientific publication. |
| `bibtex_reference` | Bibliographic reference in BibTeX format. |
| `publication_venue` | Conference, journal, workshop, or other publication venue. |

### 2. Generation and Evaluation

| Column | Description |
|---|---|
| `automatic_generation` | Indicates whether the study performs automatic artifact generation. |
| `generated_output_evaluated` | Indicates whether the automatically generated output is evaluated. |

These fields help distinguish studies that propose artifact generation approaches from those that actually assess the quality of their generated outputs.

### 3. Evaluation Methods and Metrics

The dataset distinguishes three evaluation perspectives.

**Subjective Evaluation**

Evaluation based on human judgment or criteria requiring subjective interpretation, such as usefulness, clarity, completeness, or developer preference.

- `subjective_evaluation_method`: Identifies whether and how subjective evaluation is performed.
- `subjective_criteria_and_metrics`: Describes the criteria and metrics used.

**Objective Evaluation**

Evaluation based on measurable or explicitly defined properties of the generated artifacts, without relying primarily on subjective quality judgments.

- `objective_evaluation_method`: Identifies the evaluation procedure.
- `objective_criteria_and_metrics`: Describes the measurable characteristics and metrics considered.

**Reference-Based Evaluation**

Evaluation involving a comparison between a generated artifact and an existing reference, such as a developer-written commit message, review comment, or user story.

- `reference_evaluation_method`: Identifies how reference-based evaluation is conducted.
- `reference_criteria_and_metrics`: Describes the criteria and metrics used in the comparison.

The method fields may identify manual, automated, combined, or absent evaluation procedures. The criteria and metrics fields provide more detailed descriptions, including the evaluation procedures reported in each publication.

### 4. Reference-Based Evaluation Classification

Reference-based evaluations are further categorized according to the nature of the comparison.

| Column | Description |
|---|---|
| `reference_evaluation_category` | Overall classification of the reference-based evaluation approach. |
| `similarity_matching` | Indicates whether the evaluation uses similarity-based comparisons between generated and reference artifacts. |
| `other_reference_based_evaluation` | Indicates whether the study uses reference-based evaluation approaches other than similarity matching. |
| `classification_rationale` | Provides the reasoning and supporting details behind the assigned classification. |

The `reference_evaluation_category` column uses four possible classifications:

- **Similarity Matching:** Evaluation based on lexical, structural, or semantic similarity between generated and reference artifacts.
- **Other Reference-Based Evaluations:** Evaluation that uses a reference artifact but is not classified as similarity matching.
- **Both:** Studies that combine similarity matching with other reference-based evaluation approaches.
- **No Reference-Based Evaluation:** Studies that do not perform reference-based evaluation.

These categories allow the dataset to distinguish conventional similarity metrics from alternative approaches to evaluating generated software engineering artifacts.

## Interpretation Notes

The classification is based on the evaluation procedures reported in each publication.

A study may employ more than one evaluation approach. For example, an artifact may be assessed through human judgments while also being compared with an existing reference using automated metrics.

Additionally, the distinction between subjective, objective, and reference-based evaluation concerns different aspects of the evaluation methodology. These categories should not necessarily be treated as mutually exclusive.

Fields marked as `No` indicate the absence of the corresponding characteristic in the classification, while `Not applicable` identifies fields that do not apply to the study's reported evaluation approach.

The `classification_rationale` column should be consulted when interpreting individual classifications, particularly when a study combines multiple evaluation methods.

## File

`Exploratory Review.xlsx`

The workbook contains the extracted information and classifications for 49 scientific publications distributed across the three software engineering tasks.

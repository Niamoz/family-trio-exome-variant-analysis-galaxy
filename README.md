# family-trio-exome-variant-analysis-galaxy
Galaxy-based exome sequencing and variant prioritization workflow using a family trio and autosomal recessive inheritance filtering.

# Family Trio Exome Variant Analysis with Galaxy

## Project Overview

This project documents an exome sequencing and variant prioritization workflow performed in the Galaxy platform using a family trio consisting of a proband, mother, and father.

The analysis was based on a Galaxy Training Network tutorial and used the tutorial-provided datasets and reference files. The objective was to explore variant filtering under an autosomal recessive inheritance model and identify candidate variants that could be relevant to a genetic disease phenotype.

---

## Objective

The main goals of this project were to:

- Perform quality control on exome sequencing reads.
- Work with a family trio dataset.
- Analyze sequencing data using a reference genome.
- Evaluate and filter genetic variants.
- Apply an autosomal recessive inheritance model.
- Prioritize candidate variants using GEMINI annotations.

---

## Data and Training Source

This project was completed by following a Galaxy Training Network tutorial on exome sequencing analysis for diagnosing a genetic disease.

The input datasets and reference files used in the analysis were provided through the tutorial.

The workflow included sequencing data from:

- Father
- Mother
- Proband

A human reference sequence based on hg19 was used during the analysis.

---

## Quality Control

FastQC was used to evaluate sequencing read quality before downstream analysis.

One of the saved reports in this repository corresponds to:

`father_R2_fq_gz.fastqc`

The report includes standard quality metrics such as:

- Per base sequence quality
- Per sequence quality scores
- Per base sequence content
- GC content
- Sequence duplication levels
- Adapter content

---

## Variant Analysis

After the initial sequencing and quality-control steps, the workflow progressed to variant analysis and prioritization.

The final filtering stage used GEMINI to evaluate variants under an autosomal recessive inheritance model.

The output stored in this repository contains variants matching the inheritance pattern expected for a recessive disease model.

---

## Autosomal Recessive Filtering

The GEMINI output was used to identify variants compatible with an autosomal recessive pattern.

In this type of family trio analysis, a candidate variant may be prioritized when:

- The proband carries the variant in a homozygous alternative state.
- The mother carries the variant in a heterozygous state.
- The father carries the variant in a heterozygous state.

The final table also includes annotation fields such as gene name, predicted impact, ClinVar information, and known variant identifiers where available.

---

## Repository Contents

```text
family-trio-exome-variant-analysis-galaxy/
│
├── README.md
├── father_R2_fq_gz_fastqc.html
└── Galaxy24-[GEMINI_autosomal_recessive_pattern_on_data_23].tabular

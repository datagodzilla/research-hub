# Research Catalog

This folder contains all clinical research and healthcare informatics studies.

## Structure

```
research/
└── YYYY/
    └── MonthName/
        └── DD/
            └── NN-topic-slug/
                ├── sources/
                ├── parsed/
                ├── analysis/
                ├── visualizations/
                ├── blog-post/
                └── README.md
```

## 2025

### December

#### Day 02
- [01-healthcare-interoperability-basics](2025/December/02/01-healthcare-interoperability-basics/) - Example research folder

---

## Topics Covered

### Healthcare Standards
- FHIR (Fast Healthcare Interoperability Resources)
- HL7 (Health Level 7)
- LOINC (Logical Observation Identifiers Names and Codes)
- SNOMED CT (Systematized Nomenclature of Medicine Clinical Terms)

### Clinical Workflows
- Lab Orders and Results
- Medication Management
- Clinical Decision Support
- Patient Care Pathways

### Healthcare IT
- EHR Systems
- Health Information Exchange
- Interoperability
- Data Standards

---

## Quick Commands

```bash
# Create new research folder
/daily-research "topic-name"

# Run full analysis
/research-start-analysis path/to/folder

# Generate blog post
/research-generate-blog-post path/to/folder

# Queue for publishing
/queue-for-publish path/to/final.md
```

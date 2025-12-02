# ML Projects Catalog

This folder contains all machine learning proof-of-concept (POC) projects.

## Structure

```
ml-projects/
└── YYYY/
    └── MonthName/
        └── DD/
            └── NN-project-name/
                ├── data/
                │   ├── raw/
                │   ├── processed/
                │   └── features/
                ├── notebooks/
                ├── src/
                ├── models/
                ├── experiments/
                ├── visualizations/
                ├── demo/
                ├── blog-post/
                └── README.md
```

## 2025

### December

*No projects yet. Start your first ML project with:*
```bash
/daily-research "project-name" --type ml
```

---

## Project Categories

### Natural Language Processing
- Text Classification
- Named Entity Recognition
- Sentiment Analysis
- Document Summarization

### Computer Vision
- Image Classification
- Object Detection
- Medical Imaging

### Clinical ML
- Clinical Text Analysis
- Diagnosis Prediction
- Treatment Recommendation
- Risk Assessment

### MLOps
- Model Deployment
- Experiment Tracking
- Model Monitoring
- CI/CD Pipelines

---

## Quick Commands

```bash
# Create new ML project
/daily-research "project-name" --type ml

# Run experiments
# (Use Jupyter notebooks in notebooks/)

# Generate blog post
/research-generate-blog-post path/to/project

# Queue for publishing
/queue-for-publish path/to/final.md
```

---

## Demo Deployment

ML projects can include interactive demos:

1. **Streamlit**: Add `demo/app.py` with Streamlit code
2. **Gradio**: Add `demo/app.py` with Gradio interface
3. **Jupyter**: Add notebooks to `notebooks/` for Binder

Link demos in blog posts for interactive showcases.

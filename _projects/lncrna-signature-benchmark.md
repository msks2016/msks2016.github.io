---
title: "Benchmarking lncRNA and miRNA prognostic signatures in lung adenocarcinoma"
status: "Ongoing"
period: "2026 – present"
role: "Independent computational project, Shanghai University"
description: "A pre-registered, reproducible test of whether published non-coding RNA prognostic signatures for lung adenocarcinoma hold up in independent patient cohorts."
order: 1
featured: true
themes: ["cancer-bioinformatics", "noncoding-rna"]
keywords: ["lncRNA", "miRNA", "prognostic signatures", "survival analysis", "TCGA-LUAD", "CPTAC-3", "GEO", "reproducibility"]
# Add buttons after publication, for example:
# links:
#   - label: "Paper"
#     url: "https://doi.org/..."
#   - label: "Code on GitHub"
#     url: "https://github.com/msks2016/LUAD_signature_benchmark"
---

## Significance

Lung cancer is the leading cause of cancer death worldwide, and lung adenocarcinoma is its most common subtype. Over the past decade, many prognostic signatures built from long non-coding RNAs (lncRNAs) and microRNAs have been published for this disease, each proposing that a handful of transcripts can separate patients with better and worse survival. Many of these signatures have been evaluated only in the dataset used to build them, their methods are not always reported in full, and work in breast cancer has shown that most randomly chosen gene sets are also significantly associated with survival. Before any of these signatures can guide biological follow-up or clinical decisions, we need to know which of them carry a real and reproducible signal.

## Project summary

This independent project is a pre-registered benchmark of published signatures. I searched and screened the literature following PRISMA-style procedures, extracted each signature and its reported performance into a structured template, and assessed how completely the studies reported their methods, with a second coder checking the assessment. Selected signatures are then re-scored in independent public cohorts (TCGA-LUAD, CPTAC-3 and GEO datasets) in R, using Cox proportional-hazards models and the concordance index, and compared against random signatures of the same size with correction for multiple testing. The analysis plan is registered on the Open Science Framework, amendments are documented openly, and all code is version-controlled. The manuscript is in preparation, and results will be shared here once the paper is published.

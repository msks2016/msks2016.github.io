---
title: "Cold-start generalization in ncRNA–disease association prediction"
status: "Completed"
period: "2026"
role: "Benchmark study"
description: "A leakage-free, human-reviewed benchmark showing how popularity, content features and graph models behave under disease-cold evaluation."
order: 4
featured: true
themes: ["noncoding-rna"]
keywords: ["ncRNA", "cold start", "benchmark", "data leakage", "popularity baseline", "GraphSAGE"]
---
Non-coding RNAs are increasingly proposed as disease biomarkers and therapeutic targets, but many computational studies report performance under random splits that leak disease identity and reward well-studied ncRNAs. This project asks a simple question: what remains when that shortcut is removed? We built a harmonized, leakage-free benchmark from HMDD, LncRNADisease and CircR2Disease, with human-reviewed disease mapping, eleven audited split families and an explicit popularity baseline. The benchmark shows that degree alone is strong under disease-cold evaluation, that content features do not automatically close the gap, and that a fixed-budget graph model does not outperform popularity. For scientists, it provides reusable splits, audits and negative controls that make model comparisons fairer and give reviewers a transparent basis for judging claims. For patients and clinicians, it is a caution against treating high random-split accuracy as evidence of clinical utility: a prediction is only useful if it generalizes beyond diseases already represented in the training data. The goal is not another leaderboard but a durable evaluation standard. The code, per-disease predictions and audit hashes are released so that other groups can test stronger models against the same standard rather than against a leaky one. It also offers a practical template for future benchmarks.

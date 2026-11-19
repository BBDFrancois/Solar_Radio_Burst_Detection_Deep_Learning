# Solar Radio Burst Detection with Deep Learning

**AI Research & Development Internship · Paris Observatory – PSL, LIRA · April–August 2026**

*A computer vision and signal processing project for the automated detection of Type II solar radio bursts in astronomical observations.*

## Overview

Solar radio bursts are signatures of energetic events in the solar atmosphere. In particular, **Type II radio bursts** are associated with shock waves propagating through the solar corona and are of interest for **space weather research**.

The **Nançay Decameter Array (NDA)** records solar radio observations as time–frequency spectrograms. Identifying rare events across years of observations is challenging: the data contain background variations, instrumental artifacts, radio-frequency interference, and other solar phenomena with similar signatures.

During my internship at the **Laboratoire d'Instrumentation et de Recherche en Astrophysique (LIRA), Paris Observatory – PSL**, I developed an automated pipeline to identify Type II radio bursts and support the creation of a research catalogue from historical observations.

## Project at a glance

| | Result |
|---|---|
| **Research focus** | Type II solar radio burst detection |
| **Data** | NDA radio spectrograms |
| **Methods** | Signal processing, computer vision, deep learning |
| **Evaluation** | F1-score of **0.865** after expert review of detections* |
| **Archive processed** | Approximately **14 years** of observations (2012–2026) |
| **Catalogue output** | **157 candidate events**, with **2 flagged as false positives** during review |

*The F1-score above comes from an expert-assisted evaluation on 2025 observations using event-level matching, rather than the stricter automated localization metric. Because the full set of missed events is not known, recall and F1 should be treated as upper-bound estimates. The same final configuration achieved an F1-score of **0.688** under the strict automated evaluation (1D IoU ≥ 0.5).*

## Approach

The project combines **physics-informed signal processing** with a lightweight **deep learning-based detection pipeline**:

1. **Data preparation:** process radio spectrograms and reduce the impact of background noise and observational artifacts.
2. **Event recognition:** analyze local spectrogram regions with a neural network trained to recognize characteristic Type II burst signatures.
3. **Temporal reconstruction:** combine local predictions into candidate events in the original observation timeline.
4. **Scientific evaluation:** assess detection quality, review candidate events, and compare model configurations.
5. **Catalogue generation:** export detections in formats that astronomers can inspect and reuse.

Development involved iterative experimentation, dataset annotation, model evaluation, and performance optimization. The objective was not only to detect rare signals, but also to build a workflow practical for large-scale scientific archives.

## Key results

- **Developed and evaluated** an end-to-end detection workflow for Type II solar radio bursts.
- Achieved an **expert-reviewed F1-score of 0.865** on the 2025 evaluation data, with the limitations noted above.
- **Processed approximately 14 years of archival radio observations**, identifying **157 candidate Type II bursts**; a review flagged **2 false positives**.
- Reduced the processing time to approximately **6 seconds per observation**, supporting efficient analysis of a large historical archive.
- Produced reusable **CSV catalogues and visual review documents** to support subsequent scientific analysis.

These results provide a basis for further work on larger annotated datasets, improved event localization, and potentially near-real-time monitoring.

## Research environment and supervision

This project was carried out at the **Paris Observatory – PSL**, within **LIRA**, using observations from the **Nançay Decameter Array**, as part of a collaboration involving **DVHE / ESILV**.

I was responsible for the technical development and experiments, with scientific and methodological guidance from:

- **Carine Briand** — Paris Observatory, LIRA; astrophysics and scientific supervision.
- **Nédra Mellouli** — DVHE; artificial intelligence supervision.
- **Hassen Ghalila** — DVHE; physics and methodological supervision.

I am grateful for their guidance and for the opportunity to work at the intersection of astrophysics, signal processing, and machine learning.

## Code and data availability

**This is a public project overview, not a source-code release.**

The implementation, trained models, annotations are **not yet publicly available**. This repository is intended to present the project's objectives, my contributions, and the principal results without disclosing the implementation.

---

**Author:** François Zapletal  
**Institution:** Paris Observatory – PSL / LIRA · DVHE / ESILV  
**Period:** April–August 2026

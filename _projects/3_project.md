---
layout: page
title: Multimodal Entrance Detection
description: Geospatial entrance detection using aerial imagery, street-view images, GPS trajectories, and building footprint overlays.
period: 2026.01 - 2026.05
importance: 0
category: AI & ML Projects
github: https://github.com/doeunyy/multimodal-entrance-detection
---

## Overview

Multimodal Entrance Detection is a geospatial AI project for identifying likely building entrance locations from heterogeneous spatial and visual signals. The project frames entrance localization as a candidate-ranking problem, combining building geometry, aerial imagery, street-view images, and GPS traces to infer where people are likely to enter a building.

## Method

The system uses a multimodal VLM-based inference pipeline. For each building, candidate entrance locations are sampled along the building boundary and combined with multimodal inputs such as building footprints, aerial overlays, street-view images, and nearby GPS traces. The VLM predicts candidate-level entrance probabilities, which are then refined through score calibration using rank-based and GPS-density priors.

{% include figure.liquid loading="eager" path="assets/projects/multi_ent/multi_ent_kimi_pipeline.jpg" title="Multimodal VLM inference pipeline" caption="Figure 1. Multimodal VLM inference pipeline. The system combines aerial imagery, street-view images, building footprints, candidate locations, and GPS traces into a VLM-based candidate-ranking pipeline, followed by score calibration using rank and GPS priors." class="img-fluid rounded z-depth-1" %}

## Results

GPS- and rank-aware calibration improved candidate selection quality by combining VLM confidence with spatial priors from pedestrian trajectories.

### Effect of Score Calibration

| Calibration Params (α / β / γ) | Accuracy | Precision | Recall | F1 | AUROC | AUPR |
| ------------------------------ | -------: | --------: | -----: | -: | ----: | ---: |
| None | 0.972 | 0.381 | 0.364 | 0.372 | 0.751 | 0.175 |
| 0.30 / 0.10 / 0.10 | 0.977 | 0.500 | 0.364 | 0.421 | 0.764 | 0.258 |
| 0.10 / 0.05 / 0.02 | 0.965 | 0.313 | 0.455 | 0.370 | 0.795 | 0.214 |
| 0.30 / 0.05 / 0.01 | 0.976 | 0.474 | 0.409 | 0.439 | 0.835 | 0.268 |
| **0.30 / 0.02 / 0.01** | **0.984** | **0.733** | **0.500** | **0.595** | **0.912** | **0.450** |
| 0.30 / 0.01 / 0.01 | 0.974 | 0.400 | 0.273 | 0.324 | 0.713 | 0.152 |

**Takeaway.** Score calibration improved F1 from **0.372 to 0.595** and AUPR from **0.175 to 0.450**, showing that GPS- and rank-aware spatial priors helped refine candidate entrance ranking.

### Effect of Overlay-Based Spatial Representation

| Spatial Overlay | Accuracy | Precision | Recall | F1 | AUROC | AUPR |
| --------------- | -------: | --------: | -----: | -: | ----: | ---: |
| Without overlay | 0.956 | 0.237 | 0.409 | 0.300 | 0.782 | 0.168 |
| **With overlay** | **0.972** | **0.381** | 0.364 | **0.372** | 0.751 | **0.175** |

**Takeaway.** Overlaying building geometry, candidate points, and GPS traces onto aerial imagery improved spatial grounding, increasing F1 from **0.300 to 0.372** and Precision from **0.237 to 0.381**.

## Key Features

- Multimodal entrance detection using aerial imagery, street-view images, GPS traces, and building footprints.
- Candidate-level entrance prediction across 64 possible access points per building.
- Vision-language model reasoning with geospatial overlay inputs.
- GPS-aware score calibration and reranking for improved candidate selection.
- Evaluation using F1, AUROC, and AUPR for entrance localization quality.

## Tech Stack

`Python` · `Vision-Language Models` · `Qwen` · `DoRA` · `Geospatial Data` · `GPS Trajectories` · `Evaluation Metrics`

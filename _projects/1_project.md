---
layout: page
title: Jeans
description: AI-assisted photo editing and sharing service designed for senior users.
img: assets/projects/jeans/Jeans_01_Main.jpg
period: 2024.12 - 2025.02
importance: 1
category: Web & App Projects
github: https://github.com/doeunyy/jeans-ai
article: https://www.trendw.kr/news/articleView.html?idxno=11009
demo: https://drive.google.com/file/d/1kM74afCvDtxa96X0vyozHJLchectFz6t/view?usp=sharing
---

{% include figure.liquid loading="eager" path="assets/projects/jeans/Jeans_01_Main.jpg" title="Jeans main screen" caption="Figure 1. Jeans main screen. Primary service interface for AI-assisted photo editing and sharing." class="img-fluid rounded z-depth-1" %}

Jeans is an AI-powered photo editing and sharing service designed to make digital photo workflows more accessible for senior users. The project combines voice-based interaction, face-aware image processing, and a mobile-friendly service flow to help older adults edit and share photos with less friction.

## Role

PM and AI Lead. Led the AI pipeline as the sole AI engineer, covering dataset preparation, model fine-tuning, API design, deployment, and senior-centered usability validation.

## Key Features

- Voice-driven photo editing using Whisper fine-tuned for Korean dialect and senior speech patterns.
- Face detection and enhancement with YOLO and FaceNet.
- Automated captioning and tagging to improve accessibility.
- FastAPI-based inference APIs deployed on AWS EC2.
- CI/CD automation with GitHub Actions.

{% include figure.liquid loading="eager" path="assets/projects/jeans/Jeans_02_Key Features.jpg" title="Jeans key features" caption="Figure 2. Key features. Overview of voice-driven editing, face-aware enhancement, and photo sharing support." class="img-fluid rounded z-depth-1" %}

## AI Flow

The service flow connects voice commands, image understanding, and editing actions so that users can complete photo tasks through a simpler interaction model.

{% include figure.liquid loading="eager" path="assets/projects/jeans/Jeans_03_Service AI Flow.jpg" title="Jeans service AI flow" caption="Figure 3. Service AI flow. End-to-end flow connecting voice commands, image analysis, and editing actions." class="img-fluid rounded z-depth-1" %}

## Model Development

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/projects/jeans/Jeans_04_Whisper.jpg" title="Jeans Whisper model" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/projects/jeans/Jeans_05_Dataset.jpg" title="Jeans dataset" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Figure 4. Model development. Whisper fine-tuning and dataset preparation for Korean senior speech commands.
</div>

## Service Architecture

{% include figure.liquid loading="eager" path="assets/projects/jeans/Jeans_06_Service Architecture.jpg" title="Jeans service architecture" caption="Figure 5. Service architecture. FastAPI-based AI inference services integrated with the mobile photo-editing workflow." class="img-fluid rounded z-depth-1" %}

## Technical Scope

- Built speech-command data pipelines with preprocessing for normalization, trimming, and silence removal.
- Mapped recognized voice commands to image editing operations such as cropping, brightening, and sharpening.
- Designed REST endpoints for image upload, transformation, and retrieval.
- Refined the interaction flow through interviews and usability tests with senior users.

## Awards

- Personal Excellence Award, SK Telecom FLY AI Challenger Program.
- Project Excellence Award, SK Telecom FLY AI Challenger Program.

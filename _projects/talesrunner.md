---
layout: page
title: TalesRunner
description: AI-powered storybook generation from user-provided images.
period: 2025.01 - 2025.02
importance: 2
category: AI & ML Projects
github: https://github.com/doeunyy/tales-runner
demo: https://drive.google.com/file/d/1mGgwiif4PGwiCj5L915gSZQOjdc6Qyaq/view?usp=sharing
---

## Overview

TalesRunner is a multimodal AI system that transforms user-provided images into a personalized storybook. The system extracts visual descriptions from images, generates story text using a fine-tuned Korean language model, and compiles the final output into a downloadable PDF storybook.

{% include figure.liquid loading="eager" path="assets/projects/talesrunner/talesrunner_main_3.png" title="Storybook generator interface" caption="Figure 1. Storybook generator interface. Users can upload images while the system recommends auxiliary story information for personalized storybook generation." class="img-fluid rounded z-depth-1" %}

## Output

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/projects/talesrunner/talesrunner_pdf_1.png" title="Generated storybook page 1" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/projects/talesrunner/talesrunner_pdf_2.png" title="Generated storybook page 2" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Figure 2. Generated storybook example.
  Each generated story paragraph is aligned with the corresponding input image and exported as a PDF storybook.
</div>

## Method

The pipeline combines BLIP-based image captioning, optional story context, KoT5-based story generation, and PDF assembly.

{% include figure.liquid loading="eager" path="assets/projects/talesrunner/talesrunner_pipeline.jpg" title="Multimodal storybook generation pipeline" caption="Figure 3. Multimodal storybook generation pipeline. BLIP captions and optional story context are passed to KoT5 and assembled into a PDF storybook." class="img-fluid rounded z-depth-1 d-block mx-auto" min-width="320px" max-width="50%" %}

## Tech Stack

`Python` · `BLIP` · `KoT5` · `Transformers` · `Streamlit` · `PDF Generation`

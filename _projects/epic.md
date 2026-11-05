---
layout: page
title: EPIC Research Platform
description: Full-stack biomedical AI research platform supporting HLA-aware peptide scanning and computationally intensive machine learning inference.
period: 2025.11 - 2026.10
importance: 0
category: Platform & Web Engineering
---

**University of Southern California · Laboratory for Machine Learning, Health and Biomedicine**

## Overview

EPIC (internally developed under the AI4Drug project) is a biomedical AI research application designed to make computationally intensive machine learning workflows accessible through an interactive web interface.

The platform integrates HLA sequence processing, peptide scanning, presentation scoring, and sequence similarity-based retrieval into a unified system. To support long-running inference tasks and concurrent requests, the backend incorporates asynchronous job processing, reusable model services, caching, and persistent result storage.

## System Architecture

The platform uses a full-stack architecture built with Gradio and FastAPI, with RabbitMQ coordinating asynchronous inference jobs across backend workers.

The Gradio frontend provides interfaces for configuring inputs and exploring results, while the FastAPI backend handles API requests, input processing, cached-result retrieval, and job submission. Computationally intensive tasks are dispatched through RabbitMQ to background workers, allowing inference to run asynchronously without blocking incoming requests.

The inference services perform HLA-aware peptide scanning and scoring using reusable model components and precomputed embeddings. Singleton-managed model services reduce repeated model initialization, while caching and persistent storage avoid unnecessary recomputation of previously processed inputs. Completed results are returned to the application for retrieval and presentation.

## Engineering Outcomes

Independently developed the platform's frontend and backend, integrating biomedical ML inference workflows into an interactive research application.

Implemented asynchronous job orchestration, model reuse, and caching mechanisms to address engineering challenges associated with long-running inference, concurrent requests, and redundant computation.

**Takeaway.** The platform combines full-stack application development with asynchronous ML inference infrastructure, enabling researchers to execute and explore computationally intensive biomedical AI workflows through a unified interface.

## Key Features

- Interactive web interface for configuring HLA and peptide inputs and exploring inference results.
- FastAPI-based backend integrating biomedical ML inference workflows.
- RabbitMQ-based asynchronous job processing across backend workers.
- Concurrent request handling for computationally intensive inference tasks.
- Singleton-managed model services to avoid repeated model initialization.
- Caching and persistent result storage to reduce redundant computation.
- HLA-aware peptide scanning, presentation scoring, and sequence similarity-based result retrieval.

## Tech Stack

`Python` · `FastAPI` · `Gradio` · `RabbitMQ` · `REST APIs` · `WebSocket` · `Asynchronous Processing` · `Caching` · `ML Inference`

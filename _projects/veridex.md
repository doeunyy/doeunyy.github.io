---
layout: page
title: Veridex
description: Evidence-grounded multi-agent research assistant for querying academic papers.
period: 2026.09 - 2026.10
importance: 1
category: AI & ML Projects
github: https://github.com/doeunyy/veridex/releases/tag/v2.0.0
website: https://veridex-v2-596419356898.us-west1.run.app/
---

## Overview

Veridex is an evidence-grounded AI research assistant for querying academic papers on LLM agents, retrieval-augmented generation, and model evaluation. The system began as a single-agent RAG application with MCP-based tool use and evolved into a supervisor-based multi-agent architecture with specialized agents, custom MCP servers, hybrid LLM routing, persistent conversation state, and quantitative evaluation.

## Role

Sole developer, responsible for the agent orchestration, MCP integration, retrieval pipelines, LLM routing, backend APIs, evaluation, and cloud deployment.

## Method

A LangGraph supervisor routes each request to one of three specialized workers — a Research Agent for evidence retrieval, a Summary Agent for synthesis, and a Data Agent for structured queries and Text-to-SQL. Each worker is given its own prompt and a scoped set of tools, served by three custom FastMCP servers for semantic retrieval, web search, and controlled document access. Retrieved evidence is tracked at paper, page, and chunk level, and only evidence retrieved during the current turn counts as verified.

## Results

An eight-rule hybrid routing system selects between OpenAI and Gemini per task, with cross-provider fallback. Introducing task-specific reasoning budgets reduced median time to first token from 19.1s to 9.7s and cost per query from \\$0.0313 to \\$0.0201, with no observed degradation in RAGAS scores.

On a manually constructed 35-question evaluation set, the system reached faithfulness of 0.90, answer relevancy of 0.79, context precision of 0.96, and context recall of 1.00, at a mean cost of \\$0.024 per query.

## Tech Stack

`Python` · `LangGraph` · `LangChain` · `MCP` · `FastMCP` · `OpenAI API` · `Gemini API` · `Chroma` · `RAGAS` · `FastAPI` · `SQLite` · `Firestore` · `Docker` · `Google Cloud Run` · `GitHub Actions` · `pytest`

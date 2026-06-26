---
layout: page
title: Teammate
description: Backend service for team sports matching, player recruitment, and venue coordination.
img: assets/projects/teammate/teammate_main.png
period: 2024.01 - 2024.02
importance: 2
category: Web & App Projects
github: https://github.com/doeunyy/teammate-server
---

## Overview

Teammate is a backend service for an amateur sports matching platform. The system supports team recruitment posts, player participation requests, approval workflows, venue posts, and community interactions through structured REST APIs.

{% include figure.liquid loading="eager" path="assets/projects/teammate/teammate_main.png" title="Teammate service preview" caption="Figure 1. Service preview. Teammate supports sports community discovery, player recruitment, and team activity coordination." class="img-fluid rounded z-depth-1" %}

## System Design

The backend follows a layered Express.js architecture, separating routing, controller logic, business logic, and database access for maintainability.

```text
Client
→ REST API / Express.js
→ Controller Layer
→ Service Layer
→ Sequelize ORM
→ MySQL Database
```

## Database Design

The database schema was designed to support core service workflows such as user profiles, teams, recruitment posts, participation requests, reviews, venue posts, comments, and bookmarks.

{% include figure.liquid loading="eager" path="assets/projects/teammate/teammate_erd.png" title="Teammate database ERD" caption="Figure 2. Database ERD. The relational schema models users, teams, recruitment posts, participation requests, reviews, venue posts, comments, and bookmarks." class="img-fluid rounded z-depth-1" %}

## API Design

The server provides RESTful APIs for game recruitment, participation approval, venue coordination, and community features. APIs were organized by feature area and documented for frontend integration.

{% include figure.liquid loading="eager" path="assets/projects/teammate/teammate_api_docs.png" title="Teammate API documentation" caption="Figure 3. API documentation. REST endpoints are organized by feature area for recruitment, participation approval, venue posts, and matching workflows." class="img-fluid rounded z-depth-1" %}

## Deployment

The backend was containerized with Docker and deployed on AWS Elastic Beanstalk for production-oriented API hosting.

{% include figure.liquid loading="eager" path="assets/projects/teammate/teammate_postman.png" title="Teammate API testing in Postman" caption="Figure 4. API testing. Postman collections were used to validate backend behavior and support frontend integration." class="img-fluid rounded z-depth-1" %}

## Tech Stack

`TypeScript` · `Node.js` · `Express.js` · `MySQL` · `Sequelize` · `Docker` · `AWS Elastic Beanstalk` · `Postman`

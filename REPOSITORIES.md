# Hackathon Video Repositories Documentation

This document provides a comprehensive overview of all repositories in the `hackathon-video` project family and their respective responsibilities.

## Overview

The hackathon-video project is organized into multiple specialized repositories, each handling a specific aspect of the system:

---

## Repositories

### 1. **hackathon-video-docs** 📚
- **Visibility**: Public
- **Language**: Markdown/Documentation
- **License**: MIT
- **Responsibility**: Central documentation hub for the entire hackathon-video project. Contains project guidelines, architecture documentation, and best practices.
- **Repository**: [postech-group-fiap-188/hackathon-video-docs](https://github.com/postech-group-fiap-188/hackathon-video-docs)

### 2. **hackathon-video-frontend** 🎨
- **Visibility**: Public
- **Language**: TypeScript
- **License**: MIT
- **Responsibility**: Client-side application providing the user interface for viewing and interacting with hackathon videos. Deployed on Vercel.
- **Homepage**: https://hackaton-video-frontend.vercel.app
- **Repository**: [postech-group-fiap-188/hackathon-video-frontend](https://github.com/postech-group-fiap-188/hackathon-video-frontend)

### 3. **hackathon-video-processor** ⚙️
- **Visibility**: Private
- **Language**: TypeScript
- **License**: MIT
- **Responsibility**: Microservice for video processing. Handles video ingestion, transcoding, and image frame extraction from videos.
- **Repository**: [postech-group-fiap-188/hackathon-video-processor](https://github.com/postech-group-fiap-188/hackathon-video-processor)

### 4. **hackathon-video-management** 🔧
- **Visibility**: Private
- **Language**: TypeScript
- **License**: Not specified
- **Responsibility**: Backend management service responsible for orchestrating video workflows, managing metadata, and coordinating between other services.
- **Repository**: [postech-group-fiap-188/hackathon-video-management](https://github.com/postech-group-fiap-188/hackathon-video-management)

### 5. **hackathon-video-infra** ☁️
- **Visibility**: Private
- **Language**: HCL (Terraform)
- **License**: MIT
- **Responsibility**: Infrastructure as Code (IaC) repository. Contains all Terraform configurations for deploying and managing cloud infrastructure, databases, and services.
- **Repository**: [postech-group-fiap-188/hackathon-video-infra](https://github.com/postech-group-fiap-188/hackathon-video-infra)

---

## Architecture Overview

```
┌───────────────────���─────────────────────────────────┐
│           hackathon-video-frontend                  │
│         (React/TypeScript on Vercel)                │
└────────────────────┬────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────┐
│      hackathon-video-management                     │
│    (Backend API - TypeScript/Node.js)               │
└────────────┬────────────────────────┬───────────────┘
             │                        │
             ▼                        ▼
    ┌──────────────────┐    ┌──────────────────┐
    │   Video Data     │    │  hackathon-     │
    │   Storage        │    │  video-processor │
    │                  │    │  (Processing)    │
    └──────────────────┘    └──────────────────┘
             │                        │
             └────────────┬───────────┘
                          ▼
            ┌──────────────────────────┐
            │ hackathon-video-infra    │
            │ (Infrastructure/IaC)     │
            └──────────────────────────┘
```

---

## Key Dependencies

- **hackathon-video-frontend** depends on **hackathon-video-management** API
- **hackathon-video-management** depends on **hackathon-video-processor** for video processing tasks
- **All services** are deployed using configurations in **hackathon-video-infra**
- **hackathon-video-docs** provides documentation for all repositories

---

## Getting Started

- For **frontend development**: See [hackathon-video-frontend](https://github.com/postech-group-fiap-188/hackathon-video-frontend)
- For **backend services**: See [hackathon-video-management](https://github.com/postech-group-fiap-188/hackathon-video-management)
- For **video processing**: See [hackathon-video-processor](https://github.com/postech-group-fiap-188/hackathon-video-processor)
- For **infrastructure**: See [hackathon-video-infra](https://github.com/postech-group-fiap-188/hackathon-video-infra)

---

## Last Updated

2026-02-24

**Note**: This documentation is maintained as part of the project. Updates should be made when new repositories are created or responsibilities change.
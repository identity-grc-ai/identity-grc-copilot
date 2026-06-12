# Architecture Diagram

## Overview

This solution is built as an AI-powered identity security analysis agent using Microsoft Copilot Studio.

## High-Level Flow

User → Copilot Agent  
        ↓  
Knowledge Sources (Assessment + CIS + ISO + Zero Trust)  
        ↓  
AI Reasoning Engine (Prompt-based cross-framework analysis)  
        ↓  
Security Insights (Risk, Compliance, Threat Modeling)

## Components

- Microsoft Copilot Studio: Agent orchestration
- Knowledge Data Sources:
  - Identity assessment dataset (Excel)
  - CIS benchmarks
  - ISO 27001 controls
  - Zero Trust framework
  - Conditional Access baseline
  - Threat models

- AI Reasoning Engine:
  - Structured system prompt
  - Cross-framework correlation logic

- Output Layer:
  - Risk prioritization
  - ISO compliance evaluation
  - Attack simulation
  - Impact analysis

## Future Integration

- Microsoft Graph API
- Entra ID real-time assessments
- Automated remediation workflows

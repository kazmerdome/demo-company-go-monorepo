# Core Data Science

This package is the central domain library for all data science-related logic across the monorepo.  
It provides reusable components, models, and abstractions for data pipelines, ML modeling, and analytics.  

> ⚠️ This package is not a standalone application. It is intended to be imported and used by services within the monorepo.

## Purpose

- Provide a centralized, reusable library for all Data Science components
- Encapsulate domain logic related to predictions, experiments, and data preprocessing
- Maintain clear, testable modules that can be composed by other internal systems

## Structure
```
core-data-science/
├── prediction/ # Prediction model interfaces and logic
│ └── churn.go
├── preprocessing/ # Data transformation and feature engineering
│ └── cleaner.go
├── experiment/ # A/B testing and experimentation utilities
│ └── ab_test.go
├── metrics/ # Common DS-related metrics and evaluation logic
│ └── evaluator.go
├── internal/ # Internal helpers (non-exported)
│ └── utils.go
└── README.md # You're here
```

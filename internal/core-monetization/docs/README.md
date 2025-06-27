# Core Monetization

This package serves as the central domain library for all monetization-related logic across the monorepo.
It offers reusable components, models, and abstractions to manage billing, pricing, and revenue analytics. 

> ⚠️ This package is not a standalone application. It is intended to be imported and used by services within the monorepo.

## Purpose

- Provide a centralized, reusable library for all Monetization components
- Encapsulate domain logic related to billing workflows, pricing strategies, and revenue tracking
- Maintain modular, testable code to be integrated seamlessly with other internal services

## Structure
```
core-monetization/
├── billing/       # Billing processes and invoicing logic
│   └── invoice.go
├── pricing/       # Pricing rules and discount models
│   └── discount.go
├── analytics/     # Revenue and monetization metrics
│   └── revenue.go
├── subscription/  # Subscription management utilities
│   └── subscription.go
├── internal/      # Internal helpers (non-exported)
│   └── helpers.go
└── README.md      # You're here
```

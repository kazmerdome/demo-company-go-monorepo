# Core Monetization

This package is the central domain library for all product-related logic within the monorepo.
It provides reusable components, models, and abstractions for product management, catalog handling, and inventory tracking.

> ⚠️ This package is not a standalone application. It is intended to be imported and used by services within the monorepo.

## Purpose

- Provide a centralized, reusable library for all Product components
- Encapsulate domain logic related to product lifecycle, categorization, and stock management
- Maintain clean, modular, and testable code that integrates with other internal systems

## Structure
```
core-product/
├── catalog/       # Product catalog models and logic
│   └── item.go
├── inventory/     # Stock and warehouse management
│   └── stock.go
├── pricing/       # Product pricing rules and adjustments
│   └── pricing.go
├── review/        # Customer product reviews and ratings
│   └── review.go
├── internal/      # Internal helpers (non-exported)
│   └── utils.go
└── README.md      # You're here
```

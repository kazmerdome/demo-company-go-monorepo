# Cohort Worker Application

cohort-worker is a background worker service responsible for processing user cohorts and generating cohort-based analytics.
It operates as part of the monorepo ecosystem, relying on core domain libraries to perform data science computations and product-related data enrichment.


## Purpose

- Process and update user cohorts periodically
- Generate cohort analytics reports used by other systems
- Integrate with core-data-science and core-product domains for data enrichment and modeling


## Domain Dependencies
This service depends on the following core packages within the monorepo:

- core-data-science
  For accessing data preprocessing, prediction models, and experiment logic required to analyze cohort data.

- core-product
  For product metadata, catalog information, and inventory data that enrich cohort profiles with product-related insights.


## Structure
```
cmd/cohort-worker/
├── main.go          # Entry point of the worker application
├── config.go        # Configuration loader and environment variables
├── processor.go     # Core logic for cohort processing
├── reporter.go      # Cohort analytics report generation
└── README.md        # You're here
```

## Running the Cohort Worker

### Prerequisites

- Go 1.20+ installed
- Access to monorepo's core-data-science and core-product packages
- Proper environment variables or config files set (see below)


### Configuration

The worker requires the following environment variables for proper operation, lorem ipsum

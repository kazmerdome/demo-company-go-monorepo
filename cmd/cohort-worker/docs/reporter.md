# Reporter Module

The `reporter.go` module is responsible for generating and exporting cohort analytics reports.  
It collects processed cohort data, computes key metrics, and prepares summaries for consumption by other services and dashboards.

## Key Responsibilities

- Aggregate cohort data from the processor output  
- Calculate analytics metrics such as retention, churn rate, and conversion  
- Format reports in predefined templates or data structures  
- Export reports to external systems or storage for further analysis  

## Important Functions

- `FetchCohortData()` – Retrieves processed cohort information  
- `ComputeMetrics()` – Calculates essential cohort statistics  
- `GenerateReport()` – Creates formatted report outputs  
- `ExportReport()` – Sends reports to reporting endpoints or file storage  

## Dependencies

The reporter relies on the following packages:

- `core-data-science` for metric calculations and evaluation logic  
- `core-product` for enriching reports with product-related metadata  

## Usage Notes

The reporter typically runs after the processor completes cohort updates and can be triggered manually or scheduled as part of the cohort-worker service workflow.

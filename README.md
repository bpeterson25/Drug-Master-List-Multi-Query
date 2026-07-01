# DrugMaster Query – Multi-Drug Search

## Overview

DrugMaster Multi-Drug Query extends the single-drug search capability by allowing users to analyze multiple drugs simultaneously.

The notebook aggregates product, package, clinical, and labeling information across a portfolio of drugs.

This notebook is intended for market assessments, competitive evaluations, and formulary analysis.

---

## Example Usage

```python
drug_list = [
    "Opdivo",
    "Keytruda",
    "Yervoy"
]

multi_results = search_drugs(drug_list)
```

---

## Business Use Cases

### Medical Economics

- Market basket analysis
- Competitive intelligence
- Oncology portfolio reviews
- Drug category assessments

### Formulary Strategy

- Therapeutic category review
- Manufacturer concentration analysis
- Package size comparison

### Pharmacy Analytics

- Landscape monitoring
- Product availability analysis
- Drug repository development

---

## Data Sources

### OpenFDA

Provides:

- Product-level information
- Package-level information
- Manufacturer details

### DailyMed

Provides:

- Label metadata
- SPL information

### RxNorm

Provides:

- Clinical relationships
- Standardized drug concepts

---

## Portfolio Outputs

### Products

One row per FDA product.

### Packages

One row per package configuration.

### Ingredients

Ingredient-level detail.

### Package Analytics

Parsed package information including:

- Quantity
- Unit
- Container Type

### Drug Repository

Consolidated portfolio table.

---

## Portfolio Repository Example

The resulting repository may include:

| Field |
|---------|
| Brand Name |
| Generic Name |
| Ingredient |
| Product NDC |
| Package NDC |
| Package Description |
| Manufacturer |
| Dosage Form |
| Route |
| Application Number |
| Marketing Category |

---

## Export Capability

```python
export_excel(
    multi_results,
    "ImmunoOncologyPortfolio"
)
```

Output:

```text
DrugMaster_ImmunoOncologyPortfolio.xlsx
```

---

## Strategic Roadmap

This notebook serves as the bridge between:

### Query Layer

```text
DrugMaster Query
```

and

### Repository Layer

```text
DrugMaster Builder
```

Future repository assets:

```text
products.parquet
packages.parquet
ingredients.parquet
repository.parquet
```

These assets will support:

- Formulary Analytics
- Medical Economics
- Value-Based Pharmacy
- Competitive Intelligence
- Drug Market Monitoring

---

## Audience

- Medical Economics
- Pharmacy Analytics
- Clinical Strategy
- Formulary Management
- Market Access
- Value-Based Care Teams

---

## Author

DrugMaster Initiative

Building a normalized drug intelligence repository from public domain drug data sources.

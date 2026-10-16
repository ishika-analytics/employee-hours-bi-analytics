# Employee Hours BI Portfolio Project

## Purpose
Synthetic business intelligence project designed for practicing:
- Power BI data modeling
- Power Query transformations
- DAX measures
- Filter context and CALCULATE
- Row-Level Security
- Dashboard design
- Git/GitHub documentation

## Data model

```text
Dim Employee     1 ───── * Fact Hours * ───── 1 Dim Program
                         |
                         |
                         * 
                         |
                     1 Dim Activity

Dim Date         1 ───── * Fact Hours
```

Recommended relationship direction:
- Dimensions -> Fact: Single direction
- Cardinality: 1:* for the standard dimension/fact relationships

### Fact grain
**One row in `fact_hours.csv` represents hours recorded for one employee, one program, one activity, on one date.**

### Important modeling decision
Department is stored as an attribute in the Employee dimension rather than as a separate dimension in this first version.

## Files

- `employees.csv` — Employee dimension
- `programs.csv` — Program dimension
- `activities.csv` — Activity dimension
- `dates.csv` — Date dimension
- `fact_hours.csv` — Hours fact table

## Dataset size
- Employees: 50
- Programs: 8
- Activities: 12
- Dates: 638
- Fact rows: 2889

## Portfolio roadmap
1. Load and profile data
2. Build the star schema
3. Create core measures
4. Practice filter context and CALCULATE
5. Add time intelligence
6. Build an executive dashboard
7. Add RLS
8. Document design decisions
9. Publish project artifacts to GitHub

> All data in this project is synthetic and created for portfolio/learning purposes.

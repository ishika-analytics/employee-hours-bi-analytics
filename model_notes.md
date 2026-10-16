# Model Notes

## Recommended relationships

| From | To | Cardinality | Cross-filter |
|---|---|---|---|
| Dim Employee | Fact Hours | 1:* | Single |
| Dim Program | Fact Hours | 1:* | Single |
| Dim Activity | Fact Hours | 1:* | Single |
| Dim Date | Fact Hours | 1:* | Single |

## Core DAX measures for later lessons

```DAX
Total Hours =
SUM(Fact_Hours[Hours])

Average Hours per Employee =
AVERAGEX(
    VALUES(Employee[EmployeeKey]),
    [Total Hours]
)

Employee Count =
DISTINCTCOUNT(Fact_Hours[EmployeeKey])
```

Do not build all advanced measures at once. We will add them lesson by lesson.

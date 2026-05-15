# SemanticSearchHistoryAppliedDateRange

Echoed back only when the caller passed `startDate` and/or `endDate`.
Each bound is an ISO 8601 string when set; the field is absent when
the corresponding query param was omitted (utils.ts:480-486 reads
`appliedFilters.createdAt.$gte?.toISOString()` directly, so missing
bounds become `undefined` and drop out of the JSON).



## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `Start`                                    | [*time.Time](https://pkg.go.dev/time#Time) | :heavy_minus_sign:                         | N/A                                        |
| `End`                                      | [*time.Time](https://pkg.go.dev/time#Time) | :heavy_minus_sign:                         | N/A                                        |
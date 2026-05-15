# Feedback

The feedback entry just appended to the message. Echoes
the fields supplied in the request plus server-stamped
`feedbackProvider`, `timestamp`, and `metrics`.



## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `IsHelpful`                                                                        | **bool*                                                                            | :heavy_minus_sign:                                                                 | Echoed from the request when supplied.                                             |
| `Ratings`                                                                          | map[string]*float64*                                                               | :heavy_minus_sign:                                                                 | Echoed per-aspect ratings (values 1–5).                                            |
| `Categories`                                                                       | [][operations.CategoryResponse](../../models/operations/categoryresponse.md)       | :heavy_minus_sign:                                                                 | Echoed categories from the request.                                                |
| `Comments`                                                                         | [*operations.CommentsResponse](../../models/operations/commentsresponse.md)        | :heavy_minus_sign:                                                                 | Echoed free-text comments from the request.                                        |
| `FeedbackProvider`                                                                 | *string*                                                                           | :heavy_check_mark:                                                                 | User who submitted the feedback. Always present.                                   |
| `Timestamp`                                                                        | *int64*                                                                            | :heavy_check_mark:                                                                 | Submission time as epoch milliseconds (not an ISO 8601<br/>datetime). Always present.<br/> |
| `Metrics`                                                                          | [operations.MetricsResponse](../../models/operations/metricsresponse.md)           | :heavy_check_mark:                                                                 | Telemetry recorded server-side alongside the feedback.<br/>Always present.<br/>    |
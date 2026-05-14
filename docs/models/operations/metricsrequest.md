# MetricsRequest

Optional client-supplied telemetry.


## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `UserInteractionTime`                                                          | **float64*                                                                     | :heavy_minus_sign:                                                             | Total time the user spent reviewing the response, in milliseconds.             |
| `FeedbackSessionID`                                                            | **string*                                                                      | :heavy_minus_sign:                                                             | Opaque session identifier used by the client to group related feedback events. |
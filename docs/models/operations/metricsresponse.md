# MetricsResponse

Telemetry recorded server-side alongside the feedback.
Always present.



## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `TimeToFeedback`                                                                | *float64*                                                                       | :heavy_check_mark:                                                              | Milliseconds between message creation and feedback<br/>submission. Always present.<br/> |
| `UserInteractionTime`                                                           | **float64*                                                                      | :heavy_minus_sign:                                                              | Echoed from `metrics.userInteractionTime` in the request when supplied.         |
| `FeedbackSessionID`                                                             | **string*                                                                       | :heavy_minus_sign:                                                              | Echoed from `metrics.feedbackSessionId` in the request when supplied.           |
| `UserAgent`                                                                     | **string*                                                                       | :heavy_minus_sign:                                                              | Value of the `User-Agent` request header captured server-side.                  |
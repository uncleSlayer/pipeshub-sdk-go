# KnowledgeHubNodesResponseFilters


## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `Applied`                                                    | [components.Applied](../../models/components/applied.md)     | :heavy_check_mark:                                           | Echo of applied filters; unused slots are JSON `null`.       |
| `Available`                                                  | [components.Available](../../models/components/available.md) | :heavy_check_mark:                                           | Populated when `include=availableFilters`; otherwise `null`. |
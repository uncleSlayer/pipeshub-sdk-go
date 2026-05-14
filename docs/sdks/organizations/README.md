# Organizations

## Overview

### Available Operations

* [GetCurrentOrganization](#getcurrentorganization) - Get current organization

## GetCurrentOrganization

Retrieve details about the authenticated user's organization.<br><br>
<b>Overview:</b><br>
This endpoint returns complete information about the current user's organization, including profile data, settings, and configuration. Use this for organization profile pages and settings.<br><br>
<b>Response Includes:</b><br>
<ul>
<li>Organization profile (name, email, address)</li>
<li>Account type and billing status</li>
<li>Feature flags and limits</li>
<li>Branding settings (logo, colors)</li>
<li>Creation and modification timestamps</li>
</ul>
<b>Use Cases:</b><br>
<ul>
<li>Organization profile pages</li>
<li>Settings and configuration screens</li>
<li>Billing and subscription displays</li>
<li>White-label branding retrieval</li>
</ul>
<b>Note:</b><br>
All authenticated users can access this endpoint to view their organization's details.


### Example Usage

<!-- UsageSnippet language="go" operationID="getCurrentOrganization" method="get" path="/org" -->
```go
package main

import(
	"context"
	"os"
	"github.com/pipeshub-ai/pipeshub-sdk-go/models/components"
	pipeshub "github.com/pipeshub-ai/pipeshub-sdk-go"
	"log"
)

func main() {
    ctx := context.Background()

    s := pipeshub.New(
        pipeshub.WithSecurity(components.Security{
            BearerAuth: pipeshub.Pointer(os.Getenv("PIPESHUB_BEARER_AUTH")),
        }),
    )

    res, err := s.Organizations.GetCurrentOrganization(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.Organization != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetCurrentOrganizationResponse](../../models/operations/getcurrentorganizationresponse.md), error**

### Errors

| Error Type         | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| apierrors.APIError | 4XX, 5XX           | \*/\*              |
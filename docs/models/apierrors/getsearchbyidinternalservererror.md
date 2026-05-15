# GetSearchByIDInternalServerError

Server error. Possible causes:

- Explicit `InternalServerError`
  or any other 500 `BaseError` thrown by the handler.
- Non-`BaseError` exception caught by the
  global error middleware.
- Response serializer fallback.



## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `Error`                                                                                                              | [operations.GetSearchByIDInternalServerErrorError](../../models/operations/getsearchbyidinternalservererrorerror.md) | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `HTTPMeta`                                                                                                           | [components.HTTPMetadata](../../models/components/httpmetadata.md)                                                   | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
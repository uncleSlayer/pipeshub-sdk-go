# AuthenticateResponse

Either the next step in a multi-factor flow (`status`, `nextStep`, `allowedMethods`, `authProviders`)
or final tokens (`message`, `accessToken`, `refreshToken`).



## Supported Types

### AuthenticateMultiStepResponse

```go
authenticateResponse := components.CreateAuthenticateResponseAuthenticateMultiStepResponse(components.AuthenticateMultiStepResponse{/* values here */})
```

### AuthenticateFinalResponse

```go
authenticateResponse := components.CreateAuthenticateResponseAuthenticateFinalResponse(components.AuthenticateFinalResponse{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch authenticateResponse.Type {
	case components.AuthenticateResponseTypeAuthenticateMultiStepResponse:
		// authenticateResponse.AuthenticateMultiStepResponse is populated
	case components.AuthenticateResponseTypeAuthenticateFinalResponse:
		// authenticateResponse.AuthenticateFinalResponse is populated
	default:
		// Unknown type - use authenticateResponse.GetUnknownRaw() for raw JSON
}
```

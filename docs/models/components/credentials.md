# Credentials

Credentials based on the authentication method


## Supported Types

### PasswordCredentials

```go
credentials := components.CreateCredentialsPasswordCredentials(components.PasswordCredentials{/* values here */})
```

### OtpCredentials

```go
credentials := components.CreateCredentialsOtpCredentials(components.OtpCredentials{/* values here */})
```

### OAuthCredentials

```go
credentials := components.CreateCredentialsOAuthCredentials(components.OAuthCredentials{/* values here */})
```

### 

```go
credentials := components.CreateCredentialsStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch credentials.Type {
	case components.CredentialsTypePasswordCredentials:
		// credentials.PasswordCredentials is populated
	case components.CredentialsTypeOtpCredentials:
		// credentials.OtpCredentials is populated
	case components.CredentialsTypeOAuthCredentials:
		// credentials.OAuthCredentials is populated
	case components.CredentialsTypeStr:
		// credentials.Str is populated
}
```

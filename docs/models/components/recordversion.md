# RecordVersion


## Supported Types

### 

```go
recordVersion := components.CreateRecordVersionStr(string{/* values here */})
```

### 

```go
recordVersion := components.CreateRecordVersionNumber(float64{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch recordVersion.Type {
	case components.RecordVersionTypeStr:
		// recordVersion.Str is populated
	case components.RecordVersionTypeNumber:
		// recordVersion.Number is populated
	default:
		// Unknown type - use recordVersion.GetUnknownRaw() for raw JSON
}
```

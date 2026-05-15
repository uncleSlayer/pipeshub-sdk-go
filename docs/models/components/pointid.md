# PointID

Qdrant point identifier attached during vector lookup (shape varies by deployment).


## Supported Types

### 

```go
pointID := components.CreatePointIDStr(string{/* values here */})
```

### 

```go
pointID := components.CreatePointIDInteger(int64{/* values here */})
```

### 

```go
pointID := components.CreatePointIDNumber(float64{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch pointID.Type {
	case components.PointIDTypeStr:
		// pointID.Str is populated
	case components.PointIDTypeInteger:
		// pointID.Integer is populated
	case components.PointIDTypeNumber:
		// pointID.Number is populated
	default:
		// Unknown type - use pointID.GetUnknownRaw() for raw JSON
}
```

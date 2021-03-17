## nullable

nullable is a library with reasonable options for dealing with nullable SQL and JSON values

Types in `nullable` will only be considered null on null input, and will JSON encode to `null`. If you need zero and null be considered separate values, use these.

All types implement: `encoding.TextMarshaler`, `encoding.TextUnmarshaler`, `json.Marshaler`, and `json.Unmarshaler`. A null object's `MarshalText` will return a blank string.

#### nullable.String
Nullable string.

Marshals to JSON null if SQL source data is null. Zero (blank) input will not produce a null String.

#### nullable.Int
Nullable int64. 

Marshals to JSON null if SQL source data is null. Zero input will not produce a null Int.

#### nullable.Float
Nullable float64. 

Marshals to JSON null if SQL source data is null. Zero input will not produce a null Float.

#### nullable.Bool
Nullable bool. 

Marshals to JSON null if SQL source data is null. False input will not produce a null Bool.

### License
BSD

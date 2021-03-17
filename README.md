## null [![GoDoc](https://godoc.org/github.com/guregu/null?status.svg)](https://godoc.org/github.com/guregu/null) [![CircleCI](https://circleci.com/gh/guregu/null.svg?style=svg)](https://circleci.com/gh/guregu/null)
`import "gopkg.in/guregu/null.v4"`

null is a library with reasonable options for dealing with nullable SQL and JSON values

Types in `null` will only be considered null on null input, and will JSON encode to `null`. If you need zero and null be considered separate values, use these.

All types implement `sql.Scanner` and `driver.Valuer`, so you can use this library in place of `sql.NullXXX`.
All types also implement: `encoding.TextMarshaler`, `encoding.TextUnmarshaler`, `json.Marshaler`, and `json.Unmarshaler`. A null object's `MarshalText` will return a blank string.

### null package

`import "gopkg.in/guregu/null.v4"`

#### null.String
Nullable string.

Marshals to JSON null if SQL source data is null. Zero (blank) input will not produce a null String.

#### null.Int
Nullable int64. 

Marshals to JSON null if SQL source data is null. Zero input will not produce a null Int.

#### null.Float
Nullable float64. 

Marshals to JSON null if SQL source data is null. Zero input will not produce a null Float.

#### null.Bool
Nullable bool. 

Marshals to JSON null if SQL source data is null. False input will not produce a null Bool.

### License
BSD

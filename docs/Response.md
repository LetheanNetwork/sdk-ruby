# LthnApi::Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | **Object** |  | [optional] |
| **error** | [**Error**](Error.md) |  | [optional] |
| **meta** | [**Meta**](Meta.md) |  | [optional] |
| **success** | **Boolean** |  |  |

## Example

```ruby
require 'lthn_api'

instance = LthnApi::Response.new(
  data: null,
  error: null,
  meta: null,
  success: null
)
```


# tostring

The `tostring()` function converts its argument to a string format.

#### Syntax

```lua
tostring(value)
```

#### Parameters

* **value**: The value to be converted to a string.

#### Returns

* Returns the string representation of the given value.

#### Example

```lua
local num = 123
local str = tostring(num)
print(type(str))  -- Output: string
```

#### Notes

* If the value is already a string, `tostring()` will return the value unchanged.
* For tables, it returns a string with the format "table: `address`". Use a `__tostring` metamethod for custom string representations.

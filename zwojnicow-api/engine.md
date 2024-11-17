---
icon: engine
cover: ../.gitbook/assets/Zrzut ekranu 2024-11-17 140853.png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Engine

### Log Function

The **`log`** function prints an object to the console for debugging purposes.

```lua
---@param obj any
---Prints an object to the console.
function log(obj) end
```

#### Parameters

* `obj`\
  The object to be printed to the console. This can be of any type.

### MessageBoxType Enumeration

`MessageBoxType` is an enumeration that specifies the different types of message boxes available.

* `AbortRetryIgnore`: Value `0`
* `CancelTryContinue`: Value `1`
* `Help`: Value `2`
* `OK`: Value `3`
* `OKCancel`: Value `4`
* `RetryCancel`: Value `5`
* `YesNo`: Value `6`
* `YesNoCancel`: Value `7`

### MessageBoxResponse Enumeration

`MessageBoxResponse` is an enumeration that specifies the possible responses from a message box.

* `OK`: Value `0`
* `Cancel`: Value `1`
* `Abort`: Value `2`
* `Retry`: Value `3`
* `Ignore`: Value `4`
* `Yes`: Value `5`
* `No`: Value `6`
* `TryAgain`: Value `7`

### msgbox Function

The `msgbox` function displays a Windows message box with specified text, caption, and type, and returns the user's response.

```lua
---@param text string
---@param caption string
---@param type MessageBoxType
---@return MessageBoxResponse
---Shows Windows message box.
function msgbox(text, caption, type) end
```

#### Parameters

* `text`: The message to be displayed in the message box.
* `caption`: The title of the message box window.
* `type`: The type of the message box, specified using `MessageBoxType`.

#### Returns

* `MessageBoxResponse`: The response from the message box interaction.

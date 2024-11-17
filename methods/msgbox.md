# msgbox

## MsgBox Method

The `MsgBox` method displays a native message box that shows a message, a caption, and a specified type of buttons, returning the user's response.

### **Syntax**

```plaintext
MsgBox(message, caption, type)
```

* **`message`**: The text to display in the message box. Required.
* **`caption`**: The text for the title of the message box. Required.
* **`type`**: Specifies the buttons and icons to display, using `MessageBoxType`. Required.

### **Enums**

* `MessageBoxType`: Determines the set of buttons displayed.
  * `AbortRetryIgnore` = 0
  * `CancelTryContinue` = 1
  * `Help` = 2
  * `OK` = 3
  * `OKCancel` = 4
  * `RetryCancel` = 5
  * `YesNo` = 6
  * `YesNoCancel` = 7
* `MessageBoxResponse`: Possible responses from the user.
  * `OK` = 0
  * `Cancel` = 1
  * `Abort` = 2
  * `Retry` = 3
  * `Ignore` = 4
  * `Yes` = 5
  * `No` = 6
  * `TryAgain` = 7

### Example usage

```lua
local response = MsgBox("Hello :)", "Zwojnicow", MessageBoxType.YesNoCancel)

if response == MessageBoxResponse.Yes then
    log("Hello, World!")
end
```

<figure><img src="../.gitbook/assets/Zrzut ekranu 2024-11-17 190133.png" alt=""><figcaption><p>MessageBox in-game</p></figcaption></figure>



In this example, the message box asks the user about saving changes, and the response will be one of the `MessageBoxResponse` values.

{% hint style="warning" %}
It's important to note that displaying a message box can cause the application to halt its normal execution. Therefore, this method is typically not recommended for use in production environments where smooth operation is crucial.
{% endhint %}




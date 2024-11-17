---
icon: bolt-lightning
---

# Event

The `Event` class serves as a mechanism for managing events, providing the ability to connect, trigger, and disconnect callback functions. This documentation outlines the methods available within the `Event` class, allowing developers to interact with events effectively.

### Methods

#### Connect

Connects a callback function to the event.

* **Syntax**: `Event:Connect(callback)`
* **@param** `callback function`: The function that will be invoked when the event is triggered.

This method allows you to attach a function that will be called whenever the event fires. It's particularly useful when you want to execute specific code in response to an event occurrence.

#### Fire

Triggers the event, invoking all connected callback functions with any provided arguments.

* **Syntax**: `Event:Fire(...)`

When you want all the connected functions to execute, you use the `Fire` method. It can also pass any number of arguments to the connected callback functions, which can be used within those functions.

#### Disconnect

Disconnects a previously connected callback function from the event.

* **Syntax**: `Event:Disconnect(callback)`
* **@param** `callback function`: The function to be disconnected from the event.

This method is used when you no longer want a particular function to respond to the event. It removes the function from the list of callbacks, ensuring it won't be called when the event is next fired.

#### Return

* **returns** `Event`: Returns the event instance.

The methods in the `Event` class work with the event instance, allowing developers to maintain a clear and organized event handling process. By working with events, developers can ensure that their applications respond dynamically to user actions and other occurrences.

#### Usage Example

To effectively use the `Event:Disconnect(callback)` method, consider the following example:

```lua
local event = Event.new()

local function OnEventTriggered()
    print("Event has been triggered!")
end

-- Connecting the function to the event
event:Connect(onEventTriggered)

-- Later in the code, disconnect the function
event:Disconnect(onEventTriggered)
```

In this example, the `onEventTriggered` function is first connected to the event and then later disconnected using the `Event:Disconnect` method. This ensures that once the function is no longer needed, it is properly removed from the event's callback list, optimizing memory usage and performance.

{% hint style="info" %}
Using the `Event:Disconnect` method is crucial for managing event listeners efficiently within your application. This is particularly important in long-running applications where failing to disconnect unused callbacks can lead to memory leaks or unexpected behavior due to lingering event listeners.
{% endhint %}


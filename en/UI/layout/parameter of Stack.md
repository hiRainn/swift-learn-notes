### Attribute of Stack

#### .spacing

The ``spacing`` parameter is often used in SwiftUI’s layout containers like ``VStack``, ``HStack``, and ``LazyVStack`` to control the spacing between child views along the container’s main axis.

Usage: When you create a VStack/HStack/LazyVStack, you can specify the spacing parameter to set the distance between child views. For example:

```swift
VStack(spacing: 20) {
    Text("Hello")
    Text("World")
}
```

In this example, there will be 20 points of spacing between "Hello" and "World".

Use Cases: The ``spacing`` parameter is useful in many scenarios where you need to control the distance between views. For example, you might want to increase the spacing between elements in a list for better readability, or decrease the spacing to fit more content on the screen.

Applicable Layouts: The ``spacing`` parameter can be used with any layout that arranges views along a single axis, including ``VStack`` (for vertical stacks), ``HStack`` (for horizontal stacks), and ``LazyVStack`` (for lazily loaded vertical stacks). It is not applicable to ``ZStack``, which overlays views on top of each other, because the concept of spacing between overlaid views does not apply.
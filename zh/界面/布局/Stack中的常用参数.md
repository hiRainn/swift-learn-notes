### Stack中的常用属性

#### .spacing

``spacing`` 参数常用于 SwiftUI 的布局容器，如 ``VStack``，``HStack`` 和 ``LazyVStack``，用于控制沿容器主轴的子视图之间的间距。

使用方法：当你创建 VStack/HStack/LazyVStack 时，你可以指定 ``spacing`` 参数来设置子视图之间的距离。例如：

```swift
VStack(spacing: 20) {
    Text("Hello")
    Text("World")
}
```

在这个例子中，"Hello" 和 "World" 之间将有 20 点的间距。

使用场景：``spacing`` 参数在许多需要控制视图之间距离的场景中都非常有用。例如，你可能希望增加列表元素之间的间距以提高可读性，或者减小间距以在屏幕上显示更多内容。

适用布局：``spacing`` 参数可以用于任何沿单一轴排列视图的布局，包括 ``VStack``（用于垂直堆栈），``HStack``（用于水平堆栈）和 ``LazyVStack``（用于延迟加载的垂直堆栈）。它不适用于 ``ZStack``，因为 ``ZStack`` 将视图叠加在一起，间距的概念并不适用。


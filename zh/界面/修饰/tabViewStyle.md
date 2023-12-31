### tabViewStyle

在SwiftUI中，``.tabViewStyle``用于指定TabView的样式。通过使用不同的tabViewStyle，可以改变TabView的外观和交互方式。常用的tabViewStyle包括PageTabViewStyle、DefaultTabViewStyle、以及其他自定义的样式。

下面是一个示例，展示了如何使用``.tabViewStyle``来设置TabView的样式：

```swift
TabView {
    Text("First Tab")
        .tabItem {
            Image(systemName: "1.square.fill")
            Text("First")
        }
    Text("Second Tab")
        .tabItem {
            Image(systemName: "2.square.fill")
            Text("Second")
        }
}
.tabViewStyle(PageTabViewStyle())
```

在这个示例中，我们使用``.tabViewStyle(PageTabViewStyle())``来将TabView的样式设置为页面样式，这意味着用户可以通过左右滑动来浏览不同的选项卡内容。

常用的tabViewStyle包括以下几种：
1. PageTabViewStyle：页面样式，允许用户通过左右滑动来浏览不同的选项卡内容
2. DefaultTabViewStyle：默认样式，通常显示为选项卡式的标签，用户可以通过点击不同的选项卡来切换内容
3. StackTabViewStyle：堆叠样式，以堆叠的方式显示选项卡，特别适合于较少的选项卡
4. DoubleColumnTabViewStyle：双列样式，适合于在iPad等较大屏幕上显示多个选项卡

除了以上内置的tabViewStyle，你还可以通过创建自定义的tabViewStyle来定制TabView的外观和交互方式。自定义的tabViewStyle通常需要遵循TabViewStyle协议，并实现相应的样式逻辑。

总之，通过使用.tabViewStyle，你可以轻松地改变TabView的外观和交互方式，从而为用户提供更丰富的用户体验。
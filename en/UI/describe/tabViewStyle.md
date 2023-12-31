### tabViewStyle

In SwiftUI, the ``.tabViewStyle`` modifier is used to specify the style of a TabView. By applying different tabViewStyle modifiers, you can change the appearance and interaction behavior of the TabView. Common tabViewStyle options include PageTabViewStyle, DefaultTabViewStyle, as well as custom styles.

Here is an example that demonstrates how to use ``.tabViewStyle`` to set the style of a TabView:

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

In this example, we use ``.tabViewStyle(PageTabViewStyle())`` to set the style of the TabView to a page style, allowing users to navigate through different tabs by swiping left or right.

Commonly used tabViewStyle options include:

1. PageTabViewStyle: Page style that allows users to navigate through different tabs by swiping left or right.
2. DefaultTabViewStyle: Default style that typically displays as tabbed labels, allowing users to switch content by clicking on different tabs.
3. StackTabViewStyle: Stack style that displays tabs in a stacked manner, suitable for a smaller number of tabs.
4. DoubleColumnTabViewStyle: Double-column style, suitable for displaying multiple tabs on larger screens such as iPad.

In addition to the built-in tabViewStyle options, you can create custom tabViewStyles to customize the appearance and interaction behavior of the TabView. Custom tabViewStyles typically need to conform to the TabViewStyle protocol and implement the corresponding styling logic.

In summary, by using ``.tabViewStyle``, you can easily change the appearance and interaction behavior of the TabView, providing users with a richer user experience.

### TabView

在Swift中，TabView是一种用于在应用程序中显示多个视图的容器视图。它通常用于创建具有选项卡式导航的用户界面，用户可以通过点击不同的选项卡来浏览不同的内容

TabView的常用参数包括：

- selection：表示当前选定的选项卡的绑定状态。可以使用@State或@Binding属性来跟踪所选选项卡的状态
- content：表示TabView中包含的视图。通常是一个包含多个Tab标签的视图，每个标签对应一个选项卡
- tag：表示每个选项卡的唯一标识符。通常与selection绑定状态一起使用，以确定当前选项卡的标识符

TabView的用法通常包括创建一个TabView实例，并在其中定义多个Tab标签，每个标签对应一个选项卡。每个标签通常包含一个目标视图和一个标识符，以便TabView可以根据用户的选择进行导航。

示例如下：

```swift
struct ContentView: View {
    @State private var selectedTab: Int = 0
    
    var body: some View {
        TabView(selection: $selectedTab) {
            Text("First View")
                .tabItem {
                    Image(systemName: "1.square.fill")
                    Text("First")
                }
                .tag(0)
            
            Text("Second View")
                .tabItem {
                    Image(systemName: "2.square.fill")
                    Text("Second")
                }
                .tag(1)
        }
    }
}
```

在这个示例中，我们创建了一个TabView，其中包含两个选项卡。每个选项卡都有一个与之相关联的标签和唯一的标识符。用户可以通过点击不同的选项卡来浏览不同的内容。

TabView的常见用途包括：

1. 应用程序的主导航界面，用于展示不同的功能模块或内容
2. 创建具有选项卡式导航的用户界面，例如设置页面、个人资料页面、消息页面等
3. 在应用程序中实现多个功能模块之间的切换，例如展示不同的数据视图、图表视图等

#### 非常规用法

除了作为常规的选项卡式导航界面之外，TabView还可以用于以下非常规的用法：

1. 类似日历的翻页工具：可以使用TabView来创建类似日历的翻页工具，每个选项卡代表一个页面或日期，用户可以通过左右滑动或点击不同的选项卡来浏览不同的日期或内容
2. 引导页：TabView可以用作应用程序的引导页，每个选项卡代表引导页中的一个页面或步骤。用户可以通过滑动或点击不同的选项卡来浏览引导内容，并完成引导过程
3. 表单向导：将TabView用作表单向导，每个选项卡代表表单中的一个部分或步骤。用户可以依次填写每个步骤的内容，通过点击不同的选项卡来切换到下一个或上一个步骤
4. 图片浏览器：TabView可以用作图片浏览器，每个选项卡代表一个图片或图片集合。用户可以通过左右滑动或点击不同的选项卡来浏览不同的图片
5. 多语言支持：TabView可以用于显示不同语言的内容，每个选项卡代表不同语言的内容页面。用户可以通过点击不同的选项卡来切换到不同语言的内容

总之，TabView可以根据具体的需求和创意，灵活地应用于各种非常规的场景中，扩展其用法并提供更丰富的用户体验。

[tabViewStyle的使用](https://github.com/hiRainn/swift-learn-notes/blob/master/zh/%E7%95%8C%E9%9D%A2/%E4%BF%AE%E9%A5%B0/tabViewStyle.md)

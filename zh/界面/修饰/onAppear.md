### onAppear

在SwiftUI中，.onAppear是一个ViewModifier，用于在视图出现在屏幕上时执行特定的操作。当包含.onAppear修饰符的视图在屏幕上首次出现时，指定的操作将被触发。这在需要在视图加载后立即执行某些操作时非常有用，比如异步加载数据或执行一些初始化操作。

例如，可以使用.onAppear来触发网络请求，加载数据，或者执行其他需要在视图加载后立即执行的操作。这样可以确保在视图显示给用户之前，数据已经准备好并可以立即显示。

示例代码如下：

```Swift
struct ContentView: View {
    @State private var data: [String] = []

    var body: some View {
        List(data, id: \.self) { item in
            Text(item)
        }
        .onAppear {
            fetchData()
        }
    }

    func fetchData() {
        // Perform data fetching here
        // Update the data state with fetched data
    }
}
```

在这个例子中，当ContentView首次出现在屏幕上时，.onAppear修饰符将触发fetchData方法，从而加载数据并更新界面。


### self.attribute与self.$attribute

在SwiftUI中，使用self.attribute和self.$attribute有着不同的作用和用法。

#### self.attribute:

当我们使用self.attribute时，我们是在访问视图的状态属性或普通属性。这意味着我们只是获取或设置属性的当前值，而不会创建绑定。这通常用于在视图内部访问和修改其自身的状态。

```Swift
struct ContentView: View {
    @State private var counter = 0
    
    var body: some View {
        Button("Increment") {
            self.counter += 1 // 使用self.attribute来访问和修改视图的状态属性
        }

        if self.counter > 5 {
            Text("hello swift")
        }
    }
}
```

#### self.$attribute:

当我们使用self.$attribute时，我们是在创建一个绑定，用于将属性的值与其他视图或控件进行双向绑定。这允许属性的值在不同的视图之间同步更新。

```Swift
struct ContentView: View {
    @State private var text = ""
    
    var body: some View {
        ChildView(text: self.$text) // 使用self.$attribute来创建绑定并将属性传递给子视图
    }
}

struct ChildView: View {
    @Binding var text: String
    
    var body: some View {
        TextField("Enter text", text: self.$text) // 在子视图中使用绑定的属性
    }
}
```

总的来说，使用self.attribute用于访问和修改视图内部的状态属性，而使用self.$attribute用于创建绑定并在视图之间传递和同步属性的值。
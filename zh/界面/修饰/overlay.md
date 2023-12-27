### overlay

在 SwiftUI 中，overlay 是一种用于在视图上添加叠加层的修饰符。它允许您在现有的视图上方添加额外的内容，比如文本、形状、图像等，从而实现视图的叠加效果。

overlay 修饰符通常用于在现有的视图上添加附加的视觉效果、标签、图标等。下面是一个简单的示例，演示了如何使用 overlay 在一个矩形视图上添加文本标签：

```Swift
struct ContentView: View {
    var body: some View {
        Rectangle()
            .fill(Color.blue)
            .frame(width: 200, height: 100)
            .overlay(
                Text("Overlay Text")
                    .foregroundColor(.white)
            )
    }
}
```

在这个示例中，我们创建了一个蓝色的矩形视图，并使用 overlay 修饰符在其上方添加了一个文本标签。这样，文本标签就会叠加在矩形视图上，从而实现了一个视觉效果。

除了文本，您也可以在 overlay 中添加其他类型的视图，比如形状、图像、按钮等，以实现不同的叠加效果。

总之，overlay 修饰符是 SwiftUI 中用于在视图上方添加叠加层的一种方便机制，可以帮助您实现更丰富的视觉效果和交互效果。


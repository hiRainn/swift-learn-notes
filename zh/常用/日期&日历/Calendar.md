### Calendar

以下示例为生成一周的日期，第一天为周日的代码

```Swift
func getWeekDays(_ date: Date = .init())
    let calendar = Calendar.current
    let startDate = calendar.startOfDay(for: date)
    calendar.firstWeekday = 1 
    var week: [WeekDay] = []
    let weekForDate = calendar.dateInterval(of: .weekOfMonth, for: startDate)

    guard let startOfWeek = weekForDate?.start else {
        return []
    }
    (0..<7).forEach { index in
        if let weekDay = calendar.date(byAdding: .day,value: index ,to: startOfWeek) {
            week.append(.init(date: weekDay))
        }
    }
    return week
}
```

- Calendar类的startOfDay方法用于获取给定日期的开始时间。这个方法将给定的日期重置为当天的开始时间，即将时间部分设置为午夜（00:00:00），而保留日期部分不变。
- Calendar类的firstWeekday属性可用于设置一周的起始日是星期几。默认情况下，firstWeekday属性的值是1，表示一周的起始日是星期日。可以使用这个属性来更改一周的起始日。
- Calendar类的dateInterval(of:for:)方法用于获取指定日期的时间间隔。它接受两个参数：第一个参数指定要获取的时间间隔的类型，第二个参数是要获取时间间隔的日期。
- dateInterval方法返回一个DateInterval对象，其中包含了所请求的时间间隔的起始日期和结束日期。需要注意的是，DateInterval是一个结构体，它包含了起始日期和结束日期，可以方便地用于执行日期范围的操作，比如计算日期范围的长度或检查某个日期是否在范围内。因此下面的startOfWeek调用了WeekForDate?.start

calendar.date(byAdding:value:to:)方法来计算每一天的日期。这个方法接受三个参数：

- byAdding: .day表示我们要添加的时间单位是天。
- value: index表示要添加的数量，它会在每次迭代中增加1，从而获取一周内的每一天。
- to: startOfWeek表示要将时间添加到哪个日期上，即一周的起始日期。

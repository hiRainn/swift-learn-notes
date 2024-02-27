### Drag Event

In SwiftUI, drag events can be implemented using the DragGesture in the Gesture type, as shown below.

struct CalendarView: View {
    @State private var currentDate: Date = Date()
    @State private var weekDays: [Date.WeekDay] = []
    @State private var isMoveDate: Bool = false

    var body: some View {
        VStack {
            CalendarView() // Use self.weekDays to generate a week's data
        }
        .gesture(
            DragGesture()
                .onChanged { _ in
                    self.isMoveDate = true
                }
                .onEnded { value in
                    if self.isMoveDate {
                        let calendar = Calendar.current
                        let moveX = value.startLocation.x - value.location.x
                        if moveX > 0 {
                            self.currentDate = calendar.date(byAdding: .day, value: 7, to: self.currentDate) ?? self.currentDate
                        } else if moveX < 0 {
                            self.currentDate = calendar.date(byAdding: .day, value: -7, to: self.currentDate) ?? self.currentDate
                        }
                        self.isMoveDate = false
                        self.weekDays = Date.fetchWeekDay(self.currentDate)
                    }
                }
            )
        }
    }
}

This code defines a SwiftUI view called CalendarView. It has a state property called currentDate of type Date, a state property called weekDays of type [Date.WeekDay], and a state property called isMoveDate of type Bool.

In the body property, it returns a vertical stack view that contains a subview called CalendarView, which uses self.weekDays to generate a week’s data.

A drag gesture is added using the gesture modifier. When the gesture changes, the isMoveDate state property is set to true. When the gesture ends, the value of the currentDate state property is updated based on the direction of the gesture, and the weekDays state property is updated using the fetchWeekDay method.

The expression ``let moveX = value.startLocation.x - value.location.x`` is used to calculate the direction of the drag. When ``moveX > 0``, it means dragging to the left; otherwise, it means dragging to the right.
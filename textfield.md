---
description: A control that displays an editable text interface.
---

# TextField

{% embed url="https://developer.apple.com/documentation/swiftui/TextField" %}

### Simple TextField

```swift
struct ContentView: View {
    @State private var searchText = ""
    
    var body: some View {
        TextField("Search...", text: $searchText, onCommit: {
            print("do something")
        })
    }
}
```

### TextField with custom keyboard

```swift
struct ContentView: View {
    @State private var searchText = ""
    
    var body: some View {
        TextField("Search...", text: $searchText, onCommit: {
            print("do something")
        })
            .keyboardType(.numberPad)
            .textContentType(.telephoneNumber) // specify content type
    }
}
```


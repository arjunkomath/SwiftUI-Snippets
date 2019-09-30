---
description: A container that presents rows of data arranged in a single column.
---

# List

{% embed url="https://developer.apple.com/documentation/swiftui/list" %}

### List of Text

```swift
List {
    Text("John Appleseed")
    Text("John Appleseed")
    Text("John Appleseed")
    Text("John Appleseed")
}
```

### List inside [NavigationView](../layout-and-views/navigationview.md)

```swift
NavigationView {
    List {
        Text("John Appleseed")
        Text("John Appleseed")
        Text("John Appleseed")
        Text("John Appleseed")
    }
    .navigationBarTitle("Contacts")
}
```

![List inside NavigationView](../.gitbook/assets/screen-shot-2019-09-30-at-9.24.24-pm.png)

### List using ForEach

```swift
let names: [String] = [
    "Lorretta",
    "Tonie",
    "Leesa",
    "So",
    "Sammy"
]

struct ContentView: View {
    var body: some View {
        List {
            ForEach(names, id: \.self) { name in
                Text(name)
            }
        }
    }
}
```


---
description: An affordance for creating hierarchical view content.
---

# Section

{% embed url="https://developer.apple.com/documentation/swiftui/Section" %}

### Sections in a [List](list.md)

```swift
let names: [String] = [
    "Lorretta",
    "Tonie",
    "Leesa",
    "So",
    "Sammy"
]

struct ContentView: View {
    @State private var userName = ""
    @State private var password = ""
    
    var body: some View {
        List {
            Section(header: Text("Some names")) {
                ForEach(names, id: \.self) { name in
                    Text(name)
                }
            }
            
            Section(header: Text("Some more names")) {
                ForEach(names, id: \.self) { name in
                    Text(name)
                }
            }
        }
    }
}
```

![Sections in a List](.gitbook/assets/screen-shot-2019-09-30-at-9.50.15-pm.png)

### Section in a [Form](form.md)

```swift
struct ContentView: View {
    @State private var userName = ""
    @State private var password = ""
    
    var body: some View {
        NavigationView {
            Form {
                Section(header: Text("Enter your login details")) {
                    TextField("Username", text: $userName)
                    SecureField("Password", text: $password)
                    Button(action: {
                        print("do something")
                    }) {
                        Text("Login")
                    }
                }
            }.navigationBarTitle("Login")
        }
    }
}
```

![Section in a Form](.gitbook/assets/screen-shot-2019-09-30-at-9.53.20-pm.png)


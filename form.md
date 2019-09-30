---
description: >-
  A container for grouping controls used for data entry, such as in settings or
  inspectors.
---

# Form

{% embed url="https://developer.apple.com/documentation/swiftui/form" %}

### Form with [TextField](textfield.md)

```swift
struct ContentView: View {
    @State private var firstName = ""
    @State private var lastName = ""
    
    var body: some View {
        Form {
            Section(header: Text("Enter your name")) {
                TextField("First Name", text: $firstName)
                TextField("Last Name", text: $lastName)
            }
        }
    }
}
```

### Form with Button

```swift
struct ContentView: View {
    @State private var firstName = ""
    @State private var lastName = ""
    
    var body: some View {
        Form {
            Section(header: Text("Enter your name")) {
                TextField("First Name", text: $firstName)
                TextField("Last Name", text: $lastName)
                Button(action: {
                    print("do something")
                }) {
                    Text("Submit")
                }
            }
        }
    }
}
```

### Simple Login Form with SecureField

```swift
struct ContentView: View {
    @State private var userName = ""
    @State private var password = ""
    
    var body: some View {
        Form {
            Section(header: Text("Welcome")) {
                TextField("Username", text: $userName)
                SecureField("Password", text: $password)
                Button(action: {
                    print("do something")
                }) {
                    Text("Login")
                }
            }
        }
    }
}
```


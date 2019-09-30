---
description: A view that displays one or more lines of read-only text.
---

# Text

{% embed url="https://developer.apple.com/documentation/swiftui/text" %}

### Simple Text

```swift
// Any String
Text("Arjun Komath")
// or
Text(contact.name)
```

### Styled Text

```swift
// Style using modifies
Text("SwiftUI is cool")
    .font(.largeTitle) // font size
    .lineSpacing(50) // spacing
    .background(Color.yellow) // add background color
    .foregroundColor(Color.red) // add forground color
```

### Heading and Caption

```swift
VStack() { // a vertical stack
    Text(caller.name)
        .font(.headline)
    Text(caller.phoneNumber)
        .font(.caption)
}
```


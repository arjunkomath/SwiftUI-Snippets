---
description: A view that displays an environment-dependent image.
---

# Image

{% embed url="https://developer.apple.com/documentation/swiftui/image" %}

### Simple Image

```swift
Image(systemName: imageName)
```

### Image using UIImage

```swift
Image(uiImage: UIImage(data: contact.avatarData))
```

### Resize Image with fixed size

```swift
Image(uiImage: UIImage(data: contact.avatarData))
                    .resizable()
                    .frame(width: 40.0, height: 40.0)
                    .aspectRatio(contentMode: .fit)
```

### Image within a clip shape \(Avatar Image\)

```swift
Image(uiImage: UIImage(data: contact.avatarData))
                    .resizable()
                    .frame(width: 40.0, height: 40.0)
                    .aspectRatio(contentMode: .fit)
                    .clipShape(Circle())
```

### Image inside a Button

```swift
Image(uiImage: UIImage(data: contact.avatarData!)!)
                    .renderingMode(.original)
```


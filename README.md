# SeismicLib

SeismicLib is a lightweight Swift library that provides an easy interface for connecting to an MQTT broker and subscribing to seismic activity data streams.

## 📦 Features

- Connect to an MQTT broker
- Subscribe to topics
- Handle real-time incoming seismic messages
- Easy integration with any iOS app

## ⚙️ Requirements

- iOS 14.0+
- Swift 5+
- Xcode 15+

## 🚀 Installation

### Manual
1. Clone the repository:
    ```bash
    git clone https://github.com/Sianwa/SeismicLib.git
    ```
2. Drag and drop `SeismicLib.xcodeproj` into your workspace.

### Swift Package Manager (Coming Soon)

## 🛠 Usage

```swift
import SeismicLib

.....

 // Add target action for the button
 executeButton.addTarget(self, action: #selector(loadLibrary), for: .touchUpInside)

.....

 @objc private func loadLibrary(){
        do {
            try Seismic.instance.subscribe(previousUIViewController:self){
                completion in
                    self.showResponse(message: completion)
            }
        } catch {
            self.showResponse(message: error.localizedDescription)
        }
        
    }

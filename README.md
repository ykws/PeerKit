# PeerKit

## An open-source Swift framework for building event-driven, zero-config Multipeer Connectivity apps

## Installation

### CocoaPods

You can use CocoaPods to install YourLibrary by adding it to your Podfile:

```
platform :ios, '8.0'
use_frameworks!
pod 'PeerKit'
```

## Usage

```swift
// Automatically detect and attach to other peers with this service type
PeerKit.transceive(serviceType: "com-jpsim-myApp")

enum Event: String {
    case StartGame, EndGame
}

// Send a StartGame event with attached data to all peers
PeerKit.sendEvent(Event.StartGame.rawValue, object: ["myInfo": "hello!"])
```

See the [CardsAgainst](https://github.com/jpsim/CardsAgainst) app for example usage. Specifically the [ConnectionManager](https://github.com/jpsim/CardsAgainst/blob/master/CardsAgainst/Controllers/ConnectionManager.swift) class.

## License

This project is under the MIT license.

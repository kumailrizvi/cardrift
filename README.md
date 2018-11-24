# Card Slider for Swift
interface with cards that users can swipe right or left

## Usage

This project isn't a framework, it's more so of a demonstration of how to approach this sort of user interface.
Card Slider basically uses a `UIPanGestureRecognizer` in conjunction with several `UIKit Dynamics` behaviors. Because of this, ideally you would want all the card logic code in a view controller class, so I opted not make an external class that uses delegation to talk to the view controller.

### `CardView.swift`
Most of the logic code is in the `ViewController` class, but each card is a subview of `CardView`. In the demo project, `ImageCard` is a subview of CardView and has its own custom subviews and layouts.
You can create your own subclass of `CardView` and modify the `cards` data structure in `ViewController` to swap in your own custom cards.
You can also modify the `CardOption` enum to show your own custom text on the cards for each of the 6 options (you may even add more, but that would require dealing with more emojis and laying them out properly.)

### `EmojiOptionsOverlay.swift`
This file has all the logic code associated with showing the 6 emojis on the sides when the user pans the card around, as well as the heart emoji on the top right.

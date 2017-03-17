# MVC

`Model` + (`View + Controller`)

in Apple design

# Code

* UI elements and its auto-layout mechanism are done via code-only through constraints (`NSLayoutConstraint(item:, attribute:, relatedBy:, toItem:, attribute:, multiplier:, constant:)`).
* Show UIView on screen via `PlaygroundPage.current.liveView = yourVC.view`
* You can also set up constraint via [Visual Format Language](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/VisualFormatLanguage.html) but just for personal taste, I found that using `NSLayoutConstraint(item:, attribute:, relatedBy:, toItem:, attribute:, multiplier:, constant:)` is more robust and offer complete functionality.
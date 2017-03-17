# VIPER

`Entity` + `Interactor` + `Presenter` + `View` + `Router`

# Code

* The most of distribution for responsibility but the most of high maintenance cost 
* `Model` now is `Entity` but with `Interactor` to act as its data provider
* `Presenter` hooks up with both `View` and `Interactor`.
   * `Presenter` hooks up with `Interactor` to get notified for its `Entity`'s states update
   * `Presenter` hooks up with `View` (owned by) to allow functionality for `View` to get its representable data to show
* `Router` is responsible for switching the screen (UIViewController)
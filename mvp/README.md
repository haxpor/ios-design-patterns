# MVP

`Model` + `UIViewController` + `Presenter`

or

`Model` + `Passive View` + `Presenter`

Usually regard 
* `UIViewController` -> `UIView`
* `Presenter`` -> `UIViewController` or simply Controller in general term

`Passive View` as compared to `UIViewController` in MVC in which the latter is more active in making activity compared to former which will be called by `Presenter` to update its state.

# Code

* `Model` structure is defined isolatedly in the same way as did in MVC
* There are 2 new protocols defined: one for `Passive View`, and another one for `Presenter`.
* `Passive View` protocol provides functionality (aim at `Presenter`) to update its state
* `Presenter` protocol provides functionality to initialize itself using both `Passive View` and model as parameters, and others to control or update its in-controlled `Passive View`
* The possible reason that `Presenter` needs to be embedded inside `Passive View` is because `Passive View` is actually `UIViewController` which normally is the default entry of to show on screen or operate in iOS sense. It's embedded there to allow code to make use of it.
* `Passive View` won't update its state by itself, but it provides how it is going to show UI element on screen. Instead it's up to `Presenter` to update the state. You can see in `GreetingViewController` class that it handles all UI layouting including constraints, and how to show on screen, but doesn't care about the states (values) of individual UI element which is `UILabel` in this case. 
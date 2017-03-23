# MVVM

`Model` + `View Model` + `View`

Usually regard 
* `View Model` -> the handler or controller of model
* `View` -> ``UIViewController`` or simply Controller in general term

# Code

* It's very similar to MVP but with binding setup in code. Like a supervisoning version of MVP.
* `View` has more activities to do compared to MVP. Instead of `View` to provide functionality for `View Model` to update its state. `View` will do by itself via binding which is setup in code.
* Binding can be regarded as reactive programming approach. Users can utilize reactive library out there i.e. [ReactiveCocoa](https://github.com/ReactiveCocoa/ReactiveCocoa), or [RxSwift](https://github.com/ReactiveX/RxSwift). Or just go via callback approach.
* `View Model` is added as part of `View` can be viewed for a reason as because `View Model` is supervisoning of `View`, but it's not so strong reason.
* Anyway from previous point, separating `View Model` and `View` from each other is to have better testability. `View Model` doesn't have to know about `View`. Thus now we have separated component which can be further tested separately.
   * I think MVP already done a great job at distribution, but MVVM does it better to remove completely a requirement for `View Model` to have a knowledge about its `View`.

# Dynamic Dispatch

Method Dispatch is the mechanism that helps to decide which operation should be executed, or more specifically, which method implementation should be used.

To start things off, Static Dispatch is supported by both value types and reference types.
However, Dynamic Dispatch is supported only by reference types(i.e. Class). The reason for this is that, for dynamism, or dynamic dispatch, in short, we need inheritance and our value types do not support inheritance.

checks at runtime.



# Static dispatch

At compile-time


# Examples

## Value Types
Since struct and enum are value types and does not support inheritance, the compiler puts it under Static dispatch as it is aware of the fact that it can never be subclassed.

```swift
struct Person {
    func isIrritating() -> Bool { } // Static
}
extension Person {
    func canBeEasilyPissedOff() -> Bool { } // Static
}
```

## Protocol

The key point to note here is that any method defined inside extension uses Static Dispatch

```swift
protocol Animal {
    func isCute() -> Bool { } // Table
}
extension Animal {
    func canGetAngry() -> Bool { } // Static
}
```
## Class

Normal method declarations follow the same principles as protocol
Whenever we expose a method to Objective-C runtime using @objc, the method uses Message Dispatch
However, if we mark a class as final, that class cannot be subclassed and thus its methods use Static Dispatch.

```swift
class Dog: Animal {
    func isCute() -> Bool { } // Table
    @objc dynamic func hoursSleep() -> Int { } // Message
}
extension Dog {
    func canBite() -> Bool { } // Static
    @objc func goWild() { } // Message
}
final class Employee {
    func canCode() -> Bool { } // Static 
}
```

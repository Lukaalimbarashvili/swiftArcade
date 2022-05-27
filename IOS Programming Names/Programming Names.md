1. Type Inference - Swift compiler can deduce type of variable. <br /> <br /> 
2. Ternary conditional operator - (`<CONDITION>`) ? `<TRUE VALUE>` : `<FALSE VALUE>` <br /> <br />
3. Countable closed range
``` swift
let closedRange = 0...5
```
4. Countable half-open range
``` swift
let halfOpenRange = 0..<5
```
5. Triangle numbers - 0, 1, 3, 6, 10, 15, 21 ...
```swift
let count = 10
var sum = 0
for i in 1...count {
    sum += i
    print(sum)
}
```
6. Overloading - In Swift, two or more functions may have the same name if they differ in parameters.

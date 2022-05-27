
To assign function to a variable in Swift, declare a variable that takes specific set/typeof parameters and return a specific type of value. Then we can assign a function that has same type of parameters and return value to this variable.
```swift
func add(a: Int, b: Int) -> Int {
    return a + b
}
//declare variable
var addFunction: (Int, Int) -> Int
//assign function to variable
addFunction = add
//call function using variable
let result = addFunction(5, 4)
print("Result is \(result)")
```

To pass function as parameter to another function in Swift, declare the parameter to receive a function with specific parameters and return type.

## Example
In the following program, we will define a calculate() function that can accept two numbers for parameters a and b, and accept a function for the parameter operation

```swift
func addition(a: Int, b: Int) -> Int {
    return a + b
}
 
func subtraction(a: Int, b: Int) -> Int {
    return a - b
}
 
func multiply(a: Int, b: Int) -> Int {
    return a * b
}
 
func division(a: Int, b: Int) -> Int {
    return a / b
}
 
func calculate(a: Int, b: Int, operation: (Int, Int) -> Int) {
    let result = operation(a, b)
    print(result)
}
 
calculate(a: 7, b: 2, operation: addition)
calculate(a: 7, b: 2, operation: subtraction)
calculate(a: 7, b: 2, operation: multiply)
calculate(a: 7, b: 2, operation: division)
```

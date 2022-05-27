## Assign Function to a Variable
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
print("Result is \(result)") // Result is 9
```

To pass function as parameter to another function in Swift, declare the parameter to receive a function with specific parameters and return type.

## Pass Function as Parameter
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
 
calculate(a: 7, b: 2, operation: addition) // 9
calculate(a: 7, b: 2, operation: subtraction) // 5
calculate(a: 7, b: 2, operation: multiply) // 14
calculate(a: 7, b: 2, operation: division) // 3
```

## Keyword: Overloading
In Swift, two or more functions may have the same name if they differ in parameters
```swift
// Function 1 to calculate sum
func printSum(value1: Int, value2: Int) {
}
  
// Function 2 to calculate sum
func printSum(value1: Int, value2: Int, value3: Int) {
}
```

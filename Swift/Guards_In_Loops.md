# Guards in loops

One thing to be wary of is how guards function in loops. When a guard clause evaluates to else in a loop, you need to transfer control with a “break” or “continue”. Saying it another way, in functions you would normally “return” from a guard, but in a loop you need to “break or continue” (note: you never “break” or “continue” from a function).

This example demonstrates this.
```swift
var array: [Int?] = [1,2,3,nil,4,5,]
    
for item in array {
    guard let item = item else {
        print(":)")
        break
    }
    print(item)
}
/// 1,2,3,:)
```
```swift
var array: [Int?] = [1,2,3,nil,4,5,]
    
for item in array {
    guard let item = item else {
        print(":)")
        continue
    }
    print(item)
}
///1,2,3,:),4,5,
```

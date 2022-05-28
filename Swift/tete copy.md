# Set

### Creating sets
You can declare a set explicitly by writing Set followed by the type inside angle brackets:
```swift
let setOne: Set<Int> = [1] Set literals
```

Sets don’t have their own literals. You use array literals to create a set with initial values. Consider this example:
```swift
let someArray = [1, 2, 3, 1]
```

This is an array. So how would you use array literals to create a set? Like this:
```swift
var explicitSet: Set<Int> = [1, 2, 3, 1]
```
You have to explicitly declare the variable as a Set. However, you can let the
compiler infer the element type like so:
```swift
var someSet = Set([1, 2, 3, 1])
```
To see the most important features of a set in action, let’s print the set you just
created:
```swift
print(someSet)
// > [2, 3, 1] but the order is not defined
```
First, you can see there’s no specific ordering. Second, although you created the set with two instances of the value 1, that value only appears once. Remember, a set’s values must be unique.

### Running time for set operations

The running time of all the operations is identical to those of dictionaries, and they also require the elements to be hashable.
* [Dictionaries running time](https://github.com/Lukaalimbarashvili/swiftArcade/blob/main/Swift/Dictionary.md)

# Dictionary

Simple Dictionary
```swift
var namesAndScores = ["Anna": 2, "Brian": 2, "Craig": 8, "Donna": 6]
print(namesAndScores)
// > ["Craig": 8, "Anna": 2, "Donna": 6, "Brian": 2]
```
Swift dictionaries have a type requirement for keys. Keys must be Hashable or you will get a compiler error

 If you’re using a dictionary that has values that are optional types, `<dictionary[key] = nil>` still removes the key completely.
 ```swift
 var dictWithNils: [String:Int?] =  [
    "one"  : 1,
    "two"  : 2,
    "none" : nil
]

dictWithNils["two"] = nil
dictWithNils["none"] = nil
let result = dictWithNils.count // 1
 ```
If you want keep the key and set the value to nil you must use the updateValue method.
```swift
var dictWithNils: [String:Int?] =  [
    "one"  : 1,
    "two"  : 2,
    "none" : nil
]

dictWithNils["none"] = nil
dictWithNils.updateValue(nil, forKey: "two")

let result = dictWithNils.count // 2
```
### Running time for dictionary operations

<b>Accessing elements:</b> Getting the value for a key is a constant time operation, or O(1).
Inserting elements: To insert an element, the dictionary needs to calculate the hash value of the key then store data based on that hash. These are all O(1) operations.
Deleting elements: Again, the dictionary needs to calculate the hash value to know exactly where to find the element, and then remove it. This is also an O(1) operation.
Searching for an element: As mentioned above, accessing an element has constant running time, so the complexity for searching is also O(1).
While all of these running times compare favorably to arrays, remember that you lose order information when using dictionaries.

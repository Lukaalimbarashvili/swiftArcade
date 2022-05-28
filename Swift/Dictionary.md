# Dictionary

Simple Dictionary
```swift
var namesAndScores = ["Anna": 2, "Brian": 2, "Craig": 8,
"Donna": 6]
print(namesAndScores)
// > ["Craig": 8, "Anna": 2, "Donna": 6, "Brian": 2]
```

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

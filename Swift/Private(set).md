# Private(set)

You can access variable to use but cant change it.


```swift
import Foundation

struct person {
    let id: UUID
    private(set) var name: String
    
    mutating func changeName() {
        self.name = "new Name" //ok
    }
}

var lukas = person(id: UUID(), name: "lukas")
lukas.name = "Lucas" //ko
lukas.name // ok
```


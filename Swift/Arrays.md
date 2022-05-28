# Array

Arrays are stored as a contiguous block in memory. That means if you have ten elements in an array, the ten values are all stored one next to the other. With that in mind, here’s the performance cost of various array operations:
## Accessing elements:
 The cost of fetching an element is cheap, meaning that it happens in a fixed or constant time. Sometimes this is written O(1). Since all the values are sequential, it’s easy to use random access and fetch a value at a particular index; all the compiler needs to know is where the array starts and what index you want to fetch.
## Inserting elements:
 The complexity of adding an element depends on the position in which you add the new element:
• If you add to the beginning of the array, Swift requires time proportional to the size of the array because it has to shift all of the elements over by one to make room. This is called linear time and sometimes written O(n).
• Likewise, if you add to the middle of the array, all values from that index on need to be shifted over. Doing so will require n/2 operations, therefore the running time is still linear with the size of the array or O(n).
• If you add to the end of the array using append and there’s room, it will take O(1). If there isn’t room, Swift will need to make space somewhere else and copy the entire array over before adding the new element, which will take O(n). The average case is O(1) though because arrays are not full most of the time.
## Deleting elements:
 Deleting an element leaves a gap where the removed element was. All elements in the array have to be sequential, so this gap needs to be closed by shifting elements forward.
The complexity is similar to inserting elements: If you’re removing an element from the end, it’s an O(1) operation. Otherwise, the complexity is O(n).
## Searching for an element:
 If the element you’re searching for is the first element in the array, then the search will end after a single operation. If the element doesn’t exist, you need to perform N operations until you realize that the element is not found. On average, searching for an element will take n/2 operations; therefore searching has a complexity of O(n).
As you learn about dictionaries and sets, you’ll see how their performance characteristics differ from arrays. That could give you a hint on which collection type to use for your particular case.

## Array performance: reserveCapacity()
*[Useful Link](https://www.hackingwithswift.com/articles/128/array-performance-append-vs-reservecapacity)

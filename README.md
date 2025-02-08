# Study material
https://www.hackingwithswift.com/100


## Days 1-12: Introduction to Swift
### Day 1,2 – variables, simple data types, and string interpolation
```
import UIKit

// Variable : String
//---------------------------------
print("1. Variable - string")
var str = "Hello, playground"
print(str)
str = "Goodbye"
print(str)
print("")

// Variable : Number
//---------------------------------
print("2. Variable - number")
var num = 8
print(num)

// format to be easily read
num = 8_000_000
print(num)
print("")

// Multi-line string
print("3. Variable - mutiple-line string")
var str2 = """
This goes over multiple
lines
"""
print(str2)
print("")


var str3 = """
This goes over multiple \
lines 
"""
print(str3)
print("")

// Dobule
print("4. Variable - double")
var pi = 3.14159
print(pi)
print("")

// Boolean
print("5. Variable - boolean")
var awesome = true
print(awesome)
print("")


// String interpolation
print("6. String interpolation")
var score = 85
var str5 = "Your score was \(score)"
var result = "Your test result are here \(str5)"
print(str5)
print(result)
print("")

// Constant
print("7. Constant")
let taylor = "swift"
print(taylor)
print("")

// Type annotation
let album: String = "Reputation"
let year: Int = 1989
let height: Double = 1.78
let taylorRocks: Bool = true
```

### Day 3 – Arrays, dictionaries, sets, and enums
```

import UIKit 

// Array
//-------------------------------
let Jan = "jan"
let Feb = "feb"
let Mar = "mar"
let Apr = "apr"
let beatles = [Jan, Feb, Mar, Apr]
print(beatles[0])

// Set
//  If you try to insert a duplicate item into a set, 
//  the duplicates get ignored. For example:
//-------------------------------
let colors = Set(["red", "green", "blue"])
let colors2 = Set(["red", "green", "blue", "red", "blue"])
print(colors)
print(colors2)

// Tuples
//-------------------------------
var name = (first: "Taylor", last: "Swift")
print(name.0)
print(name.first)

// Remember, you can change the values inside a tuple after you create it, but not the types of values. So,
// if you tried to change name to be (first: "Justin", age: 25) you would get an error.
name.0 = "Jonh"
print(name.0)

var fibonacci = (1, 1, 2, 3, 5, 8)

// Comparison
let address = (house: 555, street: "Taylor Swift Avenue", city: "Nashville")

let set = Set(["aardvark", "astronaut", "azalea"])

let pythons = ["Eric", "Graham", "John", "Michael", "Terry", "Terry"]

// Dictionary
//-------------------------------
let heights = [
    "Taylor Swift": 1.78,
    "Ed Sheeran": 1.73
]
print(heights["Taylor Swift"])


let favoriteIceCream = [
    "Paul": "Chocolate",
    "Sophie": "Vanilla"
]
print(favoriteIceCream["Paul"])
print(favoriteIceCream["Charlotte"])
print(favoriteIceCream["Charlotte", default: "Unknown"]
)

//  Creating empty collections
//-------------------------------
var teams = [String: String]()
teams["Paul"] = "Red"
print(teams["Paul"])

var results = [Int]()

var words = Set<String>()
var numbers = Set<Int>()

var scores = Dictionary<String, Int>()

var results_2 = Array<Int>()

// Enumerations
//-------------------------------
enum Result {
    case success
    case failure
}
let result4 = Result.failure

// Enum associated values
//-------------------------------
enum Activity {
    case bored
    case running(destination: String)
    case talking(topic: String)
    case singing(volume: Int)
}
let talking = Activity.talking(topic: "football")

// Enum raw values
//-------------------------------
enum Planet: Int {
    case mercury
    case venus
    case earth
    case mars
}

// Swift will automatically assign each of those a number starting from 0, and you can use that number to create an instance of the appropriate enum case.
let earth = Planet(rawValue: 2)

/*
enum Planet: Int {
    case mercury = 1
    case venus
    case earth
    case mars
}
 */
```



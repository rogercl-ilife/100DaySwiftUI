# Study material
https://www.hackingwithswift.com/100


## Days 1-12: Introduction to Swift
### Day 1 – variables, simple data types, and string interpolation
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

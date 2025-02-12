## Days 1-12: Introduction to SwiftUI
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

### Day 4 – Type annotations and checkpoint 2
```

let playerName: String = "Roy"
var luckyNumber: Int = 13
let pi: Double = 3.141
var isAuthenticated: Bool = true

var albums: [String] = ["Red", "Fearless"]
var user: [String: String] = ["id": "@twostraws"]
var books: Set<String> = Set(["The Bluest Eye", "Foundation", "Girl, Woman, Other"])

// empty array of strings
var teams: [String] = [String]()
var cities: [String] = []
var clues = [String]()

// enum
enum UIStyle {
    case light, dark, system
}

var style = UIStyle.light
style = .dark

let username: String
// lots of complex logic
username = "@twostraws"
// lots more complex logic
print(username)

// Arrays must always be specialized so they contain one specific type, and they have helpful functionality such as count, append(), and contains().

// Dictionary must be specialized to have one specific type for key and another for the value, and have similar functionality to arrays, such as contains() and count.

// Sets are really efficient at finding whether they contain a specific item.

// Enums let us create our own simple types in Swift so that we can specify a range of acceptable values such as a list of actions the user can perform, the types of files we are able to write, or the types of notification to send to the user.

// Practice
let albums_2 = ["Red", "Fearless","Red"]
print(albums_2.count)

let albums_3 = Set(albums_2)
print(albums_3.count)
```

### Day 5 – If, switch, and the ternary operator
```
let speed = 88
let percentage = 85
let age = 18

if speed >= 88 {
    print("a. Where we're going we don't need roads.")
}

if percentage < 85 {
    print("b. Sorry, you failed the test.")
}

if age >= 18 {
    print("c. You're eligible to vote")
}

// string comaprison
let ourName    = "Dave Lister"
let friendName = "Arnold Rimmer"

if ourName < friendName {
    print("1. It's \(ourName) vs \(friendName)")
}

if ourName > friendName {
    print("2. It's \(friendName) vs \(ourName)")
}

// Make an array of 3 numbers
var numbers = [1, 2, 3]

// Add a 4th
numbers.append(4)

// If we have over 3 items
if numbers.count > 3 {
    // Remove the oldest number
    numbers.remove(at: 0)
}

// Display the result
print(numbers)


// == & !=
let country = "Canada"

if country == "Australia" {
    print("G'day!")
}

let name = "Taylor Swift"

if name != "Anonymous" {
    print("Welcome, \(name)")
}


// Create the username variable
var username = "taylorswift13"

// == empty
if username == "" {
    // Make it equal to "Anonymous"
    username = "Anonymous"
}
print("Welcome, \(username)!")

// .count
if username.count == 0 {
    username = "Anonymous"
}


// .isEmpty
if username.isEmpty == true {
    username = "Anonymous"
}

// multiple condition
let a = false
let b = true

if a {
    print("Code to run if a is true")
} else if b {
    print("Code to run if a is false but b is true")
} else {
    print("Code to run if both a and b are false")
}

let temp = 25
if temp > 20 && temp < 30 {
    print("It's a nice day.")
}

let userAge = 14
let hasParentalConsent = true

if userAge >= 18 || hasParentalConsent == true {
    print("You can buy the game")
}

if userAge >= 18 || hasParentalConsent {
    print("You can buy the game")
}

enum TransportOption {
    case airplane, helicopter, bicycle, car, scooter
}

let transport = TransportOption.airplane

if transport == .airplane || transport == .helicopter {
    print("Let's fly!")
} else if transport == .bicycle {
    print("I hope there's a bike path…")
} else if transport == .car {
    print("Time to get stuck in traffic.")
} else {
    print("I'm going to hire a scooter now!")
}

// invalid comparison
/*
var actualWage: Int = 22_000
var medianWage: Double = 22_000
if actualWage >= medianWage {
    print("Success")
}
*/

enum Weather {
    case sun, rain, wind, snow, unknown
}

let forecast = Weather.sun

if forecast == .sun {
    print("It should be a nice day.")
} else if forecast == .rain {
    print("Pack an umbrella.")
} else if forecast == .wind {
    print("Wear something warm")
} else if forecast == .rain {
    print("School is cancelled.")
} else {
    print("Our forecast generator is broken!")
}

switch forecast {
case .sun:
    print("It should be a nice day.")
case .rain:
    print("Pack an umbrella.")
case .wind:
    print("Wear something warm")
case .snow:
    print("School is cancelled.")
case .unknown:
    print("Our forecast generator is broken!")
}

let place = "Metropolis"

switch place {
case "Gotham":
    print("You're Batman!")
case "Mega-City One":
    print("You're Judge Dredd!")
case "Wakanda":
    print("You're Black Panther!")
default:
    print("Who are you?")
}

var day = 5
print("My true love gave to me…")

switch day {
case 5:
    print("5 golden rings")
case 4:
    print("4 calling birds")
case 3:
    print("3 French hens")
case 2:
    print("2 turtle doves")
default:
    print("A partridge in a pear tree")
}

print("")



// fallthrough usage 
day = 4
switch day {
case 5:
    print("5 golden rings")
    fallthrough
case 4:
    print("4 calling birds")
    fallthrough
case 3:
    print("3 French hens")
    fallthrough
case 2:
    print("2 turtle doves")
    fallthrough
default:
    print("A partridge in a pear tree")
}


let age2 = 18
let canVote = age2 >= 18 ? "Yes" : "No"
print("\(canVote)")

let hour = 23
print(hour < 12 ? "It's before noon" : "It's after noon")

let names = ["Jayne", "Kaylee", "Mal"]   
let crewCount = names.isEmpty ? "No one" : "\(names.count) people"
print(crewCount)

enum Theme {
    case light, dark
}

let theme = Theme.dark

let background = theme == .dark ? "black" : "white"
print(background)

var averagePages: Double = 10.0
print(averagePages == 10 ? "Success" : "Failure")
```

### Day 6 – Loops, summary, and checkpoint 3
```
//================================== 
// Loop
//================================== 
let platforms = ["iOS", "macOS", "tvOS", "watchOS"]

for os in platforms {
    print("Swift works great on \(os).")
}

for i in 1...12 {
    print("5 x \(i) is \(5 * i)")
}

for i in 1...12 {
    print("The \(i) times table:")

    for j in 1...12 {
        print("  \(j) x \(i) is \(j * i)")
    }

    print()
}

for i in 1...5 {
    print("Counting from 1 through 5: \(i)")
}

print()

for i in 1..<5 {
    print("Counting 1 up to 5: \(i)")
}

var lyric = "Haters gonna"

for _ in 1...5 {
    lyric += " hate"
}

print(lyric)

var names = ["John", "Sophie", "Lottie"]
for name in names {
    print("Hello, \(name)!")
}

//================================== 
// While
//================================== 
var countdown = 10

while countdown > 0 {
    print("\(countdown)…")
    countdown -= 1
}

print("Blast off!")

let id = Int.random(in: 1...1000)
let amount = Double.random(in: 0...1)

// create an integer to store our roll
var roll = 0

// carry on looping until we reach 20
while roll != 20 {
    // roll a new dice and print what it was
    roll = Int.random(in: 1...20)
    print("I rolled a \(roll)")
}

// if we're here it means the loop ended – we got a 20!    
print("Critical hit!")

var number: Int = 10
while number > 0 {
    number -= 2
    if number.isMultiple(of: 2) {
        print("\(number) is an even number.")
    }
}

//================================== 
// break and continue
//================================== 
let filenames = ["me.jpg", "work.txt", "sophie.jpg", "logo.psd"]

for filename in filenames {
    if filename.hasSuffix(".jpg") == false {
        continue
    }

    print("Found picture: \(filename)")
}

let number1 = 4
let number2 = 14
var multiples = [Int]()

for i in 1...100_000 {
    if i.isMultiple(of: number1) && i.isMultiple(of: number2) {
        multiples.append(i)

        if multiples.count == 10 {
            break
        }
    }
}

print(multiples)

//================================== 
// Checkpoiunts
//================================== 
for i in 1...100 {
    if i.isMultiple(of:3) && i.isMultiple(of:5) {
        print("FizzBuzz")
    } else if i.isMultiple(of:3) {
        print("Fizz")
    } else if i.isMultiple(of:5) {
        print("Buzz")
    } else {
        print("\(i)")
    }
}
```

### Day 7 – Functions, parameters, and return values

```
import Foundation

// function 1
//=======================================================
showWelcome()

func showWelcome() {
    print("Welcome to my app!")
    print("By default This prints out a conversion")
    print("chart from centimeters to inches, but you")
    print("can also set a custom range if you want.")
}


// function 2
//=======================================================
printTimesTables(number: 5)


func printTimesTables(number: Int) {
    for i in 1...12 {
        print("\(i) x \(number) is \(i * number)")
    }
}


// function 3
//=======================================================
printTimesTables_2(number: 5, end: 20)

func printTimesTables_2(number: Int, end: Int) {
    for i in 1...end {
        print("\(i) x \(number) is \(i * number)")
    }
}

// function 4
//=======================================================
func square(numbers: [Int]) {
    for number in numbers {
        let squared = number * number
        print("\(number) squared is \(squared).")
    }
}
square(numbers: [2, 3, 4])

// function 5
//=======================================================
func rollDice() -> Int {
    return Int.random(in: 1...6)
}

let result = rollDice()
print(result)

// function 6
//=======================================================
func areLettersIdentical(string1: String, string2: String) -> Bool {
    let first = string1.sorted()
    let second = string2.sorted()
    return first == second
}

let re = areLettersIdentical(string1: "abc", string2: "bac")
print(re)

/* Both of following codes are good.
 
func areLettersIdentical(string1: String, string2: String) -> Bool {
    return string1.sorted() == string2.sorted()
}
 
func areLettersIdentical(string1: String, string2: String) -> Bool {
     string1.sorted() == string2.sorted()
 }
*/

// only one line inside func, it is fine without return
func rollDice_2() -> Int {
    Int.random(in: 1...6)
}

let re_2 = rollDice_2()
print(re_2)

func pythagoras(a: Double, b: Double) -> Double {
    sqrt(a * a + b * b)
}
```

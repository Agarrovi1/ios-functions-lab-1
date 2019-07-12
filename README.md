# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {

}

func totalCostAfterAddingTaxes() -> Int {
let totalCost = itemCost + (itemCost * nyTax)
return Int(totalCost)
}

totalCostAfterAddingTaxes()
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

## Question 2

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}


func whatWeatherIsLikeToday (temp: Int) -> String {
if todaysTemperature <= 40 {
return "It's cold out."
} else if todaysTemperature >= 85 {
return"It's really warm."
} else {
return "Weather is moderate."
}
}

whatWeatherIsLikeToday(temp: todaysTemperature)
```


## Question 3

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

```swift
func min2 (a: Int, b: Int) -> Int {
if a > b {
return b
} else {
return a
}
}

min2(a:1, b:2)
```


## Question 4

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

```swift
func lastDigit (_ number: Int) -> Int? {
let numString = String(number)
var last: String?

for a in numString {
last = "\(a)"
}
if let unwrappedNum = last {
if let intVersion = Int(unwrappedNum) {
return intVersion
} else {
return nil
}
} else {
return nil
}
}

lastDigit(12345)
```
## Question 5

Write a function that takes in any two positive integers and return the sum.

```swift
func theSum (x: Int, y: Int) -> Int {
return (x + y)
}

theSum(x: 4, y: 9)
```


## Question 6

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |
```swift
func letterGrade (numberGrade x: Int) -> String {
if x == 100 {
return "A+"
} else if x >= 90 && x <= 99 {
return "A"
} else if x >= 80 && x <= 89 {
return "B"
} else if x >= 70 && x <= 79 {
return "C"
} else if x >= 65 && x <= 69 {
return "D"
} else if x < 65 {
return "F"
} else {
return "not valid grade"
}
}
```

## Question 7

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)

```swift
func calculating (x: Int, y: Int, operation: Character) -> Int? {
let sum = x + y
let product = x * y
let difference = x - y
let quotient = x / y

if operation == "+" {
return sum
} else if operation == "-" {
return difference
} else if operation == "*" {
return product
} else if operation == "/" {
if y != 0 {
return quotient
} else {
return nil
}
} else {
return nil
}
}

calculating(x: 9, y: 3, operation: "/")
```


## Question 8

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

func totalWithTip (costOfMeal: Int, tip: Double) -> Double {
let costAsDouble = Double(costOfMeal)
let total = costAsDouble + (costAsDouble * tip)
return total
}

totalWithTip(costOfMeal: mealCost, tip: tipPercentage)

let finalCost = totalWithTip(costOfMeal: 45, tip: 0.15)
```

Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

//Write your code below

func totalWithTipAndTax(costOfMeal: Int, tip: Double, tax: Double) -> Double {
let costAsDouble = Double(costOfMeal)
let total = costAsDouble + (costAsDouble * tip) + (costAsDouble * tax)
return total
}

let myFinalCostWithTipAndTax =  totalWithTipAndTax(costOfMeal: mealCost, tip: tipPercentage, tax: taxPercentage)
```


## Question 9

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`

```swift
func repeatPrint(message: Character, count: Int) -> String {
var totalString = ""
for _ in 1...count {
totalString += "\(message)"
}
return totalString
}

repeatPrint(message: "+", count: 10)
```


## Question 10

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

```swift
func first (n: Int) -> [Int] {
var array: [Int] = []
for a in 1...n {
array.append(a)
}
return array
}

first(n: 3)
```


## Question 11

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)

```swift
func fizzCountBuzz(x: Int) {
for a in 1...x {
if a % 3 == 0 && a % 5 == 0 {
print("FizzBuzz")
} else if a % 3 == 0 {
print("Fizz")
} else if a % 5 == 0 {
print("Buzz")
} else {
print(a)
}
}
}

fizzCountBuzz(x: 15)
```


## Question 12

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

```swift
func reverse(numbers: [Int]) -> [Int] {
var reverseArray: [Int] = []
for a in numbers.indices {
let b = numbers.count - 1
reverseArray.append(numbers[b-a])
}
return reverseArray
}

reverse(numbers: [1,2,3])
```
## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.

```swift
func mostFrequentlyRepeatingNum(arrayOfInt: [Int]) -> Int {
let SetOfInt = Set(arrayOfInt)
var frequentNum = 0
var prevCount = 0
for a in SetOfInt {
var count = 0
for b in arrayOfInt {
if a == b {
count += 1
}
}
if count > prevCount {
prevCount = count
frequentNum = a
}
}
return frequentNum
}

mostFrequentlyRepeatingNum(arrayOfInt: [1,1,1,34,25,66,25,34,24,34,34,65])
```

## Question 14

Write a function that sums all the even indices of an array of Ints.

```swift
func sumOfEvenNums(arrayOfInts: [Int]) -> Int {
var sum = Int()
for a in arrayOfInts where a % 2 == 0 {
sum += a
}
return sum
}

sumOfEvenNums(arrayOfInts: [1,2,3,4,5,6,7,8])
```


## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`

```swift
func flipsADictionary(dictionary: [Int:String]) -> [String:Int] {
var newDictionary: [String:Int] = [:]
for (a, b) in dictionary {
newDictionary[b] = a
}
return newDictionary
}

flipsADictionary(dictionary: [1: "hi", 5: "bye"])
```

## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

```swift
func secondHighestScore(scoresDict: [String:Int]) -> String {
var arrayOfScores: [Int] = []
for a in scoresDict.values {
arrayOfScores.append(a)
}
var answer = ""


for (a, b) in scoresDict where arrayOfScores.count != 1 {
let secondIndex = arrayOfScores.count - 2
let second = arrayOfScores.sorted()[secondIndex]
if b == second {
answer = a
}
}
return answer
}
secondHighestScore(scoresDict: ["Person 1": 83, "Person 2": 74, "Person 3": 82])
```

## Question 17

Write a function that determines if a value is inside of array.

```swift
func doesTheArrayContainThisValue(value: Int, array: [Int]) -> Bool {
let trueOrFalse = array.contains(value)
return trueOrFalse
}
```

## Question 18

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

```swift
func trueIfEvenFalseIfOdd(num: Int) -> Bool {
if num % 2 == 0 {
return true
} else {
return false
}
}

let dieRoll = Int(arc4random_uniform(6) + 1)
trueIfEvenFalseIfOdd(num: dieRoll)
```

## Question 19

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

```swift
func largestNumInArray(x: [Int]) -> Int {
let lastIndex = x.count - 1
let largestNum = x.sorted()[lastIndex]
return largestNum
}
```

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

```swift
func statingLargestNumInArray(y: [Int]) -> String {
let largestNum = largestNumInArray(x: y)
return "The largest number in this array is \(largestNum)"
}
```

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.

```swift
func statingLargestNumIsEvenOrOdd(z: [Int]) -> String {
let largestNum = largestNumInArray(x: z)
let evenOrOdd = trueIfEvenFalseIfOdd(num: largestNum)
if evenOrOdd == true {
return "The largest number in my array is even"
} else {
return "The largest number in my array is odd"
}
}

largestNumInArray(x: myArray)
statingLargestNumInArray(y: myArray)
statingLargestNumIsEvenOrOdd(z: myArray)
```

## Question 20

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`


## Question 21

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"

func numberOfSpecificCharacterInString(c: Character, s:String) -> Int {
var count = Int()
for a in s {
if a == c {
count += 1
}
}
return count
}

numberOfSpecificCharacterInString(c: targetCharacter, s: testString)
```

Sample output: `3`


## Question 22

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]

func howManyCharactersInAStringAllTogether(characters: [Character], s: String) -> Int {
var count = Int()
for a in characters {
for b in s {
if a == b {
count += 1
}
}
}
return count
}

howManyCharactersInAStringAllTogether(characters: targetCharacters, s: inputString)
```

Output: `13`


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.

```swift
func uniqueIntInAnArray(array: [Int]) -> Int {
var arrayInFunc: [Int] = []
let setOfArray = Set(array)
for a in setOfArray {
var count = 0
for b in array {
if a == b {
count += 1
}
}
if count == 1 {
arrayInFunc.append(a)
}
}
return arrayInFunc.count
}

uniqueIntInAnArray(array: inputArray2)
```

## Question 24

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

```swift
func convertingBinary(binaryArray: [Int]) -> Int {
var reverseBinaryString = ""
var decimalValue = 0
for a in binaryArray {
reverseBinaryString = "\(a)" + reverseBinaryString
}
for (index, a) in reverseBinaryString.enumerated() where a == "1" {
var powerOfTwo = 1

if index == 0{
decimalValue += 1
continue
}
guard index >= 1 else {
continue
}

for _ in 1...index {
powerOfTwo *= 2
}
decimalValue += powerOfTwo
}
return decimalValue
}

convertingBinary(binaryArray: binaryArray)
```

## Question 25

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`

```swift
func timeDifference(firstHour: Int, firstMinute: Int, secondHour: Int, secondMinute: Int) -> Int {
var differenceOfHoursInMin = (secondHour - firstHour) * 60
let differenceOfMinutes = secondMinute - firstMinute
if firstHour > secondHour {
differenceOfHoursInMin *= -1
}
let totalDiff = differenceOfHoursInMin + differenceOfMinutes
return totalDiff
}

timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)
```


## Question 26

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

```swift
func filterOdd(arr: [Int]) -> [Int] {
let setArr = Set(arr)
var oddNum: [Int] = []

for a in arr {
if a % 2 != 0 {
oddNum.append(a)
}
}

let setOdd = Set(oddNum)
let evenSet = setArr.subtracting(setOdd)
return Array(evenSet)
}

filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])
```


## Question 27

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`

```swift
func doubleIt(arr: [Int]) -> [Int] {
var doubledArr: [Int] = []
for a in arr {
doubledArr.append((a * 2))
}
return doubledArr
}

doubleIt(arr: [1, 2, 3, 4])
```


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`

```swift
func multiplyIt(arr: [Int], n: Int) -> [Int] {
var multipliedArr: [Int] = []
for a in arr {
multipliedArr.append((a * n))
}
return multipliedArr
}

multiplyIt(arr: [1, 2, 3, 4], n: 4)
```


## Question 28

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`

```swift
func unwrap(arr: [Int?]) -> [Int] {
var unwrappedArr: [Int] = []
for a in arr {
if let bind = a {
unwrappedArr.append(bind)
}
}
return unwrappedArr
}

unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])
```

## Question 29

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`

```swift
func countBools(arr: [Bool]) -> [Bool:Int] {
var trueCount = 0
var falseCount = 0
var DictOfTAndF: [Bool:Int] = [:]
for a in arr {
if a == true {
trueCount += 1
} else {
falseCount += 1
}
}
DictOfTAndF[true] = trueCount
DictOfTAndF[false] = falseCount
return DictOfTAndF
}

countBools(arr: [true, true, false, true, false, true])
```


## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`

```swift
func countCharacters(str: String) -> [Character:Int] {
var charaCount: [Character:Int] = [:]
for a in str {
var count = 0
for b in str {
if a == b {
count += 1
}
}
charaCount[a] = count
}
return charaCount
}

countCharacters(str: "Hello, World!")
```

## Question 31

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`

```swift
func dictToTuples(dict: [Int:String]) -> [(Int, String)] {
var answerArray: [(Int,String)] = []
for (a, b) in dict {
let id = a
let name = b
let tuple = (id, name)
answerArray.append(tuple)
}
return answerArray
}

dictToTuples(dict: baseballTeamsById)
```

## Question 32

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)

```swift
func checkPalindrome(s: String) -> Bool {
var reverseS = ""
for a in s {
reverseS = "\(a)" + reverseS
}
if reverseS == s {
return true
} else {
return false
}
}

checkPalindrome(s: "abba")
```

## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)

```swift
func checkPangram(str: String) -> Bool {
let alphabet = "abcdefghijklmnopqrstuvwxyz"
var alphabetArray = String()

for a in alphabet {
alphabetArray.append(a)
}

let alphaSet = Set(alphabetArray)

var sentenceSet: Set<Character> = []

for a in str {
if a != " " {
sentenceSet.insert(a)
}
}

if alphaSet.isSubset(of: sentenceSet) {
return true
} else {
return false
}
}

checkPangram(str: "The quick brown fox jumps over the lazy dog")
```

## Question 34

Write your own `min()` and `max()` functions for an Array of Ints

```swift
let sample = [1,2,53,77,94,35,24,1,9]
func min(array: [Int]) -> Int {
let fromHighToLow = array.sorted()
return fromHighToLow[0]
}

func max(array: [Int]) -> Int {
let fromHighToLow = array.sorted()
return fromHighToLow[array.count-1]
}

min(array: sample)
max(array: sample)
```

## Question 35

Given two arrays of Ints, write a function that tells you all the values they have in common.

```swift
let sample = [1,2,53,77,94,35,24,1,9]
let sample2 = [1,34,52,53,33,22,1,8,2]
func whatTheyHaveInCommon(arrOne: [Int], arrTwo: [Int]) -> Set<Int> {
let aOne = Set(arrOne)
let aTwo = Set(arrTwo)
return aOne.intersection(aTwo)
}

whatTheyHaveInCommon(arrOne: sample, arrTwo: sample2)
```

## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.

```swift
func mostFrequentInArrays(arrayOfArrays: [[Int]]) -> [Int] {
var answerArr: [Int] = []
var highestCount = 0
for a in arrayOfArrays {
var count = 0
for b in arrayOfArrays {
if a == b {
count += 1
}
}
if count > highestCount {
answerArr = a
highestCount = count
}
}
return answerArr
}

let sample3 = [[1,2,3],[1,4,5],[1,4,5]]
mostFrequentInArrays(arrayOfArrays: sample3)
```

## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`

```swift
func rotateLetterByOne(str: String) -> String {
let alphabet = "abcdefghijklmnopqrstuvwxyz"
let oneLetterOver = "bcdefghijklmnopqrstuvwxyza"

var decoder: [Character:Character] = [:]
var decoderForUpperCase: [Character:Character] = [:]

var answerStr = ""

let uppercase = alphabet.uppercased()
let uppercaseOneOver = oneLetterOver.uppercased()

for (indexOuter, a) in alphabet.enumerated() {
for (indexInner, b) in oneLetterOver.enumerated() {
if indexOuter == indexInner {
decoder[a] = b
}
}
}

for (indexOuter, a) in uppercase.enumerated() {
for (indexInner, b) in uppercaseOneOver.enumerated() {
if indexOuter == indexInner {
decoderForUpperCase[a] = b
}
}
}

for a in str {
if alphabet.contains(a) {
if let letter = decoder[a] {
answerStr = answerStr + "\(letter)"
}
} else if uppercase.contains(a) {
if let letterUpper = decoderForUpperCase[a] {
answerStr = answerStr + "\(letterUpper)"
}
} else {
answerStr = answerStr + "\(a)"
}
}
return answerStr
}

rotateLetterByOne(str: "This is a test string. Anything can be written in here (even Zebras and zebras).")
```

# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)
```swift
var numberRange = 1...10
var numbersIWantInAString = ""

for i in numberRange  {
numbersIWantInAString.append(String(i))

if i != 10 {
numbersIWantInAString.append(", ")
}
}

print(numbersIWantInAString)

```

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.
```swift
var numberRange = 5...51
var numbersIWantInAString = ""

for i in numberRange  {

if i % 2 == 0 {
numbersIWantInAString.append(String(i))
numbersIWantInAString.append(" ")
}
}

print(numbersIWantInAString)

```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

```swift
var numberRange = 1...60
var numbersIWantInAString = ""

for i in numberRange  {

if i % 10 == 4 {
numbersIWantInAString.append(String(i))
numbersIWantInAString.append(" ")
}
}

print(numbersIWantInAString)

```

***
## Question 4

Print each character in the string `"Hello world!"`

```swift
Print each character in the string `"Hello world!"`
var stringToIterate = "Hello world!"

for character in stringToIterate {
print(character)
}
```

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`


```swift
let myStringSeven = "Hello world!"
let specialCharacter: Character = "!"

for char in myStringSeven {
if char != specialCharacter {
print(char)
}
}
```

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

```swift
let testString = "hello"

switch testString.count % 2  {
case 0 :
for letter in testString {
print(letter, terminator: "")
}
default :
for index in 0...testString.count - 1 {
if index % 2 != 0 {
let currentIndex = testString.index(testString.startIndex, offsetBy: index)
print(testString[currentIndex], terminator : " ")
}
}
}

```

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

```swift

let characterToString: Character = "a"
print(String(characterToString))
```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

```swift
1.
let eAcute = "un caf\u{E9}"
let combinedEAcuteQuestion = "voulez vous un caf\u{65}\u{301}?"
print(eAcuteQuestion)
print(combinedEAcuteQuestion)
print(eAcuteQuestion == combinedEAcuteQuestion)

let acute = "\u{61}\u{301}"
```
***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

```swift

let unicodeHello = "\u{48}\u{45}\u{4C}\u{4C}\u{4F}\u{20}"
let unicodeWorld = "\u{57}\u{4F}\u{52}\u{4C}\u{44}\u{21}"

print(unicodeHello + unicodeWorld)

```


***
## Question 10

**Using only Unicode**, print out your name.
```swift
let myFirstName = "\u{41}\u{6C}\u{79}\u{73}\u{6F}\u{6E}"
print(myFirstName)
```
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.
```swift
let unicodeHola = "\u{48}\u{4F}\u{4C}\u{41}\u{20}"
let unicodeMundo = "\u{4D}\u{55}\u{4E}\u{44}\u{4F}\u{21}"

print(unicodeHola + unicodeMundo)
```
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -



let horizontalLines = String(repeating: "- ", count: 11)
let flowerUnicodeAndVerticalLines = String(repeating: "| \u{2698} ", count: 5)

print(dashForBoxes)
for _ in 0...7 {
print("\(flowerUnicodeAndVerticalLines)|")
}
print(dashForBoxes)
```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
//var aString = "Replace the letter e with \*"


var aString = "Replace the letter e with *"
var letterE:Character = "e"
var replacedString = ""

for char in aString {
if char == letterE {
replacedString.append("*")
} else {
replacedString.append(char)
}
}
print(replacedString)
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift

var aString = "this string has 29 characters"
var reverse = ""

var aString = "this string has 29 characters"
var reverse = ""

for char in aString.reversed() {
reverse.append(char)
}
print(reverse)


```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift


let aString = "anutforajaroftuna"
let isPalindrome = String(aString.reversed())

if aString == isPalindrome {
print("true")
} else {
print("false")
}

```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift

var problem = "split this string into words and print them on separate lines"
var newString = problem.components(separatedBy: " ")

for element in newString {
print(element)
}


```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***

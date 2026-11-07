# Tool Learning Log

## Tool: Swift (Xcode)

## Project: Personalized Music App (iOS)

---

### 10/22/26 - Intro to Swift Playground:
* Well, things have become pretty interesting. Since I'm using Swift for a tool, I had to temporarily leave my Chromebook because Swift prioritizes.. Well, the MacBook. Since I'm also learning a new software (and an IDE thanks to XCode), I decided to try and understand how I could use Swift by doing some of the tutorials on Swift Playground! I specifically started with the Basics (Learn to Code 1) to see if there's any clear differences between the way you write code in Swift and how you write code in both JavaScript and simple Java. What I've noticed already is the fact that in Swift, all actions (so far), require parentheses '()'. Potentially this could be because all of the given commands have their own more built in functions that I don't know about yet? Whatever the case with both Java and JavaScript, you typically need a semi-colon (;) to run code (I.e., `Document.write(" ");` and `System.out.println("")`) and even with JavaScript's optional usage of a semi-colon, it's mandatory in Swift to use parentheses. Additionally Swift uses functions, just like JavaScript. However, they title functions as `func` instead of `function`, and maybe this is because of the Playground itself, but I do wonder if this'll occur once again when I pivot towards XCode? I'm not particularly sure, but either way I am quite curious what I'll see in the future. Maybe I can see it's rendition of Loops and Conditionals? I'll just need to wait and see really. For the next time I touch this website, I'll be attempting to not only complete the first tutorial, but I'll also attempt to look through some Youtube Videos to code something small using XCode! Firstly however, I do need to find a way to connect XCode to the IDE... That I'll ask Mr. Mueller about. 

![alt text](image.png)

### 11/04/26:
* I'm still in the process of figuring out how I can connect Swift and my Github account. It's been a bit of a hastle for me to try with XCode, so I've just been focusing on Swift Playground again. From what I've been learning, the loops with Swift are probably the first unique aspect of Swift in comparison to Java and Javascript. Both programs do use while loops (`while (x > 5){}`) and for loops (`for (int i = 0; i < 10; i++){}`), however Swift's loops are a bit different. For for loops, instead of writing 3 different segments, they only need 1 and look like this: `for i in 1 ... 3 {}`. `i` in this context is the variable and 3 can be substituted for anything, but here's an example of it in action for one of the playground challenges. 

```swift
func gemTest(){
    if isOnGem{
        collectGem()
    } else {
        moveForward()
    }
} 

for i in 1 ... 4 {
    for i in 1 ... 4 {
        gemTest()
    }
    turnLeft()
}

```

For the challenge, I had to complete a condition by collecting gems that were in a box like shape. The loop is iterating another loop that's making a function run 4 times per cycle. For the while loops, there's actually 2 versions of them. The first one is the typical while loop we see in Java and Javascript, but the second one is something I haven't exactly seen yet: It's `repeat-while`, and it looks like this: `repeat {} while (insert conditon)`. The difference between the traditional while loop and this loop is the fact that no matter what, the `repeat-while` loop will run at least once before establishing it's condition and running based on that. For example, there's this from the official [Swift reference page](https://docs.swift.org/latest/documentation/the-swift-programming-language/aboutswift), and going to the page called 'Control Flow', you'd see this sample for `repeat-while`: 

```swift
repeat {
    // move up or down for a snake or ladder
    square += board[square]
    // roll the dice
    diceRoll += 1
    if diceRoll == 7 { diceRoll = 1 }
    // move by the rolled amount
    square += diceRoll
} while square < finalSquare
print("Game over!")
```

This piece is connected to another code sample, but I wanted to focus on this specifically for just a moment. This whole piece is for a snakes and ladders coded game, and this `repeat-while` loop is running as long as someone doesn't reach the final square. I do wonder what some of this code means (such as the curly brackets encasing `diceRoll` as seen in the conditional), but speaking of conditionals.. The basics of it is basically identical to Java and JavaScript! That's merciful thankfully, but looking back at the same reference page, I did see something called `switch`, and I do remember tackling that for Java over the Summer! Looking back at my notes on switch, they seem really similar to one another. For each different option on switch, it's labeled as `case:` and similarly to how conditionals run, if the case aligns with the original value, that `case:` will exclusively run. For example, this is what the reference sheet provides for `switch`: 

```swift
    let anotherCharacter: Character = "a"
    let message = switch anotherCharacter {
    case "a":
        "The first letter of the Latin alphabet"
    case "z":
        "The last letter of the Latin alphabet"
    default:
        "Some other character"
    }
print(message)
// Prints "The first letter of the Latin alphabet".
```

This is definitely a lot easier for me to understand now that I've connected it back to Java, but in this case, the value of `anotherCharacter` is being checked by the different cases, and since its value is 'a', the code prints out "The first letter of the Latin alphabet". This is honestly pretty interesting to me, and I hope the Playground does cover this section! I doubt it however, because I never saw `repeat-while` or `while` get covered as I was completing the loops section of the code. Maybe they're saving it for the 2nd learning section? Either way, I plan to create my own reference sheet in the coming weeks so this becomes easier for me to digest. Still deciding if I'll write in a notebook or on Google Docs though. 
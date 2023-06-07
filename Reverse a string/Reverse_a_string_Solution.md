```Swift
import Swift

func reverseString(_ Word:String) -> String {
    var reverse = ""
    let word = Array(Word)
    let i = Word.count
    for x in 1...i {
        reverse = reverse + String(word[i - x])
    }
    //return reverse.capitalized //the solution for the extra challenge.
    return reverse
}

print(reverseString("Omar"))

```
**Output**
```
ramO

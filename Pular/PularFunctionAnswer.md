
```Swift
import Swift

func Plural(Word:String) -> Bool {
    
    switch Word{
    case "children": return true
    case "women": return true
    default:
        let word = Array(Word)
        let char = word[word.count - 1]
        if char == "s" {
            return true
        }else{
            return false
        }
    }
}


let word = "women"
let answer = Plural(Word: word)
```

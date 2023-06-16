## Solution

```Swift
func palindromeWord(of Word:String) -> Bool {
    let word = Word.lowercased()
    let wordtoArray = Array(word)
    var wordcount = wordtoArray.count - 1
    var x = 0

    if wordtoArray.count%2 == 0 {
        for _ in 0...(wordtoArray.count/2) {
            if wordtoArray[wordcount] == wordtoArray[x] {
                wordcount -= 1
                x += 1
            }else{
                return false
            }
        }
        return true
    }else{
        while x != wordcount {
            if wordtoArray[wordcount] == wordtoArray[x]{
                wordcount -= 1
                x += 1
            }else{
                return false
            }
        }
        return true
    }
}

let test = "Mom"
print(palindromeWord(of: test))
//true
```

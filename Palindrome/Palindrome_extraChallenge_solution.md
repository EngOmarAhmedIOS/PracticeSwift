## Extra Challenge Solution 
```Swift
func removeSpacing(from Word:String) -> [Character] {
    let word = Word.lowercased()
    var wordArray = Array(word)
    var result = [Character]()
    
    for index in 0...wordArray.count-1 {
        if wordArray[index] != " "{
            result.append(wordArray[index])
        }
    }
    return result
}

func palindromeSentance(of sentance:String) -> Bool {
    let sentancetoArray = removeSpacing(from: sentance)
    var sentanceCount = sentancetoArray.count - 1
    var x = 0

    if sentancetoArray.count%2 == 0 {
        for _ in 0...(sentancetoArray.count/2) {
            if sentancetoArray[sentanceCount] == sentancetoArray[x] {
                sentanceCount -= 1
                x += 1
            }else{
                return false
            }
        }
        return true
    }else{
        while x != sentanceCount {
            if sentancetoArray[sentanceCount] == sentancetoArray[x]{
                sentanceCount -= 1
                x += 1
            }else{
                return false
            }
        }
        return true
    }
}

let test = "Taco Cat"
print(palindromeSentance(of: test))
//true
```

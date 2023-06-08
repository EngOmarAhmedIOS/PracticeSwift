The solution of the problem without the extra challenge:

```Swift
func isogram(_ Word:String) -> Bool {
    let word = Array(Word)
    for index1 in 1...word.count-1{
        for index2 in 1...word.count-1{
            if ((word[index1] == word[index2]) && (index1 != index2)){
                return true
            }
        }
    }
    return false
}

print(isogram("tomorrow"))
//true
```
The solution with the extra challenge:

```Swift
func isogram(_ Word:String) -> Void{
    let word = Array(Word)
    var repated : Set = Set<Character>()
    var isogramorNot = false
    for index1 in 1...word.count-1{
        for index2 in 1...word.count-1{
            if ((word[index1] == word[index2]) && (index1 != index2)){
                if !repated.contains(word[index2]) {
                    repated.insert(word[index2])
                    isogramorNot = true
                }
            }
        }
    }
    if isogramorNot{
        print(repated)
    }else
    {
        print("false")
    }
}

isogram("tomorrow")
//["r", "o"]
isogram("today")
//false

```

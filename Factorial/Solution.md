# Solution:
```Swift
func factorialOF(_ num: Int) -> Int? { 
    if num == 0 {
        return 1
    }else if num < 0 {
        print("Input cannot be negtive")
        return nil
    }else{
       return num * factorialOF(num - 1)!
    }
}
print(factorialOF(5) ?? "0")
```

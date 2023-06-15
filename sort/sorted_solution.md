## Soulution
```Swift
//let nums = [9,6,10,7]
let nums = [110,10,11,1000]

func smallest(in nums:[Int]) -> (small:Int,inde:Int){
    var smallest = nums[0]
    var inde = 0
    for index in 0...nums.count-1{
        if smallest < nums[index] {
            continue
        }else{
            smallest = nums[index]
            inde = index
        }
    }
    return (smallest,inde)
}

func sort(_ nums:[Int]) -> [Int] {
    var sorted = [Int]()
    var numscopy = nums
    for _ in 0...numscopy.count-1{
        var y = smallest(in: numscopy)
        sorted.append(y.small)
        numscopy.remove(at:y.inde)
    }
    return sorted
}

print(sort(nums))
//[10, 11, 110, 1000]
```

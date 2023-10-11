# Albareno-assignment

## Problem Two

This is the solution of problem two of coding assessment 

```javascript
const problemTwo = (arr) => {
    const refObj = {}
    
    for(let i = 0; i < arr.length; i++) {
        refObj[arr[i].split("").sort().join("")] = []
    }
    
    for(let i = 0; i < arr.length; i++) {
        refObj[arr[i].split("").sort().join("")].push(arr[i])
    }
    
    return Object.values(refObj)
}
```
## Problem Four
This is the solution of problem four of coding assessment

```javascript
const problemFour = (arr) => {
    for (let i = 0; i < arr.length; i++) {
        arr[i] = String(arr[i])
    }
    
    // 934 or 349
    arr = arr.sort((a, b) => {
        orderOne = a + b
        orderTwo = b + a
        return orderTwo.localeCompare(orderOne)
    })
    
    return arr.join("")
}
```

## Problem Five 

This is the solution of problem five of coding assessment 

```javascript
const problemFive = (arr, k) => {
    let currElem = 0
    while (k > 0) {
        let poppedElem = Math.max(...arr)
        arr.splice(arr.indexOf(poppedElem), 1)
        currElem = poppedElem
        k -= 1
    }
    
    return currElem
}
```

# Failed to solve 

## Problem One
This is my code for problem one which I unfortunately failed to solve 

```javascript
const problemOne = (x) => {
    //  reversing
    x = String(x)
    const arr = x.split("")
    
    let l = 0
    let r = arr.length - 1
    
    while(l < r){
        temp = arr[l]
        arr[l] = arr[r]
        arr[r] = temp
        
        l += 1
        r -= 1
    }
    
    const newNum = Number(arr.join(""))
    console.log(newNum)
    
    // finding prime factors
    const primeFactorsArray = []
    if (newNum / 2 === 0) {
        primeFactorsArray.push(2)
    }
    
    if (newNum / 3 === 0) {
        primeFactorsArray.push(3)
    }
    
    let i = 0
    
    // prime numbers are represented by 6(n) + 1 or 6(n) - 1 
    while(true){
        if (((6 * i) + 1) < newNum) {
        
            if ((newNum / ((6 * i) + 1)) === 0) {
                primeFactorsArray.push(((6 * i) + 1))
            }
            if ((newNum / ((6 * i) - 1)) === 0) {
                primeFactorsArray.push(((6 * i) - 1))
            }
        }
        else {
            break 
        }
        i += 1
    }
    
    console.log(primeFactorsArray)
    
    if (primeFactorsArray.length > 0) {
        return ["YES", primeFactorsArray]
    } else {
      return "NO"
    }
}

console.log(problemOne(22))
```


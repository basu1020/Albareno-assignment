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


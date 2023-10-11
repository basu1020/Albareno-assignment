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

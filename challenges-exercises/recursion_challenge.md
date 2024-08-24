# **Recursion challenge**

### From:
#### https://www.joelonsoftware.com/2005/12/29/test-yourself/

---

The problem statement:

> Using the function
> ```javascript
> function accumulate(combiner, nullValue, l)
> {
> 	if (l.length == 0)
> 		return nullValue;
> 	var first = l.shift();
> 	return combiner(first, accumulate(combiner, nullValue, l));
> }
> ```
> Implement sumOfSquares, which calculates the sum of squares of a list, for example
> `sumOfSquares([1,2,3,4,5])`
> should evaluate to 55.

<details>
<summary>Click to see the solution</summary>

```javascript
function sumOfSquares(arr){
    accumulate((i, fun)=>i*i+fun, 0, arr)
}
```

</details>
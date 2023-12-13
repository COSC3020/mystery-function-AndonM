[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11974257&assignment_repo_type=AssignmentRepo)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

In the base case, for an array containing only one element, we will return this element. Otherwise, we work our way down to the base case by slicing from the second element through to the last. In other words we weed out the first element with each iteration. This value is stored and we make a comparison. If the maximal element from the rest of the array is greater than the first element, said maximal element becomes the return value; otherwise we keep the first element as the maximum. Through recursion we repeat this process until the array is of length one, at which point we return the greatest element. In any case, we return the greatest element in a non-empty array.

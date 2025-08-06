### Problem
  
* As a developer, you are tasked with improving a tech-savvy restaurant’s reservation system.
* Your mission: fix a bug in the transposeSeating function that rearranges seating charts.
* Inspect the provided JavaScript code and correct it to ensure the seating layout is properly transposed.
* Analyze the code, identify the error, and adjust the function.


### Solution

```js
    // TODO: Fix the function to transpose a seating arrangement represented as a 2D array
function transposeSeating(seating) {
    let rows = seating.length;
    let cols = rows > 0 ? seating[0].length : 0;
    let transposed = [];

    for (let i = 0; i < cols; ++i) {
        transposed[i] = [];
        for (let j = 0; j < rows; ++j) {
            transposed[i][j] = seating[j][i];
        }
    }

    return transposed;
}

// Sample restaurant seating arrangement represented as a 2D array
let restaurantSeating = [
    [10, 11, 12],
    [20, 21, 22]
];

// Trying to transpose the seating arrangement
let transposedSeating = transposeSeating(restaurantSeating);

for (let row of transposedSeating) {
    console.log(row.join(' '));
}
// Output isn't as expected. Can you identify the fix?
```


### Reversing the transpose

```js
function transformMatrix(matrix) {
    let rows = matrix.length;
    let cols = rows > 0 ? matrix[0].length : 0;
    let result = [];

    // TODO: Modify the loop to transpose the matrix in reverse order
    
    for(let i = 0;i<cols; ++i ){
        result[i] = []
         for(let j = 0;j<rows; ++j ){
        
        result[i][j] =matrix[j][cols-i-1]
    }
    }

    return result;
}

// let matrix = [
//     [101, 102, 103, 104],
//     [201, 202, 203, 204],
//     [301, 302, 303, 304]
// ];
let matrix = [
      [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];

// TODO: Store the result of transformMatrix in transposedMatrix and print it

const transformedMatrix = transformMatrix(matrix)


console.log(transformedMatrix)
```

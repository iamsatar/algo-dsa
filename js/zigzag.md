# zigzag Traversal

- a zigzag traversal of a grid in JavaScript, mimicking the navigation of library bookshelves. Start at the bottom-right corner, move upwards in the last column, then downwards in the previous column, alternating directions. Traverse each column in this zigzag pattern and collect the items. Good luck!


#### Example

Given the grid:

```js
    const grid = [
    [101, 102, 103, 104],
    [201, 202, 203, 204]
];
```

#### The correct zigzag traversal should return:

```js
   [204, 104, 103, 203, 202, 102, 101, 201]
```


#### Solution

```js

	function zigzagTraverse(grid) {
    // TODO: Determine the number of rows and columns in 'grid'
    
    const traversalPath = [];
    const rows = grid.length ;
    const cols = grid[0].length ;
    let row = rows - 1;
    let col = cols - 1;
    let index = 0;
    let direction = "up";
    
    while(index < rows * cols){
     traversalPath[index] = grid[row][col];

        if (direction === "up") {
            if (row - 1 < 0) {
                direction = "down";
                col -= 1;
            } else {
                row -= 1;
            }
        } else {
            if (row + 1 === rows) {
                direction = "up";
                col -= 1;
            } else {
                row += 1;
            }
            }
       



        index++
    }
    
    
    // TODO: Traverse 'grid' in a zigzag pattern starting from the bottom right
    
    return traversalPath;
}

const grid = [
    [101, 102, 103, 104],
    [201, 202, 203, 204]
];

const zigzagGrid = zigzagTraverse(grid)

console.log(zigzagGrid)

// TODO: Print the zigzag traversal path of items in 'grid'


// 0,3,6,9,12


```

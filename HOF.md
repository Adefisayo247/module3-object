# # Explain HOF WITH EXAMPLE

HOF is an abbreviation for HIGHER-ORDER FUNCTIONS. Higher order functions are functions that operate on other functions, either by taking them as arguments or by returning them. In simple words, A Higher-Order function is a function that receives a function as an argument or returns the function as output. 
For example, Array.prototype.map, Array.prototype.filter and Array.prototype.reduce are some of the Higher-Order functions built into the language.

# # # EXAMPLE
```
const strArray = ['JavaScript', 'Python', 'PHP', 'Java', 'C'];
function mapForEach(arr, fn) {
  const newArray = [];
  for(let i = 0; i < arr.length; i++) {
    newArray.push(
      fn(arr[i])
    );
  }
  return newArray;
}
const lenArray = mapForEach(strArray, function(item) {
  return item.length;
});
// prints [ 10, 6, 3, 4, 1 ]
console.log(lenArray);
```

# # # MAP METHOD WITH EXAMPLE
    Array.prototype.map
The map() method creates a new array by calling the callback function provided as an argument on every element in the input array. The map() method will take every returned value from the callback function and creates a new array using those values.
The callback function passed to the map() method accepts 3 arguments: element, index, and array.

# # # EXAMPLE
Let’s look at some examples:

```
const birthYear = [1975, 1997, 2002, 1995, 1985];
const ages = birthYear.map(year => 2018 - year);
// prints [ 43, 21, 16, 23, 33 ]
console.log(ages);

```
```
const products =[
  {
  name: 'laptop',
  amount: 7000,
  count: 5
  },
  {
    name: 'desktop',
    amount:3000,
    count: 7
    },
    {
      name: 'phone',
    amount:3000,
    count: 10
    }
  ];
  const totalProductsValue = products.map(item => ({
    name: item.name,
    totalValue: item.amount * item.count
  }));

  console.log(totalProductsValue);
  [ { name: 'laptop', totalValue: 35000 },
  { name: 'desktop', totalValue: 21000 },
  { name: 'phone', totalValue: 30000 } ] //RESULT/PRINTS
   
  ```

  # # # REDUCE METHOD WITH EXAMPLE
The reduce method executes the callback function on each member of the calling array which results in a single output value. The reduce method accepts two parameters: 
1) The reducer function (callback)
2) and an optional initialValue.

The reducer function (callback) accepts four parameters: accumulator, currentValue, currentIndex, sourceArray.
If an initialValue is provided, then the accumulator will be equal to the initialValue and the currentValue will be equal to the first element in the array.
If no initialValue is provided, then the accumulator will be equal to the first element in the array and the currentValue will be equal to the second element in the array.

# # # EXAMPLE

```
const euros = [29.76, 41.85, 46.5];

const average = euros.reduce((total, amount, index, array) => {
  total += amount;
  if( index === array.length-1) { 
    return total/array.length;
  }else { 
    return total;
  }
});

average // 39.37

```
//MARKUP LINK
https://adefisayo247.github.io/responsive-markup/responsive%20markup/index.html

//CODEALONG FOR 2020 MODULE THREE OBJECTS
https://adefisayo247.github.io/module3-object/
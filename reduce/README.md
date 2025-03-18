### Excercice 1: find a sum of all numbers that are bigger or equal to 3

```
const arr = [1, 2, 3, 5, 6, 7, 4, 1];

function getSumBiggerThan(arr, value) {
    const reducer = (acc, value) => acc + value;
    return arr.filter(arrValue => arrValue >= value).reduce(reducer, 0);
}

console.log(getSumBiggerThen(arr, 3));
```

### Excercice 2: return a count of duplicate words in that string
```
const str = 'one two three two one one four five'; // 2

function countDuplicate(str) {
    const strArray = str.split(" ");
    const reducer = (acc, value) => {
        acc[value] = (acc[value] || 0) + 1;
        return acc;
    }
    const strObject = strArray.reduce(reducer, {});
    return Object.values(strObject).filter(value => value > 1).length;
}
console.log(countDuplicate(str))
```


### Excercice 3: Use reduce() to find the sum
```
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.reduce((acc, value) => acc + value, 0));
```

### Excercice 4: Use reduce() to find the max value
```
const numbers = [10, 5, 20, 8, 15];
console.log(numbers.reduce( (acc, value) => {
    return value >= acc ? value : acc;
},0));
```


### Exercice 5: Remove duplicates from an array using reduce():

```
const numbers = [1, 2, 2, 3, 4, 4, 5];

const uniqueNumbers = numbers.reduce((acc, num) => {
  if (!acc.includes(num)) acc.push(num);
  return acc;
}, []);

console.log(uniqueNumbers); // [1, 2, 3, 4, 5]
```

### Excercice 6: Transform an array of key-value pairs into an object using reduce()
```
const keyValuePairs = [['name', 'Alice'], ['age', 25], ['city', 'Paris']];

const obj = keyValuePairs.reduce((acc, [key, value]) => {
  acc[key] = value;
  return acc;
}, {});

console.log(obj); // { name: 'Alice', age: 25, city: 'Paris' }

// Since ES2019, Object.fromEntries() provides a built-in way to do this:
const obj = Object.fromEntries(keyValuePairs);
console.log(obj); // { name: 'Alice', age: 25, city: 'Paris' }
```

### Excercice 7: Use reduce() to count occurrences
```
const fruits = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple'];

function countOccurences(fruits) {
    const reducer = (acc, value) => {
        acc[value] = (acc[value] || 0) + 1
        return acc;
    };
    
    return fruits.reduce(reducer, {});
}

console.log(countOccurences(fruits));
```

### Excercice 7: Use reduce() to flatten the array
```
const nested = [[1, 2], [3, 4], [5, 6]];

function flatten(nested) {
    const reducer = (acc, value) => acc.concat(value)

    return nested.reduce(reducer, []);
}

console.log(flatten(nested));
```

### Excercice 8: Use reduce() to concatenate into a single string
const words = ['Hello', 'world', 'this', 'is', 'JavaScript'];

function concatenation(words) {
    return words.reduce((acc, value) => `${acc} ${value}`, "").trim();
}

console.log(concatenation(words));

// Alternative using join() 
const sentence = words.join(' ');
console.log(sentence); // "Hello world this is JavaScript"

### Exercice 9: Use reduce() to calculate total cart price
const cart = [
    { product: 'Laptop', price: 1000, quantity: 2 },
    { product: 'Mouse', price: 50, quantity: 3 },
    { product: 'Keyboard', price: 80, quantity: 1 }
];


function getTotalCart(cart) {
    return cart.reduce( (acc, { price, quantity }) => acc + (price * quantity), 0);
};

console.log(getTotalCart(cart)); // 2 230


### Exercice 10: Use reduce() to count character occurrences
const text1 = "hello world";
const text2 = "one two three two three three";

function getCharCount(text, spliter) {
    const reducer = (acc, value) => {
        if(value !== ' ') {
            acc[value] = (acc[value] || 0) + 1
        }
        return acc;
    };

    return text.split(spliter).reduce(reducer, {});
};

console.log(getCharCount(text1, '')); // { h: 1, e: 1, l: 3, o: 2, w: 1, r: 1, d: 1 }
console.log(getCharCount(text2, ' ')); // { one: 1, two: 2, three: 3 }

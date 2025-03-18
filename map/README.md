### Exercice 1: Doubler les valeurs d’un tableau
```
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.map(value => value*2))
```

### Exercice 2: Convertir un tableau de prix en TVA incluse (20%)
```
const prices = [10, 20, 30, 40];
console.log(prices.map(value => value + (value * 0.2)))
```

### Exercice 3: Transformer un tableau de noms en majuscules
```
const names = ["alice", "bob", "charlie"];
console.log(names.map(value => value.toUpperCase()))
```

### Exercice 4:  Extraire les noms d’un tableau d’objets
```
const users = [
    { name: "Alice", age: 25 },
    { name: "Bob", age: 30 },
    { name: "Charlie", age: 22 }
];
console.log(users.map(({name, age}) => name))
```

### Exercice 5: Créer un tableau de longueurs de mots
```
const words = ["apple", "banana", "cherry"];
console.log(words.map(value => value.length))
```
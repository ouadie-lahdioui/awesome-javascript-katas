
### Exercice 1: Filtrer les nombres pairs d’un tableau
```
const numbers = [1, 2, 3, 4, 5, 6, 7, 8];
console.log(numbers.filter(value => value%2 === 0))
```

### Exercice 2: Garder uniquement les mots de plus de 5 lettres
```
const words = ["chat", "éléphant", "chien", "hippopotame"];
console.log(words.filter(value => value.length > 5))
```

### Exercice 3: Récupérer les utilisateurs majeurs d’un tableau d’objets
```
const users = [
    { name: "Alice", age: 25 },
    { name: "Bob", age: 17 },
    { name: "Charlie", age: 19 }
];
console.log(users.filter((({age}) => age >= 18)));
```
### Exercice 4: Supprimer les valeurs nulles ou indéfinies d’un tableau
```
const values = [10, null, 20, undefined, 30, "", 40];
console.log(values.filter(value => value));
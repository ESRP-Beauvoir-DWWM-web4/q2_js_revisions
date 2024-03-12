La boucle `while`

Il existe en javascript plusieurs types de boucles, ici nous allons voir la boucle tant que

Par exemple si je veux faire en sorte qu'une variable initialisée à 0 atteigne le chiffre 10, on fera en sorte de bouclé tant que le chiffre n'a pas atteint 10 et en utilisant un opérateur d'addition

```javascript
let i = 0

while(i < 10) {
    i = i + 1
    console.log(i)
}
```

ATTENTION : Si cette boucle est mal implémentée, elle peut générer une boucle infinie qui risque de faire planter vôtre navigateur

Il y a aussi la boucle `pour` 

Je veux faire le même traitement que précédemment mais avec une boucle for

```javascript
for (let i = 0; i <= 10; i++) {

    console.log(i)

}
```

L'opérateur ++ en dernier paramètre signifie "+1"

La boucle for peut aussi dissocier des éléments d'un tableau

```javascript
const notes = [10, 12, 15, 18, 12, 13, 14, 20]

for ( let i = 0; i < notes.length; i++ ) {
    console.log(notes[i])
}
```

Nous pouvons aussi utiliser une autre syntaxe avec `for in`

```javascript
for ( let note in notes ) {
    console.log(notes[note])
}
```

Et une autre en `for of`

```javascript
for ( let note of notes ) {
    console.log(note)
}
```

Cela fonctionne aussi pour les objets

```javascript
const notes = {
    a : 10,
    b : 12,
    c : 15,
    d : 18,
    e : 12,
    f : 13,
    g : 14,
    h : 20
}

for ( let note in notes ) {
    console.log(notes[note])
}
```

ATTENTION : Si vous faites un for of, cela ne fonctionnera pas pour les objets car ils ne sont pas itératifs

```javascript
for ( let note of notes ) {
    console.log(notes[note])
}
```

Les boucles fonctionnent aussi sur les chaines de caractères

```javascript
const chaine = "Bonjour les amis"

for ( let lettre of chaine ) {
    console.log(lettre)
}
```

Voici une boucle que vous croiserez souvent sur React et qui concerne les objets

```javascript
const personnes = [
    {
        nom : "Doe",
        prenom : "John"
    },
    {
        nom : "Dan",
        prenom : "Jane"
    },
    {
        nom : "Durand",
        prenom : "Eustache"
    },
    {
        nom : "Krieger",
        prenom : "Max"
    },
]

personnes.map(personne => (
    console.log(personne.prenom)
))
```

Une dernière boucle peut être opérée pour les tableaux et les objets

```javascript
const fruits = ['Pomme', 'Banane', 'Orange', 'Fraise']

fruits.forEach((fruit) => {
    console.log(fruit)
})
```

```javascript
const students = [
    {
        nom : "Jo"
    },
    {
        nom : "Jim"
    },
    {
        nom : "Olivier"
    },
    {
        nom : "Karl"
    },
]

students.forEach((student) => {
    console.log(student.nom)
})
```

### Exercices

### 1

Mettez en place une variable initialisée à 0 et faites en sorte d'afficher des chiffres de 2 en 2 jusqu'à 20 en utilisant une boucle

```javascript
let nombre = 0;

while (nombre <= 20) {
    console.log(nombre);
    nombre = nombre +2; // Incrémentation du compteur
}
```

### 2

Faites un mini jeux pour deviner un nombre

Initialisez une variable avec le nombre à deviner et mettez en place un traitement

Une modale qui demandera d'entrer votre chiffre (Attention les prompt sont considéré comme des chaines de caractères)

Une modale qui dira si le chiffre entré est plus grand que celui à deviner

Une modale qui dira si le chiffre entré est plus petit que celui à deviner

Une modale qui affichera un message de victoire

```javascript
let aDeviner = 8
let chiffre

while ( chiffre !== aDeviner ) {
    chiffre = prompt("Quel est le chiffre à deviner") * 1
    if ( chiffre < aDeviner ) {
        alert("Le chiffre est plus grand")
    } else if ( chiffre > aDeviner ) {
        alert("Le chiffre est plus petit")
    }
}

alert("Bravo vous avez gagné !")
```

ou

```javascript
let aDeviner = 8
let chiffre

while ( chiffre !== aDeviner ) {
    chiffre = parseInt(prompt("Quel est le chiffre à deviner"))
    if ( chiffre < aDeviner ) {
        alert("Le chiffre est plus grand")
    } else if ( chiffre > aDeviner ) {
        alert("Le chiffre est plus petit")
    }
}

alert("Bravo vous avez gagné !")
```

### 3

Mettez en place grâce à la boucle for un système qui additionnera tous les chiffres pairs entre 0 et 10

```javascript
// Initialisation de la variable de somme
let somme = 0;

// Boucle for pour calculer la somme des nombres pairs de 1 à 10
for (var i = 2; i <= 10; i += 2) {
    somme += i;
}

// Affichage du résultat
console.log("La somme des nombres pairs de 1 à 10 est : " + somme);
```

### 4 - Exercice global sur les variables, les conditions et les boucles

Mettez en place un système qui demande à l'utilisateur de saisir un nombre. 

Ensuite, la console doit afficher si ce nombre est pair ou impair. 

La console doit également afficher la table de multiplication de ce nombre jusqu'à 10.

```javascript
// Demander à l'utilisateur de saisir un nombre
let nombre = parseInt(prompt("Veuillez saisir un nombre :"));

// Vérifier si le nombre est pair ou impair
if (nombre % 2 === 0) {
    console.log(nombre + " est un nombre pair.");
} else {
    console.log(nombre + " est un nombre impair.");
}

// Afficher la table de multiplication jusqu'à 10
console.log("Table de multiplication de " + nombre + ":");
for (let i = 1; i <= 10; i++) {
    console.log(nombre + " x " + i + " = " + (nombre * i));
}
```
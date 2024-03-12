Une fonction est un bloc de code qui peut être appelé par d'autres parties de votre code pour effectuer une tâche spécifique. Les fonctions peuvent prendre des paramètres et renvoyer une valeur en fonction de ce qui est défini à l'intérieur.

```javascript
function majeur(age) {
    if( age < 18 ) {
        console.log("Vous êtes mineur")
    } else {
        console.log("Vous êtes majeur")
    }
}

majeur(16)
majeur(14)
majeur(18)
```

Il existe une autre syntaxe que vous serez susceptible d'utiliser dans React, c'est la fonction fléchée

```javascript
const majeur = (age) => {
    if( age < 18 ) {
        console.log("Vous êtes mineur")
    } else {
        console.log("Vous êtes majeur")
    }
}

majeur(16)
majeur(14)
majeur(18)
```

### Exercices

### 1

Mettez en place une fonction qui calculera l'aire d'un rectangle

```javascript
// Définition de la fonction calculerSurfaceRectangle
function calculerSurfaceRectangle(longueur, largeur) {
    console.log(`L'aire du rectangle est de : ${longueur * largeur} cm²`);
}

let longueur = parseInt(prompt("Entrer la longeur"))
let largeur = parseInt(prompt("Entrer la largeur"))
  
calculerSurfaceRectangle(longueur, largeur)
```

### 2

Mettez en place une fonction qui compte le nombre de fois qu'un caractère apparait dans une phrase

```javascript
function compterOccurences(phrase, caractere) {
    let compteur = 0;
    for (let i = 0; i < phrase.length; i++) {
        if (phrase[i] === caractere) {
            compteur++;
        }
    }
    return compteur;
}

// Exemple de test

let phrase = "Bonjour tout le monde";
let caractere = "o"

console.log(`Le caractère "${caractere}" apparait "${compterOccurences(phrase, caractere)}" fois dans la phrase "${phrase}"`)
```


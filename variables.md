## Les variables

### Les types de variables

Les variables en Javascript sont de plusieurs type : 

Les variables en chaine de caractères

```javascript
let a = "Bonjour à tous"
```

Les variables numériques entières

```javascript
let b = 10
```

Les variables numériques flottantes

```javascript
let c = 2.5
```

Les variables booléenne qui contiennent deux paramètres, soit `true` soit `false`

```javascript
let e = true
let f = false
```

Les variables de tableaux

```javascript
let tab1 = [1, 2, 3, 4]
```

Les variables d'objets

```javascript
let object = {
	a : 1,
	b : 2,
	c : 3
}
```
### Affichage des variables

Les variables peuvent être affichées dans la console de votre navigateur de deux manières

Une fois dans la console vous tapez le nom de vôtre variable et elle devrait s'afficher

Soit vous mettez en place un console.log

```javascript
console.log(a)
```

### Les déclarations

Contrairement à PHP, une variable en javascript s'instancie avec une déclaration

Soit `let`, soit `const`

Déclarons d'abord nôtre variable avec `let`.

```javascript
let ma_variable = "Je suis une variable let"
```

Si en cours de route sur mon code je décide de changer la valeur de ma variable

```javascript
ma_variable = "Je suis un oiseau"
```

Dans ce cas si nous affichons la variable dans un console.log(), nous obtiendrons la nouvelle valeur.

Déclarons à présent une variable avec `const`

```javascript
const ma_variable2 = "Je pense"
```

Si nous changeons la valeur de cette variable

```javascript
ma_variable2 = "Je suis"
```

Si nous affichons la variable avec console.log(), une erreur survient

```
Uncaught TypeError: Assignment to constant variable.
    at script.js:13:3
```

Une autre déclaration existe c'est `var` mais elle est de moins en moins utilisée à cause de sa portée. En effet en utilisant `var` on peut sortir une variable de sa fonction ce qui peut aboutir à des erreurs.

### Les différences dans la chaine de caractère

Vous pouvez écrire une chaine de caractère avec des `doubles guillemets`

```javascript
let phrase = "Bonjour, je me nomme Bob"
```

C'est la manière la plus répandue pour déclarer une chaine de caractères mais elle présente une subtilité

En effet si vous voulez accentuer un mot dans une phrase avec des guillemets, vous allez devoir échapper la chaine de caractère

ERREUR : 

```javascript
let phrase = "Bonjour je suis "Bob" et je vais bien"
```

SANS ERREURS : 

```javascript
let phrase = "Je suis \"bob\" et je vais bien"
```

Si vous souhaitez revenir à la ligne sans que cela pose de problèmes, on pourra échapper la chaine de caractères avec une autre méthode

```javascript
let phrase = "Je suis bob et je vais bien\net je suis souriant"
```

On peut écrire une chaine de caractères avec des `guillemets simples` et si nous souhaitons mettre un mot avec une apostrophe, il faudra aussi échapper la chaine de caractères

Nous pouvons aussi utiliser des antiquotes qui ont une fonction intéressante au niveau de la concaténation.

Je vais déclarer une variable qui contiendra un prénom et je vais l'ajouter à une phrase en utilisant les antiquotes

```javascript
const name = "Bob"

let phrase = `Je m'appelle ${name}`

console.log(phrase)
```

Les antiquotes permettent aussi de passer à la ligne sans échapper la chaine de caractères

```javascript
let phrase = `Bonjour comment vas tu ?
Je vais bien et toi`
```

### Les tableaux et objets

Les tableaux indexés contiennent des données ayant des indexes prédéfinis.

Mettons en place un tableau avec 4 valeurs numériques

```javascript
let tab = [1, 2, 3, 4]
```

En faisant un console.log() sur ce tableau nous obtiendrons la liste des valeurs précédé de leur index

```
0 > 1
1 > 2
2 > 3
3 > 4
```

Les index commencent par un 0

Les index peuvent servir à identifier une valeur dans le tableau, par exemple si je cherche à isoler le chiffre 3 en n'affichant que lui, j'appelle dans le console.log() la variable contenant le tableau suivi de l'index entre crochets

```javascript
console.log(tab[2])
```

Pour un objet, c'est à nous de déclarer les index selon nôtre bon vouloir, par exemple je veux afficher des données sur une personne

```javascript
let tab = {
    nom : "Doe",
    prenom : "John",
    age : "38"
}
```

Comme pour le tableau indexé, on peut afficher une seule donnée

```javascript
console.log(tab["prenom"])
```


Une manière plus rapide d'afficher le prénom est de faire un console.log() de cette manière : 

```javascript
console.log(tab.prenom)
```

C'est cette manière que vous rencontrerez dans React.

Vous trouverez parfois des objets avec des tableaux imbriqués ou objets imbriqués

```javascript
let tab = {
    nom : "Doe",
    prenom : "John",
    notes : [10, 14, 17],
    coordonnees : {
        telephone : "0123456789",
        adresse : "3 rue de la tour",
        code_postal : 35000,
        ville : "Rennes"
    }
}

console.log(tab.notes[1])
console.log(tab.coordonnees.adresse)
```

Dans le cadre du tableau imbriqué, on peut appeler l'objet puis l'index du tableau.
Dans le cadre de l'objet imbriqué, il suffit d'appeler l'index de l'objet et l'index de l'objet imbriqué.

Nous pouvons également modifier les valeurs des objets.

```javascript
let tab = {
    nom : "Doe",
    prenom : "John",
    notes : [10, 14, 17],
    coordonnees : {
        telephone : "0123456789",
        adresse : "3 rue de la tour",
        code_postal : 35000,
        ville : "Rennes"
    }
}

console.log(tab.notes[1])
console.log(tab.coordonnees.adresse)

tab.coordonnees.adresse = "3 rue de la place"

console.log(tab.coordonnees.adresse)
```

Petite chose intéressante, si vous afficher le type du tableau de notes : 

```javascript
let tab = {
    nom : "Doe",
    prenom : "John",
    notes : [10, 14, 17],
    coordonnees : {
        telephone : "0123456789",
        adresse : "3 rue de la tour",
        code_postal : 35000,
        ville : "Rennes"
    }
}

console.log(typeof tab.notes)
```

Vous obtiendrez un objet

En javascript toute les variables sont des objets avec des propriétés et ces objets peuvent avoir des propriétés.

Si je veux par exemple le nombre de caractères du prénom de nôtre objet il suffit de faire comme ça : 

```javascript
console.log(tab.prenom.length)
```

### EXERCICES

### 1

Demander à l'utilisateur de rentrer son nom dans une modale
Demander à l'utilisateur de rentrer son âge dans une modale
Afficher dans une modale la phrase suivante : 

Bonjour Nom ! Vous avez nombre ans

```javascript
// Demander à l'utilisateur de saisir son nom
let nom = prompt("Quel est votre nom ?");

// Demander à l'utilisateur de saisir son âge
let age = prompt("Quel est votre âge ?");

// Afficher un message de salutation personnalisé
alert("Bonjour " + nom + "! Vous avez " + age + " ans.");
```

### 2

Déclarez une variable "entier" et initialisez un nombre entier
Déclarez une variable "float" et initialisez un nombre flottant
Déclarez une variable "chaine" et initialisez la chaine de caractères suivante : "Le résultat est : "

Ajoutez une variable qui additionnera la variable "entier" avec la variable "float"
Convertissez le résultat en chaine de caractères
Concaténer le résultat convertit à la variable "chaine" 

```javascript
// Déclaration et initialisation des variables
let entier = 10;
let decimal = 5.5;
let chaine = "Le résultat est : ";

// Ajout de l'entier à la variable decimal
decimal += entier;

// Conversion du résultat en une chaîne de caractères
let resultatString = decimal.toString();

// Concaténation de la chaîne avec le résultat
let resultatFinal = chaine + resultatString;

// Affichage du résultat final
console.log(resultatFinal);
```

### 3

Créez un objet "etudiant" avec les propriétés suivante : nom, âge, classe

Afficher dans la console les objets avec les détails suivants : 

Nom de l'étudiant : Nom
Age de l'étudiant : Age

etc...

```javascript
// Création de l'objet étudiant
let etudiant = {
    nom: "Jean Dupont",
    age: 20,
    classe: "B3 Informatique"
};

// Affichage des détails de l'étudiant
console.log("Nom de l'étudiant : " + etudiant.nom);
console.log("Âge de l'étudiant : " + etudiant.age);
console.log("Classe de l'étudiant : " + etudiant.classe);
```

### 4

Vous avez un tableau de noms d'animaux. Mettez en place un code JavaScript qui effectue les opérations suivantes :

Affichez la longueur du tableau : "La longueur du tableau est : "
Ajoutez un nouvel animal à la fin du tableau.
Affichez le nouveau tableau avec le nouvel animal ajouté : "Nouveau tableau avec le nouvel animal ajouté : "

```javascript
// Tableau de noms d'animaux
let animaux = ["Chat", "Chien", "Lapin", "Oiseau", "Souris"];

// Affichage de la longueur du tableau
console.log("La longueur du tableau est : " + animaux.length);

// Ajout d'un nouvel animal à la fin du tableau
animaux.push("Poisson");

// Affichage du nouveau tableau avec le nouvel animal ajouté
console.log("Nouveau tableau avec le nouvel animal ajouté : " + animaux);

```


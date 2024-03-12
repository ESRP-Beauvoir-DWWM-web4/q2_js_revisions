Pour commencer nous allons créer une variable contenant un âge et nous allons mettre en place des conditions qui afficheront des messages selon certains critères.

```javascript
let age = 20

if ( age < 18 ) {
    console.log("Vous nêtes pas majeur")
} else if ( age >= 18 ) {
    console.log("Vous êtes majeur")
}
```

Il existe une autre syntaxe que vous rencontrerez dans React et qui s'implémente de la manière suivante : 

```javascript
let age = 17

{age < 18 &&(
    console.log("Vous nêtes pas majeur")
)}

  

{age >= 18 &&(
    console.log("Vous êtes majeur")
)}
```

Nous pouvons aussi découvrir grâce aux conditions si un chiffre est pair ou impair

```javascript
let num = 3

if ( num % 2 == 0 ) {
    console.log(`${num} est pair`)
} else if ( num % 2 == 1 ) {
    console.log(`${num} est impair`)
}
```

### Exercices

### 1

Écrivez un programme JavaScript qui vérifie si un nombre est positif, négatif ou nul. Affichez ensuite le résultat correspondant.

```javascript
// Déclaration du nombre à vérifier
let nombre = 3;

// Vérification si le nombre est positif, négatif ou nul
if (nombre > 0) {
    console.log("Le nombre est positif.");
} else if (nombre < 0) {
    console.log("Le nombre est négatif.");
} else {
    console.log("Le nombre est nul.");
}
```

### 2

Mettez en place une condition JavaScript dans une fonction "determinerMention()" qui prend en compte les notes d'un étudiant et détermine sa mention en fonction de sa note. Les mentions sont définies comme suit :

- Une note entre 0 et 9 inclus : "Insuffisant"
- Une note entre 10 et 11 inclus : "Passable"
- Une note entre 12 et 13 inclus : "Assez bien"
- Une note entre 14 et 15 inclus : "Bien"
- Une note entre 16 et 20 inclus : "Très bien"

Affichez ensuite la mention obtenue par l'étudiant en fonction de sa note.

```javascript
// Fonction pour déterminer la mention en fonction de la note
function determinerMention(note) {
    if (note >= 0 && note < 10) {
        return "Insuffisant";
    } else if (note >= 10 && note < 12) {
        return "Passable";
    } else if (note >= 12 && note < 14) {
        return "Assez bien";
    } else if (note >= 14 && note < 16) {
        return "Bien";
    } else if (note >= 16 && note <= 20) {
        return "Très bien";
    } else {
        return "Note invalide";
    }
}

// Déclaration de la note de l'étudiant
let noteEtudiant = 5;

// Affichage de la mention obtenue par l'étudiant
console.log("Mention obtenue : " + determinerMention(noteEtudiant));
```

### 3

Vous êtes en train de développer un système de gestion de billets de concert en ligne. Écrivez un programme JavaScript qui vérifie l'âge d'un utilisateur et détermine le tarif du billet en fonction de son âge. Voici les règles :

Les enfants de moins de 6 ans entrent gratuitement.
Les enfants de 6 à 12 ans paient demi-tarif.
Les adultes de 13 à 64 ans paient le tarif plein.
Les personnes âgées de 65 ans et plus paient demi-tarif.

Écrivez une fonction `calculerTarifBillet(age)` qui prend en paramètre l'âge de l'utilisateur et retourne le tarif du billet.

```javascript
function calculerTarifBillet(age) {
    if (age < 6) {
        return "Gratuit";
    } else if (age >= 6 && age <= 12) {
        return "Demi-tarif";
    } else if (age >= 13 && age <= 64) {
        return "Tarif plein";
    } else {
        return "Demi-tarif";
    }
}

// Test de la fonction avec différents âges
console.log("Âge : 3, Tarif du billet : " + calculerTarifBillet(3));
console.log("Âge : 8, Tarif du billet : " + calculerTarifBillet(8));
console.log("Âge : 25, Tarif du billet : " + calculerTarifBillet(25));
console.log("Âge : 70, Tarif du billet : " + calculerTarifBillet(70));
```

### 4

Déclarer une variable qui contiendra l'année en cours

Mettez en place une modale qui demandera votre année de naissance

Mettez en place une condition qui vous proposera des films adaptés à vôtre âge

Entre 0 et 13 ans : "Je vous conseille le film Le roi lion"
Entre 14 et 17 ans : "Je vous conseille le film Star Wars"
Sinon : "Je vous conseille le film  Halloween"

```javascript
const age = prompt("Quel est vôtre âge ?")

if ( age <= 13 ) {
    alert("Je vous conseille le film Le roi Lion")
} else if ( age <= 17 ) {
    alert("Je vous conseille le film Star Wars")
} else {
    alert("Je vous conseille le film Halloween")
}
```

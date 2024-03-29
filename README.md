# Cheatsheet-POO-js
- Si vous lisez ca et que vous debuter en js utiliser ce site ; https://fr.javascript.info/

## Les class en JavaScript

**- Syntaxe de base de la Classe** : https://fr.javascript.info/class

- *Qu'est-ce qu'une classe en javascript ?*
**Une classe est un modèle qui peut être utilisé pour créer des objets. Elle définit les propriétés et les méthodes que possèderont ces objets. En utilisant des classes, vous pouvez créer plusieurs objets qui partagent les mêmes propriétés et méthodes, ce qui peut être très pratique dans de nombreux cas.*

### Comment créer une class 

- https://www.gekkode.com/developpement/introduction-aux-classes-et-aux-objets-en-javascript-es6/

``` javascript
 class MaClasse {
  // Constructeur de la classe
  constructor() {
    // Initialisation des propriétés et méthodes de la classe
  }

  // Méthodes de la classe
  maMethode() {
    // Code de la méthode
  }
}
```
**Le constructeur de la classe, qui est une méthode spéciale utilisée pour créer et initialiser un objet créé à partir de cette classe s'écrit de cette maniére :**

``` javascript
// Constructeur de la classe
constructor() {
// Initialisation des propriétés et méthodes de la classe
}
```

**Les méthodes d’une classe sont définies de la même manière que les fonctions, à l’exception du mot-clé « function » qui n’est pas utilisé :**

``` javascript
// Méthodes de la classe
maMethode() {
 // Code de la méthode
}
```

**Accéder aux méthodes d’un objet de la même manière que les propriétés, en utilisant la syntaxe suivante : monObjet.maMethode();**

``` javascript
const monObjet = new MaClasse();
monObjet.maMethode();
```

## Héritage avec les classes

**L'héritage consiste à créer une nouvelle classe à partir d’une classe existante en en héritant les propriétés et les méthodes. Cela permet de réutiliser du code et de faciliter l’organisation**


``` javascript
class Parent {
  constructor(nom) {
    this.nom = nom;
  }

  saluer() {
    console.log(Bonjour, je suis ${this.nom});
  }
}

class Enfant extends Parent {
  constructor(nom, age) {
    super(nom);
    this.age = age;
  }
}

const enfant1 = new Enfant('Marie', 7);
enfant1.saluer(); // Bonjour, je suis Marie
```

### Méthodes statiques

**Les méthodes statiques sont des méthodes qui appartiennent à la classe elle-même et non à ses instances. Elles peuvent être appelées sans avoir à instancier la classe. Par exemple, vous pouvez définir une méthode statique « getAnimalType() » dans la classe Animal qui retourne le type d’animal. Voici un exemple de code :** 

``` javascript
class Animal {
  static getAnimalType() {
    return 'Animal';
  }
}

console.log(Animal.getAnimalType()); // affiche "Animal"
```


## La différence entre un object et une class

### Classe :

**Une classe est comme un plan pour créer quelque chose. Par exemple, imagine que tu as un plan pour créer des personnages dans un jeu vidéo.
Dans ce plan, tu dis qu'un personnage doit avoir certaines choses, comme un nom et un âge. Tu peux également dire qu'un personnage peut faire certaines actions, comme dire bonjour.
En JavaScript, une classe est ce plan. Tu l'écris en utilisant le mot-clé class.
Exemple de plan pour un personnage :**

``` javascript
class Personnage {
  constructor(nom, age) {
    this.nom = nom;
    this.age = age;
  }

  direBonjour() {
    console.log(`Bonjour, je m'appelle ${this.nom} et j'ai ${this.age} ans.`);
  }
}
```


### Objet : 

**Maintenant, imagine que tu utilises ce plan pour créer des personnages spécifiques. Chaque personnage que tu crées est un objet basé sur ce plan.
Tu peux donner à chaque personnage des valeurs spécifiques, comme un nom particulier et un âge.
En JavaScript, un objet est un personnage spécifique que tu crées à partir de ce plan (la classe).
Exemple de création de personnages spécifiques :**

``` javascript
const personnage1 = new Personnage("Alice", 25);
const personnage2 = new Personnage("Bob", 30);

personnage1.direBonjour(); // Affiche : Bonjour, je m'appelle Alice et j'ai 25 ans.
personnage2.direBonjour(); // Affiche : Bonjour, je m'appelle Bob et j'ai 30 ans.
```

*En résumé, une classe est un plan qui dit ce que quelque chose doit avoir et faire, et un objet est une chose spécifique créée à partir de ce plan avec des valeurs spéciales.*


## Programmation Orientée Objets :

### Les concepts fondamentaux de la POO

**Objets :**
*Les objets sont des instances de classes. Ils représentent des entités du monde réel avec des caractéristiques (attributs) et des comportements (méthodes).*

**Attributs :**
*Les attributs sont les caractéristiques d'un objet. Ils représentent les données qu'un objet peut avoir. Par exemple, un objet "Personne" peut avoir des attributs tels que le nom et l'âge.*

**Méthodes :**
*Les méthodes sont les actions qu'un objet peut effectuer. Elles représentent le comportement de l'objet. Par exemple, une méthode "direBonjour" pourrait afficher une salutation.*

**Classes :**
*Une classe est un modèle ou un plan pour créer des objets. Elle définit la structure et le comportement des objets.*

**Constructeurs :**
*Un constructeur est une méthode spéciale dans une classe qui est appelée lorsqu'un nouvel objet est créé. Il initialise les attributs de l'objet.*

**Héritage :**
*L'héritage permet à une classe d'utiliser les propriétés et les méthodes d'une autre classe. Cela favorise la réutilisation du code et la création de hiérarchies de classes.*

**Encapsulation :**
*L'encapsulation consiste à regrouper les données (attributs) et les méthodes qui agissent sur ces données dans une seule unité (la classe). Elle protège l'accès aux données de manière contrôlée.*

**Abstraction :**
*L'abstraction consiste à simplifier la complexité en masquant les détails inutiles et en exposant uniquement ce qui est nécessaire. Les classes abstraites et les interfaces sont des moyens de réaliser l'abstraction.*

**Interfaces :**
*Une interface définit un contrat que les classes doivent suivre. Elle spécifie les méthodes qu'une classe doit implémenter, mais ne fournit pas d'implémentation concrète*

**Polymorphisme :**
*Le polymorphisme signifie "beaucoup de formes". Il permet à une classe d'être utilisée de différentes manières. Le polymorphisme peut être statique (surcharge de méthodes) ou dynamique (redéfinition de méthodes).*
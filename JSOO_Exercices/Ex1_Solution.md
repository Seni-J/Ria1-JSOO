# Solution Exercice 1

## Solution des classes :
Voici la classe créée , avec leurs objets et leurs affichage dans console.log
### Classe Client :

````javascript
class Client{
  // Demande à ce que trois variable lui soit fournies lors de la création de l'objet
  constructor (id ,firstname, lastname){
    // Instancie les valeurs fournies
    this.id = id;
    this.firstname = firstname;
    this.lastname = lastname;
  }
  what(){
    // Retourne une chaine de caractères avec les variables précédement instanciées
    return `Nom : ${this.id} ${this.firstname} ${this.lastname}`;
  }
}

// Construit un nouvel objet
const Henry = new Client('1','Henry', 'Golepas');

// Appelle la fonction "what" dans console.log, afin d'afficher le contenu de l'objet
console.log(Henry.what());
````
#### Explications
````javascript
constructor (element1, element2){
this.element1 = variable1;
this.element2 = variable2;}
````

Vous pouvez nommez les éléments et les variables comme bon vous semble. Mais rappellez-vous de les nommez avec des noms qui parlent.

**this** rappelle à l'élément en cours d'utilisation, donc à l'objet en lui même.

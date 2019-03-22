# Solution de l'exercice 1

## Solution des classes :
Voici les classes créées , avec leur objet et leur affichage dans console.log

Les explications se trouvent dans les commentaires du code.

### Classe Category :
````javascript
class Category{
  constructor (id, name, description){
    this.id = id;
    this.name = name;
    this.description = description;
  }
  what(){
    return `Catégorie : ${this.id} ${this.name} ${this.description}`;
  }
}

const bois = new Category('1' ,'bois', 'contreplaqué');

console.log(bois.what());
````


### Classe Product :
````javascript
class Product{
  constructor (id, name, price, description, categorie_id){
    this.id = id;
    this.name = name;
    this.price = price;
    this.description = description;
  }
  what(){
    return `Produit : ${this.id} ${this.name} ${this.description} à ${this.price}.- `;
  }
}

const Baton = new Product('1', 'Baton', '20','Baton de ski');

console.log(Baton.what());
````

### Classe Order :

````javascript
class Order{
  constructor (id, created_at, shipped_at, status, client){
    this.id = id;
    this.created_at = created_at;
    this.shipped_at = shipped_at;
    this.status = status;
    this.client = client;
    }
  what(){
    return `Commande n:${this.id} commandé le : ${this.created_at}  lancé à ${this.shipped_at} status : ${this.status} pour ${this.client.firstname}`;
  }
}

// Donnez à l'objet "CommandeBaton", l'object "August" afin d'avoir toutes ses informations
const CommandeBaton = new Order('1', '19.03.2019', '00-00-00','not shipped', Henry);

console.log(CommandeBaton.what());
````

### Class OrderItem :
````javascript
class OrderItem{
  constructor (id, quantity, product, client, order){
    this.id = id;
    this.quantity = quantity;
    this.client = client;
    this.product = product;
    this.order = order;
    }
  what(){
    // Chaque appelle d'un objet, doit être suivit de ".SON-ARGUMENT" afin d'avoir la valeur de cet argument.
    return  `${this.client.firstname } à commandé ${this.quantity} ${this.product.name} de ${this.product.price} franc pour la commande n ${this.order.id} `;
  }
}
// Ici aussi, l'objet "OrderBaton" à été créé avec d'autres objets comme paramètre
const OrderBaton = new OrderItem('1', '5' ,Baton, Henry, CommandeBaton);

console.log(OrderBaton.what());
````

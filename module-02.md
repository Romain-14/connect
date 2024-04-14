# Le DOM (manipulation, événements ...) & timer

Le DOM ( Document Object Model ) est la représentation du squelette de notre fichier html sous forme de node (nœuds), : nodeElement, nodeText ..
Grace à javascript on peut interagir avec ces nœuds suite à une action de l'utilisateur et/ou une action asynchrone tel qu'un timer, une requête AJAX (fetch).

Pour la plupart des manipulations, il va falloir récupérer l'élément dont on souhaite modifier le contenu, ou si on veut lui rajouter un élément enfant

```js
const myElement = document.querySelector("value");
```
`querySelector` permets de récupérer un élément à la fois mais sa valeur (`value`) peut être de type id/class/balises

```js
const myElement = document.querySelectorAll("value");
```
`querySelectorAll` pareil que `querySelector` sauf qu'il peut récupérer plusieurs élément possédant la même `value` et les mettra dans un tableau (`Array`)
Exemple:
```html
<!-- ... -->
<button>ajouter</button>
<button>supprimer</button>
<!-- ... -->
```
```js
const buttons = document.querySelectorAll("button");
console.log(buttons); // sera un array sur lequel je pourrai itérer pour y placer des écouteurs par exemple
buttons.forEach(button => document.addEventListener("click", onClickHandler));
```

Pour récupérer il y a d'autres méthodes, une souvent utilisé avec `querySelector` est `getElementById`
```js
const myElementById = document.getElementById("btn");
```


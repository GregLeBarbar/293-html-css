# Exercice Flexbox

## Step1

Quel est mon conteneur qui va devenir Flexible ?

```css
/* Dans cet exercice le conteneur est la balise body (parent de tous les éléments) */
body {
  display: flex; /* Les éléments sont affichés les uns à côté des autres */
}
```

## Step2

Les éléments doivent se positionner en dessous si ils manquent de place

```css
/* Dans cet exercice le conteneur est la balise body (parent de tous les éléments) */
body {
  display: flex; /* Les éléments sont affichés les uns à côté des autres */

  /* Lorsque les éléments dépassent la taille de mon container (mon body) */
  /* il faut que les éléments se positionnent en dessous */
  flex-wrap: wrap;
}
```

A noter que le résultat peut surprendre. En effet comme chaque élément contient du texte, l'élément va prendre 100% de la largeur.

Pour le footer, par exemple, comme il y a très peu de texte, on peut voir un espace blanc.

Donc on n'est pas en `flex-direction: column;` mais bien en `flex-direction: row;` la valeur par défaut.

Vous pouvez tester pour voir la différence.

## Step3

Le `header` et le `footer` doivent prendre `100%` de la largeur.

```css
.header {
  flex-basis: 100%; /* Le header doit prendre 100% de la largeur*/
}

.footer {
  flex-basis: 100%; /* Le footer doit prendre 100% de la largeur*/
}
```

## Step4

Le `content` doit prendre `50%` et chaque `sidebar` doit pendre `25%`

```css
.sidebar {
  flex-basis: 25%; /* Les sidebars doivent prendre 100% de la largeur*/
}

.content {
  flex-basis: 50%; /* Le content doit prendre 100% de la largeur*/
}
```

## Step5

Si on rétrécie la fenêtre du navigateur, on s'aperçoit que la sidebar de droite se position sur la ligne en dessous.

On pourra régler se problème grâce aux Média queries dans un futur chapitre.

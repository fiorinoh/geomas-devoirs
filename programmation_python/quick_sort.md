# Quick Sort (tri rapide)

## Principe

Le quick sort est l'un des algorithme de tri les plus rapides. Voici son principe.  

Soit une liste (= tableau) d'entiers à trier. Par exemple : [1, 33, 6, 89, 5]. On enlève le dernier élément de la liste, ici 5, qu'on appelle le *pivot* et que l'on place dans une liste [5].  

Pour améliorer le fonctionnement du quick sort, le choix du pivot doit être plus précis. Mais pour notre version du quick sort, nous nous bornerons à prendre le dernier élément de la liste. On crée ensuite 2 listes vides qu'on appelle conventionnellement *agauche* et *adroite*. On a donc :

| agauche     | pivot | adroite     | liste à trier     |
| :---:      |    :----:   |    :----:   |    :----:   |
| [ ]      | [5]       | [ ]      | [1, 33, 6, 89]      |

Puis on place tous les éléments de la liste à trier plus petits ou égaux au pivot dans la liste agauche, et tous les plus grands dans la liste adroite :

| agauche     | pivot | adroite    | liste à trier     |
| :---:      |    :----:   |    :----:   |    :----:   |
| [1]      | [5]       | [33, 6, 89]      | [ ]      |

On applique (récursivement) cette procédure aux listes agauche et adroite qui deviennent les nouvelles listes à trier. Une liste vide ou singleton (ne contenant qu'un seul élément) à trier est cette même liste : le résultat du tri de [1] est [1]. Le résultat du tri de [33, 6, 89] est [6, 33, 89]. Le résultat final est la concaténation de ces tris récursifs : [1] + [5] + [6, 33, 89] soit [1, 5, 6, 33, 89].



## Exercice 1

Tester si une liste en triée :

- Ecrire un algorithme permettant de tester si une liste d'entiers est triée
- Traduisez-le en python

## Exercice 2

Ecrire l'algorithme du quicksort.


## Exercice 3

Ecrire le quick sort en python.


## Exercice 4

Comparer les performances du quick sort avec celles de la fonction sorted() de python.


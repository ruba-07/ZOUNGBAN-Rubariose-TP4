EXERCICE 1 : Un peu de théorie
Question 1 : Différence entre un graphe d’états et un arbre de recherche

Graphe d’états :
C'est un ensemble abstrait qui contient tous les états possibles du problème , plus tous les liens possibles entre eux ,
C’est une représentation conceptuelle, indépendante d’un algorithme,ce qui existe.

Arbre de recherche :
C'est une structure construite dynamiquement par un algorithme (BFS, DFS…) à partir de l’état initial, ce que l’algorithme explore réellement.

Question 2 : Un graphe fini produit-il toujours un arbre de recherche fini ?

Non, un graphe d’états fini ne garantit pas un arbre de recherche fini parce que l’arbre de recherche peut contenir des boucles :

Si le graphe contient des cycles

Si l’algorithme ne garde pas la trace des états déjà vus


Question 3 : Différence entre un état et un nœud

Un état est une configuration abstraite du problème tandis qu'un nœud est un objet de l’arbre de recherche contenant , un état , un parent , une action , une profondeur , un coût
 Plusieurs nœuds peuvent représenter le même état dans l’arbre.

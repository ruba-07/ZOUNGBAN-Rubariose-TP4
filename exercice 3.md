Question 1 — Nombre de nœuds générés (sans détection des répétitions)

Ordre correct des performances pour ce problème :


BFS : explore énormément ce qui  génère le plus de nœuds

DFS : peut tourner en boucle donc un énorme nombre de nœuds avant solution

IDS : meilleur compromis mais  explore peu de profondeur en profondeur

Donc l’ordre des performances :

- IDS = le plus efficace

- BFS

- DFS = le pire

Question 2 : Avec détection des états déjà vus

Lorsque tu stockes les états déjà visités : BFS devient le meilleur

Parce que , BFS ne revisite plus des états
DFS perd son intérêt car il explore toujours profondément même si inutile
IDS passe son temps à refaire les petites profondeurs

 Classement final :

BFS = meilleur

IDS

DFS = pire

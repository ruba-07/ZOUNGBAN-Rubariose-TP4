Question 1 — Quel algorithme est implémenté dans search ?

C’est une recherche en largeur (BFS).
Justification : 

On reconnaît BFS car :
On utilise une file (queue)
Les nœuds sont explorés par profondeur croissante , on trouve la solution la plus courte


Question 2 : Complexité spatiale pour 5×5 et 6×6

Un cavalier a en moyenne 8 mouvements, mais sur les bords beaucoup moins.
BFS doit stocker tous les nœuds de la frontière, jusqu’à couvrir toutes les positions possibles du tour.
Nombre d’états pour le tour du cavalier

5×5 → 25 cases

6×6 → 36 cases

Mais dans le problème du tour, un état n’est pas “la case actuelle”, mais : (position + cases déjà visitées)


Pour BFS, l’espace ≈ branching factor^profondeur

Pour un tour de n cases → profondeur = n.

5×5 : profondeur = 25

6×6 : profondeur = 36

Donc mémoire ≈ 8^25 vs 8^36, ce qui est astronomique.

La complexité spatiale est exponentielle et passe d’un problème difficile à un problème impossible à stocker en mémoire dès 6×6.

Question 3 :Implémenter DFS:

Stack<Node> frontier = new Stack<>();
frontier.push(root);

while (!frontier.isEmpty()) {
    Node n = frontier.pop();
    if (goal(n)) return n;
    frontier.push(successors(n));
}




Question 4 : Implémenter l’Iterated Deepening DFS :

for (int limit = 1; ; limit++) {
    Node result = DFS_Limited(root, limit);
    if (result != null) return result;
}

 Pertinence pour le tour du cavalier :



Question 5 — Peut-on résoudre 6×6 ou plus 
Réponse attendue :


# REFLEXION.md : réponses

1. `robots.txt` empêche-t-il, à lui seul, le duplicate content entre
   `/produits?tri=prix` et `/produits?tri=prix-asc` ? Pourquoi ?

   Non. `robots.txt` contrôle l'exploration, mais une URL bloquée peut tout de
   même être indexée si elle est découverte par des liens externes. Il ne
   signale pas aux moteurs quelle URL est la version de référence.

2. Pourquoi la balise canonique est-elle l'outil adapté ici, plutôt que
   `robots.txt` ou une meta `noindex` ?

   Les deux URL affichent le même contenu ; la balise canonique indique aux
   moteurs de recherche quelle URL privilégier pour l'indexation et regroupe
   les signaux associés à cette version. `robots.txt` bloque l'exploration et
   `noindex` exclurait la page de l'index au lieu de désigner une version de
   référence.

3. Si demain `/admin` existe sur ce site et ne doit jamais être exploré par
   Google, quelle ligne ajoutes-tu dans `robots.txt` ?

   `Disallow: /admin`

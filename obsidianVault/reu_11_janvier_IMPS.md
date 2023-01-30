#PLN 

- utiliser L-BFGS pour la montée de gradient 
- Attention au self-normalized assez ambigu ?
- Bien réecrire la variance de delta chapeau 
- vérifier le Omega-1 = L’identité 
- écrire sur le ker(C), développer sur l’asymptotique 
- Changer le nom de matrice A dans la prop sur la borne des poids 
- Etre plus clair sur le petit o
- lancer l’algo une centaine de fois, garder(sauver) les courbes et arreter quand l’écart a la médiane est en dessous d’un seuil.

Remarques: 
- L-BFGS assez galère à implémenter, mais prq pas 
- Le self-normalized est plus malgré lui qu'autre chose. A cause de la formule du gradient. 
- Tromper pour Omega. 
- besoin d'écrire sur le ker(C) ? La preuve est assez clair ? 
- un peu délicat le petit o(). Comment dire qu'il tend vers 0 quand on prend l'espérance. 
- lancé l'algo une centaine de fois, résultats satisfaisant. 
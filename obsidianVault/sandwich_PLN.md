#PLN
- Essayer deja de retrouver la matrice de Fisher avec l'[[IMPSPLN]]
- Relire McCornick et checker si on a bien les conditions suffisantes avec les simu. 
- Donner la M estimation dans l’abstract. t
- Cleaner le code et tout faire pour ma version pytorch 

- 4.1 profiled objective function. How can we say it is unique ? convexity does not yield uniqueness. Strict convexity does. 
- assumption A1: pas clair entre les et et les ou. Pour moi si on munit l’espace de la distance arctan, alors on a les bonnes prop pour beta et Sigma 
- regarder si c’est vrmt consistant. regarder la normalité par rapport a theta bar et pas theta*, en prenant n très grand et en rajoutant a chaque itération un n 
- Pourquoi on doit inverser n^2 matrices ? pas plutot n ? 
- essayer avec l’importance sampling. avec les deux formules de l’espérance ? 
- regarder a quoi ressemble la sortie de theta: est ce gaussien ? 
- relire mcCornick et vérifier les hypothèses demandées 
- si on prend s comme paramêtre et S^2 en variance, alors la fonction n’est plus concave, mais concave sur 2^np demi espace, ou chaque variable est restreinte a un demi espace (>0 ou <0) 
- Problème sur la dérivée seconde de l’elbo par rapport a M, interversion entre I_n et Omega dans le produit de Kronecker. 
- essayer de faire les test naif sur les 2 formules et regarder si l’espérance vaut bien ce que ca doit valoir mm quand on prend les 2 esp (pour la formule de l’information de Fisher)


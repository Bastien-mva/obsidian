- Changer le delta_n et delta_d en nu et rho et faire apparaitre la dépendance en n_s au dessus je pense. 
- Lancer l'algo 100 fois mais aussi changer le nombre d'itérations que l'on prend, et le faire pour l'ESS. 
- Prendre les échantillons précédents ? 
- faire du miniBatch. 
- On peut estimer la KL ? avec de l'IMPS peut etre ? 
- Regarder des papiers sur l'estimation de ratio : Monte Carlo gradient estimation in machine learning. 
- Diagnostic des poids: 
								- Grandeur du bais
								- variance des poids 
								- ESS 
- Rajouter des particules au lieu d'en simuler des nouvelles pour estimer si le biais tends vers zéro 
- Regarder la littérature sur le gradient estimé par du Monte Carlo
[[compte_rendu_imps_2fev2023]]
-  le self-normalized est a part entiere, c'est vraiment ca. Ducoup le biais tend vers 0 avec ca. 
- Faire un algo de descente de gradient juste avec $p_{\theta}$
- Checker Andrieu et Dousset en 2010. 
-   A dire: le bais est en $o(\frac 1 {n})$ alors que la précision est en $o (\frac 1 {\sqrt n })$ donc le biais est négligeable.  
- faire des simu pour l'ESS et la variance des poids vec 150 trials
[[reu_21_fev_Julien_Julien_IHP]]

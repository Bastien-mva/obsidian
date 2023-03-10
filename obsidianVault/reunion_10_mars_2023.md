Mini CR:
 regarder la balanced accuracy au lieu de l'accuracy
 pourquoi on a une accuracy a 0 ? 
 faire converger L au meme moment pour adaptatif vs accel $$\implies $$ mettre lr = 1000/L au lieu de 1/L pour les algo adaptatifs. 
 SAGAdam, SAGAdaDiag, SAGARMSprop etc... VS SAGA
  afficher le nombre d'epoch eu lieu du nombre de gradiens
lancer sur d'autres jeux de données (les mêmes grossièrement, peut etre load_svm_light de sklearn
 plus grosses dimensions pour scRNA. 
 pour imps
borne standard a 95% pour la log likelihood. 
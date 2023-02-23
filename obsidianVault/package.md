- Faire des channels etc avec python (checker sur internet) 
- faire un readthedocs (Julien) 
- test with pytest
- faire un extract gaussian layer qui renvoie la couche latente gaussienne pr faire du ML. 
- Il faudrait aussi faire du clustering ... comment ca se passe si on a plusieurs clusters ? 
 - implémenter qqch tel qu'on puisse faire plusieurs q en meme temps. 
- refaire le README.md. Voir JB
- MANIP A FAIRE pour installer le package : 
	- pip install -e pour l'installer en local. 
	- python setup.py bdist_wheel  sdist
	- check-manifest --create
	- ensuite: 
	-  twine upload --skip-existing dist/* (juste twine upload dist/* si il n’a pas été crée jse crois)
 - checker si on peut casser l'API en modifiant des trucs qu'on a moralement le droit de modifier. En gros mettre des  blanc beta et blanc C devant tout.  
 - definir des setters pour Y O et covariates
## Conseil de JB 
- apprendre comment faire un peu mieux le .yml de gitlab-ci 
- checker le license de parametrization cookbook, ainsi que le setup
- faire la doc sur github 
- papier scientifique donc docstring au format numpydoc 
- faire les test unitaires 
- la doc de matplotlib est top 
- mettre en kwargs les parametres non importants 
- print (aka __repr__) devrait return un string !
- Token rattaché au projet 
- Ne pas mettre le mot de passe 
- MDP pr générer le token sur pypi et après stop 
- Test coverage pour savoir quelles lignes sont pas testés 
- Checker la CI de JB pr les tests 
- Un bug-> un test 
- Moi qui raise l'error quand n différent de n tilde 
- Type error 
- Ne jamais lever Exception tout court 
- Google python style guide 
- Pylint Avec pylintrc 
- Fstring au lieu de format 
- Formater avec f'{b:18s
- Formatage pr value error : !r
- Si un blanc l'utilisateur ne peut pas l'utiliser
- Si il doit pvr le modifier mettre un setter avec des setter

[[question_package_JB]]

[[docstring_a_faire]]
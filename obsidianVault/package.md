- Faire des channels etc avec python (checker sur internet) 
- faire un readthedocs (Julien) 
- test with pytest
- faire un extract gaussian layer qui renvoie la couche latente gaussienne pr faire du ML. 
- Il faudrait aussi faire du clustering ... comment ca se passe si on a plusieurs clusters ? 
- MANIP A FAIRE pour installer le package : 
	- pip install -e pour l'installer en local. 
	- python setup.py bdist_wheel  sdist
	- check-manifest --create
	- ensuite: 
	-  twine upload --skip-existing dist/* (juste twine upload dist/* si il n’a pas été crée jse crois)
## Conseil de JB 
- checker le license de parametrization cookbook, ainsi que le setup 
- license=”MIT”, c’est tout 
- classifiers tout mettre sauf le dernier (dans le parametrization cookbook) 
- mettre les project url 
- faire la doc sur github 
- regarder sphinx pour (generer) la doc
- papier scientifique donc docstring au format numpydoc 
- faire project url au lieu de url et en mettre plusieurs (source) 
- faire les test unitaires 
-  developper avec pip install -e 
- clean un peu l’history qui est trop grosse
- la doc de matplotlib est top 
- mettre en kwargs les parametres non importants 
- print (aka __repr__) devrait return un string !

[[question_package_JB]]

[[docstring_a_faire]]
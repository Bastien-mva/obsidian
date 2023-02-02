give searchable [[clean_variable_names]] 
Une [[clean_functions]] devrait faire qu'une seule chose. Un level d'abstraction. On code bien la fonction plus tard, pas direct
 
[[clean_comments]]
 

## Code formatting 
- closed concepts should be close vertically 
- Variable should bé déclaréd as close go their usage 
- Scissor rule: instance variables should be declared at the top of the class
- Pas plus de 100 ou 120 charzctères par ligne
- Mettre des espaces entre les opérateurs = etc 
- Mettre des espaces entre les + et - mais pas les × par ex  
- Les espaces créent de la distance dans le fichier et a la fois dans le concept: deux concepts éloignés doivent qui se suivent doivent être séparés par une ligne 
- if one function calls another, they should be vertically close 
- the caller should be above the calle, this gives a natural flow 
- function that are similar should be close, like share common naming schem or performs similar things
## indentation
- Classes are not indented. methods inside classes are indented of one block. blocks inside methods are indented one block ahead, and so on. 
- respect number of indentation 
## Objects and data structures
- avoid creating a classes that are both data structures and objects 
## error handling
- Ne pas retourner NULL, throw exception instead
## Unit tests 
- Écrire des Unit tests CLEAN ! 
- The dirtier thé tests, thé dirtier thé production code
- BUILD OPERATE CHECK pattern. 
- BUILD thé data, OPERATE and then check if it is right 
- Domaine specific testing language (learn)
- Single assert for a Unit test is a good guideline
- Single concept per test 
- FIRST  method 
- Fast 
	- Indépendant 
	- Réparable 
	- Self-validating 
	- Timely
## CLASSES 
- First: list of variables, public static constants, private static variables, private instance variables, public functions, private utilities 
- Smaller is the primary rule 
- SRP: single responsability principle
- If top ouch variable: Split the class 
## Systèmes
- The main should not implement functions 
## émergence 
- Design rules: 
- Runs all thé tests
- Contains no duplication 
- Expresses the intent of thé programmer 
- Minimizes thé number of classes and methods
- Clean a little bit and then run the tests. 
- Au moment où on tape le code on comprend tout tout, prendre un peu de recul 
- La prochaine personne qui lira le code, c'est toi 
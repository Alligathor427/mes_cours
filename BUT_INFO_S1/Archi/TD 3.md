1-représentation 
Code de gray (ou code réflechis): 
fonctionement --> code permettant de modifier un bit a la foiq quand un nombre est modifier en binaire 
méthode --> pour passer a la ligne suivante on inverse le bit le plus a droite possible 
on a a chaque etap une symetrie qui ce crée au niveaux des bit en commençant par les  0 suivis des 1  
exemple : sur 2 bit 
0 0
0 1
-->axe de symétrie 
1 0
1 1 
 et on continue de suite pour chaque passe de octet 
**2-opération arithmétique 
2-1: Addition

L'addition binaire s'effectue **bit par bit** de droite à gauche (du poids faible au poids fort), en respectant les règles de la base 2.

Les règles fondamentales sont :

- **0 + 0 = 0**
    
- **0 + 1 = 1**
    
- **1 + 0 = 1**
    
- **1 + 1 = 10** (on inscrit **0** et on reporte **1** de retenue)
    
- **1 + 1 + 1 = 11** (on inscrit **1** et on reporte **1** de retenue)

**2-2:Soustraction 
### 1. Méthode par emprunt (Standard)

Cette méthode reproduit la soustraction posée en décimal, colonne par colonne, de droite à gauche.

- **Règles de base** :
    
    - 0−0=0
        
    - 1−0=1
        
    - 1−1=0
        
    - 0−1=1 (avec emprunt de 1 au bit de poids supérieur).

**2-3: multiplication  

La multiplication binaire suit le même principe algorithmique que la multiplication décimale posée, mais repose sur une table de vérité simplifiée où **1×1=1** et toute autre combinaison donne **0**. Pour effectuer le calcul, on multiplie le multiplicande par chaque bit du multiplicateur : si le bit est **1**, on recopie le multiplicande ; s'il est **0**, on écrit une ligne de zéros.

Chaque résultat partiel obtenu est ensuite **décalé vers la gauche** d'un cran supplémentaire par rapport au précédent (équivalent à multiplier par une puissance de 2). Enfin, on additionne tous ces produits partiels en utilisant les règles de l'**addition binaire** (où 1+1=10, générant une retenue).

- **Règles de base** : 0×0=0, 0×1=0, 1×0=0, 1×1=1.
    
- **Décalage** : Un décalage à gauche équivaut à une multiplication par 2.
    
- **Taille du résultat** : Le produit de deux nombres de M et N bits nécessite au maximum M+N bits.




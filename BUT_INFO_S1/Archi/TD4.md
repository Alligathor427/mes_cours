1. a) quelle est la plage des nombres représentables sur 7 bits ? 
	-le complément a 2 est un ereprésentation qui utilise 1 bit de signe et 6 bits pour codée le chiffre 
	-ainsi pour n nombre de bits k on peut codée 2**k-1 chifffre , donc avec 7 on a :
	-2⁶ <=N<=+2⁶-1
2. pour la représentation des chiffres negatifs ( quand le premier bit est a 1 ) a complétée ( j'ai rien compris ) :
	première etape regardée le bit e signe (le premier )
	0 => positifs 
	1 => negatifs 
	ensuite on determine la valeur absolue du nombre 
		si le nombre est positifs ou nul convertire la sequence binaire en base 10 
	ou si 
		le nombre est negatifs on calcule le complément a deux de la séqueence 
		et enfin le convertire en base 10 
exercices 
1-2 :
Séquence => <font color="#c00000">1</font>0110101 
le premier bit est 1 donc le chifre est negatifs 

le complément a 2 : on fait dabord le complément a 1 (tout les 0 deviéne de 1 et vis versa )

<font color="#c00000">1</font>0110101  => 01001010  

et on rajoute un 1 a la fin 

<font color="#c00000">1</font>0110101  => 01001010  => 01001011 

ce qui est eguale a  : 2⁰ + 2¹ +2³ + 2⁶ = 1+2+8+64+= 75  

Séquence => <font color="#c00000">1</font>1101001 

le premier bit est 1 donc le chifre est negatifs  
le complément a 2 : on fait dabord le complément a 1 (tout les 0 deviéne de 1 et vis versa )et on rajoute un 1 a la fin  
 <font color="#c00000">1</font>1101001  => 00010110 => 00010111 






- ``$IFS`` : C’est une variable spéciale de Bash qui indique à Bash comment découper une chaîne en champs ou mots lorsqu’il doit transformer une chaîne en plusieurs éléments.

- ``$#``  Cette variable contient le nombre d’arguments passés au script.

- ``$@``  Cette variable permet de récupérer la liste complète des arguments passés en ligne de commande.

- ``$n``  
Chaque argument peut être récupéré individuellement selon sa position. Par exemple, le premier argument se trouve dans `$1`.

- ``$$``  L’ID du processus (PID) du script en cours d’exécution.

- ``$?``  Le code de sortie du dernier script ou commande exécuté(e).  
    - `0` signifie que l’exécution a réussi.  
    - `1` (ou autre valeur différente de 0) signifie que l’exécution a échoué.

# String Comparaison Operateurs
- ``==``      est égal à  
- ``!=``      n'est pas égal à  
- ``<``       est inférieur selon l'ordre alphabétique ASCII  
- ``>``       est supérieur selon l'ordre alphabétique ASCII  
- ``z``      si la chaîne est vide (nulle)  
- ``n``      si la chaîne n'est pas nulle  

# Integer Comparaison Operateurs
- ``eq``     est égal à  
- ``ne``     n'est pas égal à  
- ``lt``     est inférieur à  
- ``le``     est inférieur ou égal à  
- ``gt``     est supérieur à  
- ``ge``     est supérieur ou égal à  

# File Comparaison Operateur
- ``e``     si le fichier existe  
- ``f``     teste si c'est un fichier  
- ``d``     teste si c'est un répertoire  
- ``L``    teste si c'est un lien symbolique  
- ``N``     vérifie si le fichier a été modifié après sa dernière lecture  
- ``O``     si l'utilisateur courant est le propriétaire du fichier  
- ``G``     si l'identifiant du groupe du fichier correspond à celui de l'utilisateur courant  
- ``s``     teste si le fichier a une taille supérieure à 0  
- ``r``     teste si le fichier a la permission de lecture  
- ``w``     teste si le fichier a la permission d'écriture  
- ``x``     teste si le fichier a la permission d'exécution  

# Logical Operateur
- ``!``      négation logique (NOT)  
- ``&&``     ET logique (AND)  
- ``||``     OU logique (OR)  

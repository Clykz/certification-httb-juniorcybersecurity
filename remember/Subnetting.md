- Le subnetting consiste à diviser un grand réseau IP en plusieurs plus petits sous-réseaux.
- Le masque de sous-réseau détermine où s’arrête la partie réseau et où commence la partie hôte dans une adresse IP.
- Une adresse IPv4 : 32 bits (4 octets), divisée en deux parties : uune partie reseau et une partie hote
```
10.200.20.1/27
Partie réseau (27bits): 10.200.20
Partie hote (32 - 27 bits): .1
````


- Exemple pour créer 4 sous réseaux : 
```
#addresse de base donc en 32 bits  en /27 
10.200.20.0/27

27 bits de reseau
5 bits hotes

#Nombre addresse possible
2^5 = 32

#Vue qu'on veut creer 4 sous reseaux on doit emprunter 2 bits (tout les 2 sous réseaux on emprunte 1 bit)

3 bits hotes apres 4 sous réseaux

#Update nombre addresse possible

devient un /29
donc 29 bits de réseaux
2^3 = 8
donc 6 addresse utilisables

10.200.20.0
10.200.20.8
10.200.20.16
10.200.20.24
```
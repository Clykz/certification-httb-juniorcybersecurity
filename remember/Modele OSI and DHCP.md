# Réseaux
- Modèle OSI (Open Systems Interconnection) est un modèle en 7 couches qui décrit comment les données circulent entre deux systèmes informatiques sur un réseau. Astuce mnémotechnique pour les 7 couches (du plus bas au plus haut) :
```
Please Do Not Throw Sausage Pizza Away

Physique, Liaison de données, Réseau, Transport, Session, Présentation, Application
```
![alt text](image/image.png)

# DHCP
- DORA

![alt text](image/image-1.png)

# NAT (Network Address Translation)

## Qu’est-ce que la NAT ?

La **NAT (Traduction d’Adresse Réseau)** est un mécanisme utilisé sur les routeurs pour **modifier l’adresse IP d’origine d’un paquet** qui traverse le routeur.  

- Traduit les **adresses privées** d’un réseau local (LAN) en **adresses publiques** pour accéder à Internet.  
- Fonctionne sur la **couche 3 (réseau) du modèle OSI**.

## À quoi ça sert ?

1. **Partager une seule IP publique pour plusieurs appareils**  
   - Exemple : PC, smartphone et tablette utilisent la même IP publique pour Internet.  

2. **Protéger le réseau interne**  
   - Les adresses privées (ex : 192.168.x.x) ne sont pas visibles depuis Internet.  

3. **Économiser les adresses IPv4**  
   - Plusieurs machines partagent une seule IP publique au lieu d’avoir une IP publique par appareil.

## Types de NAT

| Type              | Fonction                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Static NAT**    | Une IP privée → une IP publique fixe                                     |
| **Dynamic NAT**   | Une IP privée → une IP publique choisie dans un pool d’adresses         |
| **PAT / NAT overload** | Plusieurs IP privées → une seule IP publique (traduction avec ports) |

> Le type le plus courant pour les particuliers : **PAT**, car il permet à tous les appareils de partager une seule IP publique.
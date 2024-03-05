# Commandes Linux Utiles

## HashID

Permet d'identifier la probable fonction de hashage a généré une chaîne de caractère.

Télécharger HashID

`wget https://gitlab.com/kalilinux/packages/hash-identifier/-/raw/kali/master/hash-id.py`

Le lancer

`python3 hash-id.py`

Il suffit ensuite de saisir un hash pour identifier les possibles fonctions de hash.

## Nikto

Nikto est un scanner de vulnérabilités

`nikto -h https://www.example.com`

## Premier plan / Arrière plan

Lorsque je suis dans un programme en ligne de commande, je peux faire `ctrl + z` pour le mettre en arrière plan. 
Avec la commande `bg`, j'ai la liste des processus en arrière plan.
Avec la commande `fg`, je le remets au premier plan.

## TR

Mettre tout le contenu d'un fichier en majuscule.

`cat fichier.txt | tr -s '[a-z]' '[A-Z]'`

ou

`cat fichier.txt | tr -s '[:lower:]' '[:upper:]'`

Supprimer des caractères (pour n’avoir que des chiffres par exemple)

`cat fichier.txt | tr -d '[a-zA-Z: ]'`

## Installation de SecLists

Pour obtenir, nottament, les wordlists

`git clone https://github.com/danielmiessler/SecLists.git`

## Tree

Pour afficher l'arborescence sous forme d'arbre

`tree`

## Locate

Pour chercher des fichiers

`locate <pattern>`

## Pkill

Killer un processus sans spécifier son ID

`pkill -f <nom du process>`

## Htop

Top en plus joli ^^

`htop`

## SS

Afficher les sockets ouverts

`ss -tulpn`

## Netstat

Afficher les connexions / ports ouverts

`netstat -tulpn`

## ARP

Afficher le cache ARP

`arp -a`

On peut également l'afficher ainsi

`cat /proc/net/arp`

Vider le cache pour une adresse précise

`arp -d <adresse>`

Vider le cache intégralement

`for e in $(arp -a | sed -n 's/.*(\([^()]*\)).*/\1/p'); do arp -d $e; done`

## Pbcopy

Pour copier le résultat d'une commande dans le presse papier.

Exemple avec la commande `ls`

`ls | pbcopy`
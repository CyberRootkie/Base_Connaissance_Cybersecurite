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
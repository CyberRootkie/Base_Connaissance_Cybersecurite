# Gobuster

Gobuster est un outil de brute-force permettant de découvrir des URLs, des répertoires, des entrées DNS, ...


## Recherche de répertoires

`gobuster dir -u https://www.example.com -w wordlist.txt`

## Recherche de fichiers en précisant l'extension

`gobuster dir -u https://www.example.com -w wordlist.txt -x .php,.html`

## Recherche d'entrées DNS

`gobuster dns -d example.com -w wordlist.txt`


## Définir le nombre de threads (10 par défaut)

`gobuster dir -u https://www.example.com -w wordlist.txt -t 50`
# Nmap

Nmap est un scanner de ports très populaire.

## Sélection des cibles

- Scanner une IP précise : `nmap 192.168.0.1`
- Scanner un réseau : `nmap 192.168.0.0/24`
- Scanner plusieurs cibles : `nmap 192.168.0.1 192.168.0.2`
- Lister les cibles (sans les scanner) : `nmap -sL 192.168.0.0/24`

## Sélection des ports à scanner

> [!WARNING]
> Par défaut, Nmap ne va scanner que les 1000 premiers ports.

- Scanner uniquement un port (le 80) : `nmap -p80 192.168.0.1` 
- Scanner un range de port (1 à 100) : `nmap -p1-100 192.168.0.1`
- Scanner tous les ports (les 65 536) : `nmap -p- 192.168.0.1`

## Modes de scan

- Scanner en UDP (plus rapide) : `nmap -sU 192.168.0.1`
- Scanner en TCP avec le flag SYN uniquement (plus rapide mais plus suspect) : `nmap -sS 192.168.0.1`
- Scanner en TCP avec un flag FIN (permet d'identifier les ports ouverts même s'ils ne répondent pas) : `nmap -sF 192.168.0.1`
- Ping sans scan de ports : `nmap -sn 192.168.0.1`
- Tente d'identifier la version des services : `nmap -sV 192.168.0.1`

## Ajouter de la verbosity

- Verbose mode : `nmap -v 192.168.0.1`
- Encore plus de verbosity : `nmap -vv 192.168.0.1`
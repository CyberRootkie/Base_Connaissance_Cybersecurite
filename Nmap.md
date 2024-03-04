# Nmap

Nmap est un scanner de ports très populaire.

## Sélection des ports à scanner

> [!WARNING]
> Par défaut, Nmap ne va scanner que les 1000 premiers ports.

- Scanner uniquement un port (le 80) : `nmap -p80` 
- Scanner un range de port (1 à 100) : `nmap -p1-100`
- Scanner tous les ports (les 65 536) : `nmap -p-`
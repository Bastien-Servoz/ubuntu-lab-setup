# Configuration d'un laboratoire Linux sous VirtualBox

## 🎯 Objectif
Ce projet documente la mise en place d'un environnement de lab virtualisé sous Ubuntu, dans le cadre d'un parcours d'auto-formation en réseau et cybersécurité (objectif : certifications Linux Essentials, CCNA, Security+).

## 🛠️ Technologies utilisées
- **VirtualBox** (Oracle) — logiciel de virtualisation
- **Ubuntu 26.04 LTS** (amd64) — système d'exploitation invité
- **Terminal Linux** — ligne de commande (bash)

## 📋 Étapes réalisées
1. Installation de VirtualBox sur Windows
2. Téléchargement de l'image ISO Ubuntu 26.04 LTS
3. Création d'une machine virtuelle (4 Go RAM, 2 CPU, 40 Go disque)
4. Installation du système Ubuntu (mode automatisé)
5. Installation des VirtualBox Guest Additions (amélioration des performances graphiques et de l'intégration souris/clavier)

## 🐛 Problèmes rencontrés et solutions

| Problème | Cause | Solution |
|---|---|---|
| Fichier ISO bloqué au téléchargement | Smart App Control de Windows | Débocage manuel via les propriétés du fichier |
| VM bloquée au démarrage | Virtualisation matérielle (VT-x) à vérifier | Redémarrage / vérification BIOS |
| `bzip2 not found` lors de l'installation des Guest Additions | Paquet manquant sur Ubuntu fraîchement installé | `sudo apt install bzip2` |
| `make: not found` lors de la compilation des modules | Outils de compilation absents | `sudo apt install build-essential dkms linux-headers-$(uname -r)` |
| Redémarrage refusé (`user session inhibited`) | Protection système active | `sudo systemctl reboot -i` |

## 💡 Compétences développées
- Virtualisation et gestion de machines virtuelles
- Utilisation du terminal Linux et des commandes de base (`ls`, `sudo`, `apt`)
- Diagnostic et résolution d'erreurs système
- Gestion de paquets sous Ubuntu (APT)

## 📌 Prochaines étapes
- Premières commandes Linux avancées (navigation, permissions, fichiers)
- Configuration réseau de la VM

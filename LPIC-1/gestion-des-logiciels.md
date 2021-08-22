# Gestion des logiciels

## Concept
Archive composé de fichiers ou d'informations assurant la cohérence du système.
- exécutable ou sources
- configuration
- documentation
- scripts (pré/prost - installation et désinstallation)
- dépendances

### Différents types
- Debian: deb
- Redhat: rpm - Redhat Package Manager
- Arch: pacman (tar.gz, bz2 ou xz)
- Slackware: pkgtool (tgz ou xz)
- Gentoo (cas particulier): portage (scripts ebuilds + sources)
- Puppy: pet
- etc ...

### Dépôts
Permet de mettre à disposition une liste des packet, évite d'avoir à chetcher soit même un paquet:
- à jour
- validés
- on-line (ou via une dépôt local, cd, dossier, etc...)

### Outils
Gestionnaires de paquets
- dpkg
- rpm

Gestionnaires de téléchargement et résolution de dépendances
- yum: Red Hat
- apt: Debian & Ubuntu
- urpmi: Mandriva
- zypp: Suse

|                               | deb   | rpm   |
| ----------------------------- | ----- | ----- |
| signature des paquets         | non   | oui   |
| recommandations, suggestions  | oui   | non   |
| programme de vérification     | non   | oui   |
| priorités                     | oui   | non   |

- avantages de rpm: utilisé par la Linux Standard Base
- avantage de deb: meilleur adaptabilité
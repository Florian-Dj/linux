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


## Yum
Gestionnaires de téléchargement et résolution de dépendances pour les distributions Red Hat (Fedora, CentOs, RHEL, etc...)

### Mise à jour
```
yum update yum              # en cas de premier lancement
yum update                  # mise à jour
yum check-update            # vérifier les mises à jour disponibles
yum localupdate package.rpm # à partir d'un fichier local
yum upgrade                 # mise à jour vers une version ultérieur de la distribution
```

### Informations
```
yum info package                # équivalent à rpm -qi
yum list package                # version installée et disponibilité de mises à jour
yum provides function/file      # afficher la liste des paquets fournissant une fonctionnalité ou un fichier
yum install package             # installer un package
yum localinstall package.rpm    # installer un package depuis un fichier rpm
yum remove package              # déinstalle un package
yum erase package               # déinstalle un package
yum search package              # voir les différents package*
yum clean*
```

Nettoyer le cache
- permet de libérer de l'espace disque en supprimant les rpm téléchargés
- options: headers, packages, metadata, dbcache, plugins, expire-cache, rpmdb, all
```
yum clean option
yum shell       # permet de lancer des commandes l'une à la suite des autres
```

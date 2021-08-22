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
```

```
yum shell       # permet de lancer des commandes l'une à la suite des autres
```


## Configuration Yum

### Options de base
- Configuration par défault:
    - habituellement suffisante
- Modifer les options de base

- Ajouter des dépôts:
    - non officiels
    - plus adaptés à votre usage
    - offrant des programmes spécifiques
    - personnel

Fichier de configuration de yum '/etc/yum.conf'
```
debuglevel=2            # configurer le niveau de verbosité (entre 0 et 10)
exclude=package_name    # exlure des packages de l'installation et de la mise à jour
gpgcheck=0              # activer/désactiver la vérificationn des signatures GPG (0 ou 1)
retries=0               # nombre d'essais avant de retourner une erreur (0 ou plus)
installonly_limit=value # nombre maximum de version différentes d'un paquets installés (attention nombre de Kernel !)
exactarch=1             # prendre en compte le type d'architecture lors des màj (0 ou 1)
```

### Gestion des priorités
```
yum install yum-priorities  # permet d'activer les priorities
```
Dans le fichier : /etc/yum/pluginconf.d/priorities.conf
```
[main]
enabled=1   # vérifier que la valeur = 1
```
Puis pour chaque dépot ajouster la priorities
```
priority=value  # valeur entre 0 et x (0 autant le plus haut)
```

### Ajout de dépôt via rpm
```
wget http://link.com/depot.rpm              # télécharger le paquet
rpm --import http://link.com/key.dag.txt    # importer la clé GPG
rpm -K file.rpm                             # vérifier le checksum du paquet
rpm -i file.rpm                             # installer le paquet
yum check-update                            # tout mettre à jour
```
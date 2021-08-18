# LPIC-1
Documentation pour le certificat LPIC-1


## Première commandes

### Help et Man
--help ou man pour avoir les infos sur une commande
```
man man  # Manuel du manuel
man cd  # Manuel de la commande cd
info cd  # Plus complet que le man
cd --help  # Help pour la commande cd
```

### Commande de base
```
cd  # Permet de 'naviguer' dans les dossier
ls  # Liste les fichiers et dossier dans le chemin ou nous sommes
whereis man  # Savoir se situe le chemin d'accès de man
echo  # Afficher un message
exit  # Quitter l'utilisateur en cours et sortir du bash
history  # Voir l'historique
cp path/file path/file  # Copier coller d'un fichier d'un chemin vers un autre
cp -R path/folder path/folder  # Copier coller d'un dossier complet
mv path/file path/file  # Renommer et/ou déplacer un fichier
rm path/file  # Supprier un fichier
touch file  # Création d'un fichier
mkdir folder  # Création d'un dossier
rmdir folder  # Supprimer un dossier vide
ln -s fichier1 fichier2  # Lien symbolique entre deux fichier
```

### Commande chemin
```
cd /home/admin/  # Chemin absolu
cd admin/  # Chemin relatif
```
| Signe | Note                                      |
| :---: | :---------------------------------------: |
| ~     | répertoire personnel                      |
| .     | répertoire courant                        |
| ..    | répertoire parent du répertoire courant   |
| -     | dernier répertoire avant changement       |

PWD permet de savoir ou nous nous trouvons à l'heure actuel
```
pwd  # Savoir le chemin ou nous nous trouvons
```
Pour plus d'infos: **pwd --help**

### Raccoucis clavier
- Ctrl + R: faire un recherche de commande
- Ctrl + G: quitter la recherche
- Ctrl + A: debut de ligne
- Ctrl + E: fin de commande
- Ctrl + K: supprime depuis le curseur à la fin de lacommande
- Ctrl + X puis Backspace: surpprime debut jusqu'au cuseur
- Ctrl + T: inverse deux caratères, curseur et celui d'avant
- Esc puis T: inverse deux mots, curseur et précéde
- Esc puis U: change la case du mot (min -> màj)
- Esc puis L: change la case du mot (màj -> min)
- Esc puis c: change la case d'une lettre
- Ctrl + L: nettoie la console


## Globbing
- ?: n'importe quel caractère
- *: n'importe quelle chaine de caractère
- [..]: l'un des caractères entres les crochets
- [a-f]: n'importe quel caractères entre "a" et "f"


## Flux
- entrée standard (stdin)
- sortie standard (stdout)
- erreur standard (stderr)


## Redirections
| Signe | Note                                              |
| :---- | ------------------------------------------------- |
| >     | stdout vers un nouveau fichier                    |
| >>    | stdout à la suite d'un fichier                    |
| 2>    | stderr vers nouveau fichier                       |
| 2>>   | stderr à la suite d'un fichier                    |
| &>    | stdout + stderr                                   |
| <     | stdin depuis un fichier                           |
| <<    | stdin à partir d'une chaine de cractères          |
| <>    | stdin et stdout vers et depuis le même fichier    |


## Autres
```
mount  # Permet de monter un disque sur la machine
```
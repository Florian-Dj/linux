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

## Autres
```
mount  # Permet de monter un disque sur la machine
```
# Edition de fichiers

## Outils
- Graphiques:
    - gedit sous Gnome
    - kate ou kedit sous KDE
    - mousepad sous Xfce
    - leafpad sous LXDE
- Spécialisés:
    - jEdit
    - Bleufish
    - etc ...
- CLI:
    - vim
    - nano
    - emacs

### Vim
Référence pour LPIC. Amélioration de vim crée par Bill Jou en 1976, présent sur tout les systèmes Unis, modal mais non libre

### Emacs
Développé par James Gosling en 1981, puisant extensible et personnalisable.

### Nano
Clone livre de Pico, simple, efficace et minimal, écrit par Chris Allegratte en 1999. Contrôle par modificateurs (touche Ctrl)


## Vim
### Les modes
| Touche    | Mode      | Usage                             |
| --------- | --------- | --------------------------------- |
| Esc       | normal    | accéder à tout les autres modes   |
| i         | insertion | ajouter du texte                  |
| :         | commande  | entrer des commandes              |
| v         | visuel    | selectionner et actions           |
| q         | Ex        | idem que poru le mode commande    |

### Commandes utiles
| Commandes | Usage                         |
| --------- | ----------------------------- |
| A         | ajouter en fin de ligne       |     
| u         | annuler la dernière opération |
| ctrl+r    | rétablir (redo)               |
| yy        | copier la ligne               |
| dd        | supprimer la ligne (couper)   |
| p         | coller                        |
| x         | effacer le caractère          |
| dw        | effacer jusqu'à la fin du mot |
| diw       | effacer le mot sous le curseur|
| q         | quitter sans sauvegarder      |
| q!        | quitter de force              |
| w         | écrire (sauvegarder)          |
| wq ou x   | quitter et sauvegarder        |

Tutorial intégré en ligne de commande
```
vimtutor  # Tutorial pour bien comprendre vim dans un premier usage (possible de l'avoir en fr avec 'vimtuto fr')
```
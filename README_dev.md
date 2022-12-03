<!-- ESPACE TEST COLOR -->
<style>
r { color: Red }
o { color: Orange }
g { color: Green }
</style>

# Projet gn_module_monitoring

- [Projet gn\_module\_monitoring](#projet-gn_module_monitoring)
  - [Installation du module monitoring](#installation-du-module-monitoring)
  - [GITFLOW / WORKFLOW](#gitflow--workflow)
    - [Commandes utiles](#commandes-utiles)
  - [DEBUG - MODULE MOITORING](#debug---module-moitoring)
  - [Documentations](#documentations)
  - [TODO](#todo)

| Dépôt                                                                                                          | Branche    | version |
| -------------------------------------------------------------------------------------------------------------- | ---------- | ------- |
| [https://github.com/andriacap/gn_module_monitoring.git](https://github.com/andriacap/gn_module_monitoring.git) | develop-ac | 0.0.3   |
| [git@github.com:andriacap/GeoNature.git](git@github.com:andriacap/GeoNature.git)                               | master     | 2.10.4  |

## Installation du module monitoring

Pour installer le module monitoring on clone le projet en tant que submodule pour "tracker" depuis le dépot parent geonature pour obtenir la version adéquat du module monitoring.

⚠️ ATTENTION

Actuellement seule la branche `master` de Geoanture permet d'installer le module monitoring.
La branche `develop` demande à ce que le module monitoring soit packagé

## GITFLOW / WORKFLOW

Pour la gestion du projet du "nouveau" module monitorig voici les remote/branches concernées par le développement :

- geonature/master@2.10.4
- upstream-ns-monitoring/dev-suivi-eolien
- upstream-ac-monitoring/develop-ac (qui va servir d'environnement de travail et de testde développement)
- upstream-ac-monitoring/devevelop
- upstream-ac-monitoring/dev-suivi-eolien

L'idée de ces deux dépôts `upstream-ac-monitoring` et `upstream-ns-monitoring` qui "fork" le dépot d'origine [https://github.com/PnX-SI/gn_module_monitoring.git](https://github.com/PnX-SI/gn_module_monitoring.git) est de pouvoir travailler sur des environnements compartimentés pour éviter de "chevaucher" le travail des autres développeurs.

Ainsi depuis la branche `dev-suivi-eolien` on créée les autres branches pour lesquels on va venir faire le développement nécessaire (par bloc de fonctionnalités) pour ensuite merger le travail sur cette branche dev-suivi-eolien.

### Commandes utiles

<details>
<summary>Pour merrger uniquement un fichier d'une branche</summary>

Se placer sur la branche pour laquelle on veut merge un fichier d'une autre branche et éxécuter la commande suivante:

```sh
git checkout --patch branch_where_file_is path/to/README_dev.md
```

source : [Lien vers l'article medium](https://towardsdatascience.com/merging-only-one-file-from-a-git-branch-patching-3a9b5a9c3fa6)
 </details>

<details>
<summary>Regroupement de commit pour avoir un hsitorique de commit plus clair:
</summary>

```sh
git rebase -i #commit
```

source : [Lien vers Apero-Tech - Squasher commit](https://apero-tech.fr/squasher-commits-git/)
 </details>


## DEBUG - MODULE MOITORING

Pour pouvoir débugger le module monitoring il faut ouvrir le fichier : `/home/andriac/applications/geonature-master/backend/geonature/app.py` utiliser le fichier de debug nommer : `Python : Current File` (vérifier que les chemins de debug correspondent au chemin absolu présent sur votre ordinateur) et mettre des breakpoints au niveau des fichiers présent à la racine de : `/home/andriac/applications/geonature-master/external_modules/monitorings/backend/config/*.py` .

## Documentations

## TODO

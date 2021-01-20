# Environnement virtuel (virtuelenv) en Python 3



## Prérequis

- [Python 3](https://www.python.org/downloads/)
- Pip : 
  - Windows : Il est installé de base avec python 3 (il faut cocher une case)
  - Linux : `sudo apt-get install python-3-pip`

## Utilisation

1. Installer le package `virtualenv`.

```bash
# Windows
pip install virtualenv

# Linux
python -m pip install virtualenv
```

2. Naviger dans le projet nécessitant un environnement virtuel.
3. Créer l'environnement virtuel.

```bash
# Windows / Linux
python -m virtualenv venv
```

`venv` étant le nom de dossier de configuration.

4. Activer l'environnement virtuel.

```bash
# Windows
venv/Script/activate

# Linux
. venv/Script/activate
```

A partir de ce moment, tout les packages seront dans l'environnement virtuel.

5. Installer les packages nécessaires.

```bash
# Windows
pip install nom_du_package

# Linux
python -m pip install nom_du_package
```

6. Si vous avez une erreur d'installation, faites un `upgrade` de pip dans l'environnement virtuel.

```bash
python -m pip install --upgrade pip
```

7. Vérifier que le package se soit bien installé.

```bash
# Windows
pip list

# Linux
python -m pip list
```

Vous devriez voir les packages que vous avez installé s'afficher.

> Il est normal que les packages que avez installés en dehors de l'environnement virtuel n'apparaissent pas dans la liste de l'environnement virtuel.

8. Vous pouvez utilisez normalement votre projet.

## Exportation du projet

Créer le fichier `requirements.txt`.

```bash
# Windows
pip freeze > requirements.txt

# Linux
python -m pip freeze > requirements.txt
```

Ce fichier va contenir l'ensemble des packages nécessaires pour ce projet ainsi que les versions.

## Récupération du projet depuis un environnement virtuel

1. Récupérez le projet souhaité.
2. Activer l'environnement virtuel.

```bash
# Windows
venv/Script/activate

# Linux
. venv/Script/activate
```

3. Utilisez le projet normalement par la suite.

## Récupération du projet depuis un environnement normal

1. Récupérez le projet souhaité.
2. Installer le package `virtualenv`.

```bash
# Windows
pip install virtualenv

# Linux
python -m pip install virtualenv
```

> Vous n'aurez pas besoin de créer l'environnement virtuel, à moins que le dossier de configuration de l'environnement n'existe via un `.gitignore`.
>
> Dans ce cas, faites la commande suivante.
>
> ```bash
> # Windows / Linux
> python -m virtualenv venv
> ```

3. Activer l'environnement virtuel.

```bash
# Windows
venv/Script/activate

# Linux
. venv/Script/activate
```

> Si vous, à l'étape 2, vous avez eu besoin de créer l'environnement virtuel, vous allez devoir installer les packages nécessaires.
>
> ```bash
> # Windows
> pip install -r requirements.txt
> 
> # Linux
> python -m pip install -r requirements.txt
> ```

Vous pourrez ensuite utiliser le projet normalement.
# Commandes Linux avec Options et Notations Spéciales

## Table des Matières
1. [Commandes de Fichiers et Répertoires](#1)
2. [Commandes Utilisateurs et Permissions](#commandes-utilisateurs-et-permissions)
3. [Commandes de Processus](#commandes-de-processus)
4. [Commandes de Manipulation de Texte](#commandes-de-manipulation-de-texte)
5. [Commandes de Contrôle de Session](#commandes-de-contrôle-de-session)
6. [Commandes Diverses](#commandes-diverses)
7. [Notations Spéciales dans les Commandes](#notations-spéciales-dans-les-commandes)

---

## 1 - Commandes de Fichiers et Répertoires

| **Commande** | **Description**                          | **Options**                                                           |
|--------------|------------------------------------------|-----------------------------------------------------------------------|
| `ls`         | Liste les fichiers et répertoires         | `-l` : détails, `-a` : fichiers cachés, `-h` : taille lisible          |
| `cd`         | Change de répertoire                     | `cd ..` : répertoire parent, `cd -` : répertoire précédent             |
| `pwd`        | Affiche le répertoire courant            | Sans options                                                          |
| `mkdir`      | Crée un répertoire                       | `-p` : crée les répertoires parents                                    |
| `rmdir`      | Supprime un répertoire vide              | Sans options                                                          |
| `cp`         | Copie des fichiers/répertoires           | `-r` : récursif, `-v` : verbeux, `-i` : confirmation                  |
| `mv`         | Déplace ou renomme des fichiers/répertoires | `-i` : confirmation avant d’écraser                                  |
| `rm`         | Supprime des fichiers ou répertoires     | `-r` : récursif, `-f` : force, `-i` : confirmation                    |

---

## 2 - Commandes Utilisateurs et Permissions

| **Commande** | **Description**                          | **Options**                                                           |
|--------------|------------------------------------------|-----------------------------------------------------------------------|
| `chmod`      | Change les permissions d’un fichier      | `-R` : récursif, `u+x` : exécution pour l’utilisateur                 |
| `chown`      | Change le propriétaire et le groupe      | `-R` : récursif, `user:group` : définit propriétaire et groupe         |
| `usermod`    | Modifie les infos d’un utilisateur       | `-aG` : ajout à un groupe, `-L` : verrouille le compte                 |
| `useradd`    | Crée un nouvel utilisateur               | `-m` : répertoire personnel, `-s` : shell par défaut                   |
| `passwd`     | Modifie le mot de passe d’un utilisateur | `-d` : supprime le mot de passe                                        |

---

## 3 - Commandes de Processus

| **Commande** | **Description**                          | **Options**                                                           |
|--------------|------------------------------------------|-----------------------------------------------------------------------|
| `ps`         | Affiche les processus actifs             | `-aux` : tous les processus, `-ef` : affichage détaillé               |
| `top`        | Affiche les processus en temps réel      | `-u` : filtre par utilisateur                                         |
| `kill`       | Termine un processus                     | `-9` : force la terminaison immédiate, `PID` : numéro du processus    |
| `htop`       | Interface interactive de processus       | Sans options                                                          |
| `killall`    | Termine tous les processus d’un nom      | `-v` : verbeux, `-I` : insensible à la casse                          |

---

## 4 - Commandes de Manipulation de Texte

| **Commande** | **Description**                          | **Options**                                                           |
|--------------|------------------------------------------|-----------------------------------------------------------------------|
| `cat`        | Affiche le contenu d’un fichier          | `-n` : numéros de ligne                                               |
| `grep`       | Recherche un motif dans un fichier       | `-i` : insensible à la casse, `-v` : inverse la recherche             |
| `sed`        | Modifie du texte à la volée              | `s/motif/remplacement/` : substitution, `-i` : modifie le fichier     |
| `awk`        | Manipule et formate du texte             | `{print $1}` : première colonne, `-F` : spécifie le séparateur        |

---

## 5 - Commandes de Contrôle de Session

| **Commande** | **Description**                          | **Options**                                                           |
|--------------|------------------------------------------|-----------------------------------------------------------------------|
| `whoami`     | Affiche l’utilisateur actuel             | Sans options                                                          |
| `exit`       | Ferme la session                         | Sans options                                                          |
| `su`         | Change d’utilisateur                     | `su -` : nouvelle session utilisateur                                 |
| `sudo`       | Exécute une commande en super utilisateur | `-s` : ouvre un shell                                                 |

---

## 6 - Commandes Diverses

| **Commande** | **Description**                          | **Options**                                                           |
|--------------|------------------------------------------|-----------------------------------------------------------------------|
| `df`         | Affiche l’utilisation du disque          | `-h` : format humain, `-T` : type de système de fichiers              |
| `du`         | Affiche l’utilisation de l’espace disque | `-h` : format humain, `-s` : résumé                                   |
| `uname`      | Infos système                            | `-a` : toutes les infos, `-r` : version noyau                         |
| `free`       | Affiche l’utilisation mémoire            | `-h` : format humain                                                  |
| `uptime`     | Durée de fonctionnement du système       | Sans options                                                          |

---

## 7 - Notations Spéciales dans les Commandes

| Symbole     | Description                              | Exemple                               |
|-------------|------------------------------------------|---------------------------------------|
| `>`         | Redirige la sortie vers un fichier (écrase le contenu existant) | `echo "texte" > fichier.txt`          |
| `>>`        | Ajoute la sortie à la fin d’un fichier sans écraser le contenu | `echo "ajout" >> fichier.txt`         |
| `<`         | Utilise un fichier comme entrée pour une commande  | `command < fichier.txt`               |
| `&`         | Exécute une commande en arrière-plan     | `sleep 10 &`                         |
| `&&`        | Exécute la commande suivante uniquement si la première réussit | `mkdir test && cd test`               |
| `;`         | Sépare plusieurs commandes sur une seule ligne (exécute successivement) | `command1 ; command2`                |
| `#`         | Marque un commentaire dans un script ou une commande | `# Ceci est un commentaire`           |
| `\`         | Permet de couper une commande longue sur plusieurs lignes | `echo "texte long" \`                 |
| `` ` `` (backtick) | Exécute une commande en ligne et utilise sa sortie comme argument | ``echo `date` ``                      |
| `$()`       | Exécute une commande et remplace par sa sortie (alternative aux backticks) | `echo $(date)`                       |
| `*`         | Correspond à n’importe quel nombre de caractères dans un nom de fichier | `ls *.txt` (liste tous les fichiers .txt) |
| `?`         | Correspond à un seul caractère dans un nom de fichier | `ls fichier?.txt` (correspond à fichier1.txt, fichierA.txt, etc.) |
| `~`         | Représente le répertoire personnel de l’utilisateur | `cd ~/Documents`                      |
| `^`         | Répète la commande précédente avec une correction | `^ancienne^nouvelle` (corrige et réexécute la commande précédente) |
| `{}`        | Délimite une séquence d'arguments ou une plage | `echo {1..5}` (affiche 1 2 3 4 5)     |
| `() {}`     | Définit une fonction dans un script Bash | `function_name() { commands }`        |
| `!`         | Répète une commande spécifique depuis l’historique | `!100` (exécute la commande #100 de l’historique) |
| `!!`        | Répète la dernière commande              | `!!` (réexécute la dernière commande) |
| `$`         | Référence une variable ou une sortie de commande | `$USER` (affiche l’utilisateur actuel) |
| `2>`        | Redirige la sortie d'erreur vers un fichier ou une autre commande | `command 2> erreur.log`               |
| `2>&1`      | Redirige les erreurs vers la sortie standard | `command > fichier.txt 2>&1`          |
| `>` `/dev/null` | Ignore la sortie standard (envoie dans le "vide") | `command > /dev/null`                 |

<hr>
<h3 align="center"> 🧑🏻‍💻 | Made By : <a href="https://github.com/mohamedtalhaouii" target="_blank">Mohamed Talhaoui</a></h3>

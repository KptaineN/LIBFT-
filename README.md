# libft

Une bibliothèque C personnelle créée dans le cadre du cursus 42.
L’objectif est de recréer une partie des fonctions de la `stdlib` et d’ajouter des outils pratiques pour les futurs projets.

## À propos du projet

Cette librairie regroupe des fonctions utilitaires réécrites à la main, avec une gestion propre de la mémoire et un style compatible avec les contraintes du projet `42`.
Elle sert de base solide pour réutiliser du code dans d’autres projets du cursus.

Le dépôt contient aussi deux modules supplémentaires :

- `GNL/` : implémentation de `get_next_line`
- `PRINTF/` : implémentation de `ft_printf`

## Fonctionnalités

### Fonctions de caractères et de test

| Fonction | Rôle |
| --- | --- |
| `ft_isalpha` | Vérifie si un caractère est une lettre alphabétique. |
| `ft_isdigit` | Vérifie si un caractère est un chiffre. |
| `ft_isalnum` | Vérifie si un caractère est alphanumérique. |
| `ft_isascii` | Vérifie si un caractère appartient au jeu ASCII. |
| `ft_isprint` | Vérifie si un caractère est affichable. |
| `ft_isspace` | Vérifie si un caractère est un espace blanc. |
| `ft_tolower` | Convertit une majuscule en minuscule. |
| `ft_toupper` | Convertit une minuscule en majuscule. |

### Fonctions sur les chaînes et la mémoire

| Fonction | Rôle |
| --- | --- |
| `ft_strlen` | Calcule la longueur d'une chaîne. |
| `ft_strlcpy` | Copie une chaîne en limitant la taille de destination. |
| `ft_strlcat` | Concatène une chaîne en respectant la taille du buffer. |
| `ft_strchr` | Recherche la première occurrence d'un caractère. |
| `ft_strrchr` | Recherche la dernière occurrence d'un caractère. |
| `ft_strncmp` | Compare deux chaînes sur un nombre limité de caractères. |
| `ft_strcmp` | Compare deux chaînes lexicographiquement. |
| `ft_strcpy` | Copie une chaîne dans une autre. |
| `ft_strncpy` | Copie une chaîne sur une longueur donnée. |
| `ft_strndup` | Duplique une chaîne sur une longueur donnée. |
| `ft_strdup` | Duplique une chaîne complète. |
| `ft_strjoin` | Concatène deux chaînes dans une nouvelle allocation. |
| `ft_strtrim` | Supprime les caractères d'un ensemble aux bords d'une chaîne. |
| `ft_substr` | Extrait une sous-chaîne. |
| `ft_split` | Découpe une chaîne selon un séparateur. |
| `ft_strmapi` | Applique une fonction à chaque caractère et crée une nouvelle chaîne. |
| `ft_striteri` | Applique une fonction à chaque caractère d'une chaîne en place. |
| `ft_strnstr` | Recherche une sous-chaîne dans une zone limitée. |
| `ft_strcspn` | Mesure la longueur du segment initial sans caractères interdits. |
| `ft_memset` | Remplit une zone mémoire avec une valeur. |
| `ft_bzero` | Met une zone mémoire à zéro. |
| `ft_memcpy` | Copie une zone mémoire vers une autre. |
| `ft_memmove` | Copie une zone mémoire en gérant les recouvrements. |
| `ft_memchr` | Recherche un octet dans une zone mémoire. |
| `ft_memcmp` | Compare deux zones mémoire. |
| `ft_calloc` | Alloue et initialise une zone mémoire à zéro. |
| `ft_bubble_str_sort` | Trie un tableau de chaînes avec un tri à bulles. |

### Fonctions numériques et I/O

| Fonction | Rôle |
| --- | --- |
| `ft_atoi` | Convertit une chaîne en entier. |
| `ft_atol` | Convertit une chaîne en long. |
| `ft_itoa` | Convertit un entier en chaîne. |
| `ft_putchar_fd` | Écrit un caractère dans un descripteur de fichier. |
| `ft_putstr_fd` | Écrit une chaîne dans un descripteur de fichier. |
| `ft_putendl_fd` | Écrit une chaîne suivie d'un saut de ligne. |
| `ft_putnbr_fd` | Écrit un entier dans un descripteur de fichier. |
| `ft_swap` | Échange deux entiers. |
| `ft_swap_str` | Échange deux pointeurs de chaînes. |
| `ft_printf` | Affiche du texte formaté comme `printf`. |
| `ft_putchar` | Affiche un seul caractère. |
| `get_next_line` | Lit un fichier ligne par ligne. |

## Compilation

Le projet se compile avec `make` et génère l’archive statique `libft.a`.

### Commandes utiles

```bash
make
make clean
make fclean
make re
```

- `make` : compile la bibliothèque
- `make clean` : supprime les fichiers objets
- `make fclean` : supprime les objets et `libft.a`
- `make re` : recompilation complète

## Utilisation

Inclure l’en-tête principal dans ton projet :

```c
#include "libft.h"
```

Puis compiler avec la bibliothèque :

```bash
cc main.c -L. -lft
```

## Organisation du projet

```text
LIBFT/
├── ft_*.c
├── libft.h
├── Makefile
├── GNL/
│   ├── get_next_line.c
│   └── get_next_line_utils.c
└── PRINTF/
    ├── ft_printf.c
    ├── ft_print_num.c
    ├── ft_print_pointer.c
    └── ft_print_f.c
```

## Objectif pédagogique

Ce projet permet de mieux comprendre :

- la manipulation des pointeurs
- les chaînes de caractères en C
- la gestion mémoire
- la construction d’une bibliothèque réutilisable
- la compilation d’un fichier `.a`

## Auteur

Projet réalisé dans le cadre du cursus 42.

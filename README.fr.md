# libft

*[English version](README.md)*

Ma propre bibliothèque C, premier projet du cursus de l'école 19 (réseau 42) : 34 fonctions réécrites
d'après la bibliothèque standard du C, ou ajoutées par-dessus. Les projets suivants (Minitalk, Minishell,
Fdf…) s'appuient dessus.

## Contenu

| Groupe | Fonctions |
|---|---|
| Caractères | `ft_isalpha` `ft_isdigit` `ft_isalnum` `ft_isascii` `ft_isprint` `ft_toupper` `ft_tolower` |
| Mémoire | `ft_memset` `ft_bzero` `ft_memcpy` `ft_memmove` `ft_memchr` `ft_memcmp` `ft_calloc` |
| Chaînes (libc) | `ft_strlen` `ft_strlcpy` `ft_strlcat` `ft_strchr` `ft_strrchr` `ft_strncmp` `ft_strnstr` `ft_strdup` `ft_atoi` |
| Chaînes (ajouts) | `ft_substr` `ft_strjoin` `ft_strtrim` `ft_split` `ft_itoa` `ft_strmapi` `ft_striteri` |
| Sortie | `ft_putchar_fd` `ft_putstr_fd` `ft_putendl_fd` `ft_putnbr_fd` |

Les fonctions réécrites suivent leurs équivalents de la libc, cas limites compris : `ft_memmove` copie à
rebours quand les zones se chevauchent, `ft_strlcpy` renvoie la longueur qu'elle a tenté de créer,
`ft_atoi` ignore les espaces de tête et accepte un seul signe, `ft_itoa` gère `INT_MIN`.

## Tests

Un petit programme a comparé ces fonctions à la libc sur des cas limites (`atoi` sur `"  -17x"`, `"+0"`,
`INT_MIN` ; `memmove` avec chevauchement ; `strlcpy` qui tronque ; `split` avec séparateurs répétés ;
`itoa(INT_MIN)`) : aucune différence.

## Compilation

```bash
make                 # produit libft.a
cc main.c libft.a    # dans votre programme : #include "libft.h"
```

`make clean`, `make fclean` et `make re` fonctionnent comme d'habitude.

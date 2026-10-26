# libft

*[Version française](README.fr.md)*

My own C library, the first project of the School 19 (42 network) curriculum: 34 functions rewritten from
the C standard library or added on top of it. Later projects (Minitalk, Minishell, Fdf…) are built on it.

## What is in it

| Group | Functions |
|---|---|
| Characters | `ft_isalpha` `ft_isdigit` `ft_isalnum` `ft_isascii` `ft_isprint` `ft_toupper` `ft_tolower` |
| Memory | `ft_memset` `ft_bzero` `ft_memcpy` `ft_memmove` `ft_memchr` `ft_memcmp` `ft_calloc` |
| Strings (libc) | `ft_strlen` `ft_strlcpy` `ft_strlcat` `ft_strchr` `ft_strrchr` `ft_strncmp` `ft_strnstr` `ft_strdup` `ft_atoi` |
| Strings (new) | `ft_substr` `ft_strjoin` `ft_strtrim` `ft_split` `ft_itoa` `ft_strmapi` `ft_striteri` |
| Output | `ft_putchar_fd` `ft_putstr_fd` `ft_putendl_fd` `ft_putnbr_fd` |

The rewritten functions follow their libc counterparts, including the edge cases: `ft_memmove` copies
backwards when the areas overlap, `ft_strlcpy` returns the length it tried to create, `ft_atoi` skips
leading whitespace and takes one sign, `ft_itoa` handles `INT_MIN`.

## Tested

A small program compared these functions with the libc on edge cases (`atoi` on `"  -17x"`, `"+0"`,
`INT_MIN`; overlapping `memmove`; truncating `strlcpy`; `split` on repeated separators; `itoa(INT_MIN)`):
no difference.

## Build

```bash
make                 # builds libft.a
cc main.c libft.a    # in your program: #include "libft.h"
```

`make clean`, `make fclean` and `make re` work as usual.

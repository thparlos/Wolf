# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: thparlos <thparlos@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/08/15 09:37:48 by thparlos          #+#    #+#              #
#    Updated: 2019/10/15 14:56:33 by thparlos         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME=libft.a

SRC_PATH = srcs
SRC_NAME = ft_putchar.c ft_putstr.c ft_strcmp.c ft_strlen.c ft_atoi.c ft_memset.c \
		ft_bzero.c ft_memcpy.c ft_memccpy.c ft_memmove.c ft_memchr.c ft_memcmp.c \
		ft_strdup.c ft_strncmp.c ft_putnbr.c ft_strstr.c ft_strnstr.c ft_strcpy.c \
		ft_strncpy.c ft_strcat.c ft_strncat.c ft_strlcat.c ft_strchr.c \
		ft_strrchr.c ft_toupper.c ft_tolower.c ft_sstrlen.c get_next_line.c \
		ft_isalpha.c ft_isdigit.c ft_isalnum.c ft_isascii.c ft_isprint.c \
		ft_memalloc.c ft_strnew.c ft_strdel.c ft_memdel.c ft_strclr.c ft_striter.c \
		ft_striteri.c ft_strmap.c ft_strmapi.c ft_strequ.c ft_strnequ.c \
		ft_strsub.c ft_strjoin.c ft_strsplit.c ft_strjoin.c ft_strtrim.c ft_itoa.c \
		ft_putchar_fd.c ft_putstr_fd.c ft_putendl.c ft_putendl_fd.c ft_putnbr_fd.c \
		ft_lstnew.c ft_lstdelone.c ft_lstdel.c ft_lstadd.c ft_lstiter.c ft_lstmap.c \
		ft_strrev.c ft_swap.c ft_sort_integer_table.c ft_print_words_tables.c

OBJ_PATH = objs
OBJ_NAME = $(SRC_NAME:.c=.o)

CC = clang
CFLAGS = -Wall -Werror -Wextra

CPPFLAGS = -I includes

SRC = $(addprefix $(SRC_PATH)/,$(SRC_NAME))
OBJ = $(addprefix $(OBJ_PATH)/,$(OBJ_NAME))

all: $(NAME)

$(NAME): $(OBJ)
	@ar rc $(NAME) $(OBJ)
	@ranlib $(NAME)
	@echo "Compilation of Libft:	\033[1;32mOK\033[m"

$(OBJ_PATH)/%.o: $(SRC_PATH)/%.c
	@mkdir $(OBJ_PATH) 2> /dev/null || true
	@$(CC) $(CFLAGS) -c $< $(CPPFLAGS) -o $@

clean:
	@rm -f $(OBJ)
	@rmdir $(OBJ_PATH) 2> /dev/null || true
	@echo "Libft:	Removing Objs"

fclean: clean
	@rm -f $(NAME)
	@echo "Libft:	Removing Libft"

re: fclean all

.PHONY: all, clean, fclean, re

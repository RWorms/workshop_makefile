# 																																								\
																																								\
- Reprendre votre Makefile réalisé dans l'exercice précédent																									\
- Faire en sorte de compiler tout les fichiers du dossier (sans *.c)																							\
																																								\
																																								\
Indice: https://www.gnu.org/software/make/manual/html_node/Phony-Targets.html#:~:text=A%20phony%20target%20is%20one,name%2C%20and%20to%20improve%20performance.

NAME	=	a.out

SRCS	=	all.c		\
			clean.c		\
			fclean.c	\
			re.c

OBJS	=	$(SRCS:.c=.o)

all:	$(OBJS)
	$(CC)	-o	$(NAME)	$(OBJS)

clean:
	rm	-f	$(OBJS)

fclean:	clean
	rm	-f	$(NAME)

re:	fclean	all

.PHONY:	all clean fclean re
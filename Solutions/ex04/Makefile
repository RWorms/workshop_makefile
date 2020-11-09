#															\
- Faire en sorte de compiler le fichier main.c				\
															\
- Le Makefile doit avoir les règles standard d'Epitech:		\
all: Convertit les fichiers .c en .o et génère le binaire	\
clean: Supprime tout les fichiers .o						\
fclean: Supprime tout les fichiers .o ET le binaire			\
re: appelle la règle fclean et all							\
															\
- Vous ne devez écrire qu'une seule fois le chemin vers les .c

NAME	=	a.out

SRCSFILES	=	all.c 		\
			clean.c 	\
			fclean.c 	\
			re.c

SRCSPATH	=	path/longpath/reallythatslong/franklyitstakingforever/arewethereyet/

SRCS = $(addprefix $(SRCSPATH), $(SRCSFILES))

OBJS	=	$(SRCS:.c=.o)

all: $(NAME)

$(NAME):	$(OBJS)
	$(CC)	-o	$(NAME)	$(OBJS)

clean:
	@rm	-f	$(OBJS)

fclean:	clean
	@rm	-f	$(NAME)

re:	fclean	all

.PHONY: all re clean fclean

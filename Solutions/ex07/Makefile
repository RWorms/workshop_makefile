# 															\
															\
Let's get started !											\
															\
- Faire en sorte de compiler le fichier main.c				\
															\
- Le Makefile doit avoir les règles standard d'Epitech:		\
all: Convertit les fichiers .c en .o et génère le binaire	\
clean: Supprime tout les fichiers .o						\
fclean: Supprime tout les fichiers .o ET le binaire			\
re: appelle la règle fclean et all							\
															\
Créez un makefile capable de passer les tests et de compiler du c et du c++	\
Wildcard est autorisé. Indice: ifeq, suffix

NAME	=	a.out

SRCSEMPTY	=	main

SRCS	=	$(wildcard $(SRCSEMPTY).c*)

OBJS	=
ifeq ($(suffix $(SRCS)),.c)
	OBJS += $(SRCS:.c=.o)
else
	OBJS += $(SRCS:.cpp=.o)
endif

all: $(NAME)

$(NAME):	$(OBJS)
ifeq ($(suffix $(SRCS)),.c)
	$(CC) $(OBJS) -o $(NAME)
else
	$(CXX) $(OBJS) -o $(NAME)
endif

clean:
	rm	-f	$(OBJS)

fclean:	clean
	rm	-f	$(NAME)

re:	fclean all

%.o:	%.c
	gcc $(CFLAGS) -o $@ -c $<

%.o:	%.cpp
	$(CXX) $(CPPFLAGS) -o $@ -c $<

.PHONY : all re clean fclean

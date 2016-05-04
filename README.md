# uffsdb
A simple teaching DBMS

# how to comipile
 uffsdb/Fonte/make

# how to execute
 `uffsdb/Fonte/./uffsdb`
 
# compiler
 uffsdb commands are interpreted using `yacc` and `lex`.
 In the `interface` folder type `make` to compile both.
 You can edit the following files: `parser.h`, `parser.c`, `lex.l`, and `yacc.y`.

# Finding and fixing bugs

Nomes: Andrei Toledo e Jardel Anton

Primeiro erro:
Quando é criada uma tabela ou um atributo com o nome muito grande, acontece uma falha de memória no malloc().
Eventualmente, a tabela é criada com os 2 últimos caracteres estranhos, "lixos".

Segundo erro:
Quando é inserido uma primary key nula, eventualmente, ele dá segmentation fault.
Quando consegue inserir, ele insere como zero, o que era pra dar um erro, já que não é uma "auto increment".

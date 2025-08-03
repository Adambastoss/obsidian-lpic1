Temos bibliotecas estáticas e bibliotecas compartilhadas (dInâmicas)

Bibliotecas **estáticas**: O código da biblioteca é incorporado ao código do programa. O programa passa a não ter dependência de libs em tempo de execução (externas), mas em compensação ficam mais pesados.

Sempre terminam com a letra **a**
Ex: ==libpthread.a==

Bibliotecas **compartilhadas**: Apenas uma cópia da biblioteca precisa ser disponibilizada em tempo de execução, e pode ser utilizadas por diversos programas ao mesmo tempo. O código do programa precisa ter apenas um link que aponte para essa lib externa. O Código fica mais leve.

soname:
	- **nome** da biblioteca (normalmente prefixo **lib**)
	- so (shared object - objeto compartilhado)
	- **versão** da biblioteca


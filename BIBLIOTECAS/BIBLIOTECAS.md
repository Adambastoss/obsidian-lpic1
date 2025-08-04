Temos bibliotecas estáticas e bibliotecas compartilhadas (dInâmicas)

Bibliotecas **estáticas**: O código da biblioteca é incorporado ao código do programa. O programa passa a não ter dependência de libs em tempo de execução (externas), mas em compensação ficam mais pesados.

Sempre terminam com a letra **a**
Ex: ==libpthread.a==


Bibliotecas **compartilhadas**: Apenas uma cópia da biblioteca precisa ser disponibilizada em tempo de execução, e pode ser utilizadas por diversos programas ao mesmo tempo. O código do programa precisa ter apenas um link que aponte para essa lib externa. O Código fica mais leve.

soname:
	- **nome** da biblioteca (normalmente prefixo **lib**)
	- **so** (shared object - objeto compartilhado)
	- **versão** da biblioteca



**PRINCIPAIS DIRETÓRIOS:**

## 🔍 Localizando bibliotecas compartilhadas

As bibliotecas costumam estar nos diretórios:

- `/lib`
    
- `/lib64`
    
- `/usr/lib`
    
- `/usr/lib64`

- /usr/local/lib/
    
- Outros locais configurados via variável ou arquivo de configuração.


### 📁 Diretórios principais:

|Diretório|Uso comum|
|---|---|
|`/lib`|Bibliotecas essenciais para o sistema (arquitetura 32 bits ou genérica)|
|`/lib64`|Bibliotecas para sistemas 64 bits|
|`/usr/lib`|Bibliotecas de programas não essenciais do sistema|
|`/usr/lib64`|Versão 64 bits das bibliotecas em `/usr/lib`|


### `/etc/ld.so.conf` e `/etc/ld.so.conf.d/`

Esses arquivos informam ao sistema onde procurar bibliotecas adicionais.

- `/etc/ld.so.conf`: arquivo principal; 
		Esse arquivo contém apenas uma linha: ==include /etc/ld.so.conf.d/*.conf==
		que aponta para os arquivos que estão dentro do diretório `/etc/ld.so.conf.d/*.conf`)
		

- `/etc/ld.so.conf.d/*.conf`: arquivos adicionais incluídos automaticamente.


**COMANDOS IMPORTANTES:**

### `ldconfig`

Gerenciar ou cache de bibliotecas compartilhadas no sistema. Ele:

- Atualiza (**cria**) o conjunto de links simbólicos das bibliotecas;
    
- Cria (atualiza) o **cache** `/etc/ld.so.cache`;
    
- Leia os diretórios padrão e os listados em `/etc/ld.so.conf`.

- **Deve ser executado sempre que se adiciona um arquivo de configuração** 


### `ldd`
Exibe bibliotecas permitidas por um binário.

### Variável de ambiente `LD_LIBRARY_PATH`

Define diretórios adicionais de bibliotecas **apenas durante a execução**.

bash

CopyEdit

`LD_LIBRARY_PATH=/meu/caminho/lib ./meu_programa`

### **CP**
##### ==COPIAR UM ARQUIVO PARA O DIR ATUAL==
`cp /dir/arquivo .
(O **.** indica o diretório atual )

==COPIAR O ARQUIVO PARA OUTRO DIRETÓRIO ALTERANDO O NOME==
`cp arquivo /novo_diretorio/novo_nomearquivo

**==COPIAR UMA PASTA E TODOS OS SEUS ARQUIVOS E SUBPASTAS==**
`cp -r /dir/dir/nome_pasta

**==COPIAR E MANTER AS PERMISSÕES==**
`cp -p /dir/nomepasta_origem /diretorio_destino

----------------------------------------------------------------
### **FIND**

Procura e localiza arquivos e diretórios.

==ENCONTRAR UM ARQUIVO PELO NOME==
``find . -name "arquivo.txt"

**==ENCONTRAR ARQUIVOS COM UMA EXTENSÃO ESPECÍFICA==**
``find . -name "*.txt"

**==ENCONTRAR POR TIPO==**
``find /dir -type f 
- `f` - Arquivo regular (file)
    
- `d` - Diretório (directory)
    
- `l` - Link simbólico (symbolic link)

**==APAGAR TODOS OS ARQUIVOS .tmp==**
``find /dir -name "*.tmp" -exec rm {} \;

**==MUDAR O DONO DE TODOS OS ARQUIVOS .html PARA O USUARIO ADAM==**
``find /dir -name "*.html" -exec chown adam {} \; 
- `{}` é um placeholder que será substituído pelo nome do arquivo encontrado.
    
- `\;` indica o fim do comando a ser executado.

"Encontre todos os arquivos em `/var/log` que terminam com `.log`, têm mais de 10 megabytes e comprima cada um deles individualmente usando `gzip`."
``find /var/log -name "*.log -size +10MB -exec gzip {} \;

**==ENCONTRAR TODOS OS ARQUIVOS QUE NÃO SÃO DE UM DETERMINADO FORMATO==**
``find /dir -type f -not -name "*.txt"

--------------------------------------------------------------------------

### **MKDIR**

==**CRIA UM DIRETÓRIO**==
``mkdir nome_pasta

**==CRIA VARIAS PASTAS NO MESMO COMANDO==**
``mkdir pasta1 pasta2 pasta3

==**CRIAR UMA PASTA DENTRO DE OUTRA, DENTRO DE OUTRA, DENTRO DE OUTRA**==
``mkdir -p dir/dir2/dir3

**==CRIAR UMA PASTA JÁ ATRIBUINDO AS PERMISSÕES NECESSÁRIAS==**
``mkdir -m 700 nome_pasta

==**CRIA UMA PASTA COM MODO VERBOSO, EXIBE MENSAGEM DE CRIAÇÃO**==
``mkdir -v nome_pasta


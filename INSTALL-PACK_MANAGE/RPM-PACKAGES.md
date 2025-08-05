##### **RPM**

1. Instale, reinstale, atualize e remova pacotes usando RPM, YUM e Zypper.
	**INSTALAR UM PACOTE:**
	==rpm -ivh nome_pacote.rpm==
	
	- `-i`: instala o pacote
	    
	- `-v`: modo verboso
	    
	- `-h`: mostra barra de progresso
	
	**ATUALIZAR UM PACOTE:**
	==rpm -Uvh nome_pacote.rpm==
	
	- `-U`: atualiza ou instala se o pacote não existir. Remove versão antiga e instala uma nova.
	
	**REMOVER UM PACOTE:**
	==rpm -e nome_pacote==



2. Obtenha informações sobre pacotes RPM, como versão, status, dependências, integridade e assinaturas.

	**LISTA OS PACOTES INSTALADOS:**
	==rpm -q== [opções] ==nome_pacote==
	Opções úteis:
	
	- `-qa`: lista todos os pacotes instalados
	    
	- `-qi`: mostra informações do pacote (incluindo **versão**)
	    
	
	    
	- `-qc`: lista arquivos de configuração do pacote
	    
	- `-qd`: lista arquivos de documentação do pacote
	
	**VERIFICA A INTEGRIDADE DO PACOTE:**
	==rpm -V==
	Verifica se arquivos foram modificados desde a instalação.



3. Determine quais arquivos um pacote fornece, bem como descubra de qual pacote um arquivo específico vem.

	- `rpm -ql`: lista todos os arquivos instalados pelo pacote
	
		**ENCONTRAR QUAL PACOTE PERTENCE UM ARQUIVO:**
		``rpm -qf /caminho/do/arquivo




- Conscientização sobre dnf.










**VERIFICAR DEPENDÊNCIAS:**
==rpm -qpR nome-do-pacote.rpm==         # para pacote não instalado
==rpm -qR nome-do-pacote==                  # para pacote instalado


##### **rpm2cpio**

O `rpm2cpio` é uma ferramenta útil para **extrair** o conteúdo de um pacote RPM sem instalá-lo no sistema.
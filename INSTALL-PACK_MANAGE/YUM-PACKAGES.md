##### **YUM** (*alto nível*)
## **📌 Principais Características do YUM**

✅ **Resolução automática de dependências**  
✅ **Suporte a múltiplos repositórios** (configurados em `/etc/yum.repos.d/`)  
✅ **Histórico de transações** (permite desfazer operações)  
✅ **Assinatura GPG de pacotes** (verificação de integridade)  
✅ **Cache de metadados** (acelera buscas)

###### ARQUIVO DE CONFIGURAÇÃO PRINCIPAL:
***/etc/yum.conf***


###### **INSTALAR UM PACOTE:**
``yum install nome_pacote

###### **ATUALIZAR UM PACOTE:**
``yum update nome_pacote

###### **ATUALIZAR TODOS OS PACOTES DE FATO** (*não os respositórios*)
``yum update

###### **REMOVER UM PACOTE:**
``yum remove nome_pacote

###### **PROCURAR PACOTES NOS REPOSITÓRIOS:**
``yum search

###### **MOSTRAR DETALHES DE UM PACOTE:**
``yum info nome_pacote

###### **LISTAR PACOTES INSTALADOS:**
``yum list installed

###### **LISTAR PACOTES DISPONÍVEIS PARA INSTALAÇÃO:**
``yum list available





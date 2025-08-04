
 **Principais áreas de conhecimento:**

- Instalar, atualizar e desinstalar pacotes binários do Debian.
- Encontre pacotes contendo arquivos ou bibliotecas específicas que podem ou não estar instalados.
- Obtenha informações do pacote, como versão, conteúdo, dependências, integridade do pacote e status da instalação (se o pacote está instalado ou não).
- Consciência de apt.
>
- **/etc/apt/sources.list**
- dpkg
- dpkg-reconfigure
- apt-get
- apt-cache

##### **Extensão padrão** de pacotes Debin é **.deb**
Temos gerenciadores de pacotes de **baixo** nível e de **alto** nível

==Baixo== nível: **Não** tratam dependências
Gerenciador de baixo nível padrão: **dpkg**

>

==INSTALAR UM PACOTE:==
**dpkg -i pacote.deb**

==LISTA TODOS OS ARQUIVOS DE UM PACOTE INSTALADO:==
**dpkg -L nome_pacote**

==REMOVER UM PACOTE:==
**dpkg -r nome_pacote**

==REMOVER TODOS OS ARQUIVOS E RESQUÍCIOS DE UM PACOTE REMOVIDO:==
**dpkg --purge** **nome_pacote**
**dpkg -P** **nome_pacote**

==MOSTRAR AS INFORMAÇÕES DE UM PACOTE:==
**dpkg --info pacote.deb**

==LISTAR TODOS OS PACOTES INSTALADOS:==
**dpkg -l**

> 

==CONFIGURAR UM PACOTE:==
**dpkg --configure nome_pacote**
### 🧠 Contexto:

Durante a instalação de um pacote `.deb`, o `dpkg` segue basicamente **duas etapas**:

1. **Extração dos arquivos** do pacote no sistema.
    
2. **Execução dos scripts de configuração**, como `postinst`, `preinst`, etc.
    

Se algo falhar **durante a configuração**, o pacote ficará com o status de **"unconfigured"**. É aí que o `dpkg --configure` entra.



==RECONFIGURAR UM PACOTE INSTALADO:==
**dpkg-reconfigure nome_pacote**



**GERENCIADOR DE PACOTES** de ==ALTO NÍVEL==
#### Resolve todas as **dependências** de forma **automática**

- `apt`:
    
    É o comando recomendado para o uso diário, oferecendo uma interface mais simples e intuitiva. 
    
- `apt-get`:
    
    Continua funcional e compatível, mas pode ser considerado uma opção mais de baixo nível, especialmente útil em casos específicos ou scripts mais antigos.

**ATUALIZA A LISTA DE PACOTES DISPONÍVEIS:**
==apt-get update==


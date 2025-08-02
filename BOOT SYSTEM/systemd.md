
Principais características:

- Paraleliza a inicialização dos serviços, acelerando o boot.
    
- Usa _unit files_ (arquivos de unidade) para definir como serviços e recursos devem ser gerenciados.
    
- Oferece ferramentas para monitorar e controlar o estado do sistema.

## 🧩 **Principais tipos de unidades no `systemd`:**

|**Tipo de Unidade**|**Extensão**|**Descrição**|
|---|---|---|
|`service`|`.service`|Gerencia **serviços e daemons** (ex: `sshd.service`)|
|`socket`|`.socket`|Gerencia **sockets** usados para ativar serviços sob demanda|
|`target`|`.target`|Agrupa unidades; equivale a "runlevels" no SysVinit|
|`device`|`.device`|Representa dispositivos do kernel detectados por udev|
|`mount`|`.mount`|Representa **pontos de montagem** (ex: `/home`)|
|`automount`|`.automount`|Configura **montagem automática** de dispositivos|
|`swap`|`.swap`|Gerencia **espaços de swap**|
|`timer`|`.timer`|Executa unidades baseadas em **tempo agendado** (substitui cron)|
|`path`|`.path`|Monitora **arquivos ou diretórios** e aciona serviços quando há alterações|
|`slice`|`.slice`|Controla grupos de processos (cgroups) — **gerenciamento de recursos**|
|`scope`|`.scope`|Criado automaticamente para processos externos ao systemd|





[[BOOT]]


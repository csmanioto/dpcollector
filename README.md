# Data Power Collector (dpcollector)

Data Power Collector

O PowerCollector é um software em python, OpenSource :)

Essa ferramenta é um coletor de dados instalado no S.O (Windows, Linux, FreeBSD, MacOS) que irá coletar informações sobre:

* SGDB: PostgreSQL e  MySQL
* Web: Apache,
* Network: F5 BigIP (Load Balancer)

Ele substitui o zabbix_agentd e realiza os checks de tudo o que é importante em um servidor de Banco de Dados. Uma desses checks é justamente o balanceamento de banco de dados usando o BigIP.

### eficiência:
Coletando 126 itens para monitorar Linux + MySQL, o PowerCollector gera 9 kbytes de pacote, com bandwith médio de 16kbp/s de upload.

### Agradecimentos:
Quero agradecer ao time de telecom da Catcho Online! Em especial ao Eber Duarte por permitir a criação da ferramenta para instrumentar o ambiente; Willian Santana por dar idéias de métricas e  Darciso Luis Zenatti (O Z) pelo incentivo e sugestões.

Esse projeto foi muito legal para auxiliar na consolidação do meu conhecimento em Python, protocolo Zabbix e ajudou em gerar uma visão mais ampla sobre monitoramento eficiente de ambientes críticos.


## Faz verificação de:

#### MySQL:
  - [x] Horário de Verão
  - [x] Buffers do InnoDB
  - [x] IOPS
  - [x] Tcp Stats
  - [x] Query por segundo Qps
  - [x] Entre outros

#### Sistema Operacional:
  - [x] Espaço em disco
  - [x] Memória ram
  - [x] Swap
  - [x] Hostname
  - [x] Default route
  - [x] Network gateway interface
  - [x] TCP Stats
  - [x] Quantidade de Processos
  - [x] Entre Outros

#### BigIP:
Com essa integração é possível criar regras no Zabbix do tipo: Não alarmar se o serviço cair e a máquina estiver fora do Pool do BigIP :)

 - [x] Lista de pools
 - [x] Pools ativos
 - [x] Pools inativos
 - [x] Membros do pools
 - [x] Status dos membros


### No Radar para fazer:
O código é bem flexivel o que esta na minha lista fazer:
* Integração com PostgreSQL
* Integração com Oracle
* Integração com SQL Server
* Análise de ambiente AWS/RDS
* FreeRadius
* Integração com Apache SOLR
* MongoDB

Com o PCollector é possível integrar as coletas com o Zabbix e criar regras do tipo: Não alarmar se o serviço cair e a máquina estiver fora do Pool do BigIP :)

Um exemplo de eficiência: Coletando 126 itens para monitorar Linux + MySQL, o PowerCollector gera 9kbytes de pacote, com bandwith médio de 16kbp/s de upload.

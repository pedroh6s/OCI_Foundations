# Serviços de Base de Dados

- OCI oferece sistema de bancos de dados single node ou dual node.
- Sistemas single node estão disponíveis usando VMs ou Bare Metal Machines;
- Porém os sistemas dual node estão disponíveis apenas em VMs

Existem 5 serviços de DB na OCI:
1. VM DB System;
2. VM BM System;
3. Oracle RAC;
4. Exadata Db System;
5. Autonomous;
6. MySQL;
7. NoSQL;
8. Autonomous JSON Database. 

## VM DB System
- É uma VM rodando uma instância de Oracle Database;
- O armazenamento usa block storage;
- Um motivo para usar esse serviço é seu provisionamento rápido;

## VM BM System
- É uma Bare Metal Machine rodando uma instância de Oracle Database;
- Como não tem hypervisor a perfomance é muito mais rápida;
- O armazenamento usa Fast Local Storage;
- Um motivo de uso é quando se precisa de um DB realmente rápido.

## Oracle RAC
- Oracle Databases **Running As a Cluster** (RAC);
- Mais de uma instância de DB compartilhando o mesmo disco, porém rodando em nós diferentes;
- Se algum nó falhar a conexão faz fail over para outro nó do cluster;
- Um motivo de uso é quando se precisa de tolerâcia à falha.

## Exadata Db System
- É uma combinação pré-configurada de hardware e software;
- Essa combinação fornece infraestrutura para rodar DBs;
- É uma combinação própria criada pela Oracle cuja vantagem é excelente perfomance para casos específicos.

## Autonomous
- Esse serviço é dividido em dois tipos: Autonous - Shared (multi-tenant) ou Autonomous - Dedicated (single-tenant);
- Esse tipo de DB faz automaticamente praticamente qualquer tarefa: patches, upgrades e self-healing bad data;
- Para automatizar essas tarefas esses DBs usam machine learning;
- Esses DBS são capazes de fazer: self-driving, self-securing e self-repairing;
- Portanto esses DBs fazem todas as tarefas padrão de um DBA, permitindo que esses profissionais se concentrem em outras tarefas que agreguem valor ao negócio;
- Altamente disponível por padrão;
- Seguro por padrão;
- Um DB totalmente auto gerenciado;
- Portanto o tipo mais caro da OCI.

![OCI Databases](Imagens/05%20-%2001.png)

## MySQL
- Serviço totalmente gerenciado;
- Desenvolvido, administrado e suportado pela equipe de trabalho MySQL da Oracle;
- 

## Oracle NoSQL

- Esse modelo tem suporte para JSON, tabela e chave/valor;
- Com latência de 1 dígito em milisegundos.
**Casos de escolha**
- Produzir e consumir dados em altos volumes e velocidade;
- Se for necessário tempo de resposta instantâneo para satisfazer as expectativas do cliente;
-  

## Autonomous JSON Database

- É excelente para desenvolver aplicações que usem documentos JSON.


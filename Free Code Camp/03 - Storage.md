# Serviços de Storage

Para escolher um serviço de storage é preciso avaliar algumas características:
1. Esse armazenamento precisa ser persistente ou não persistente;
2. Tipo de dado: DB, vídeo, áudio, foto, texto;
3. Performance: capacidade, IOPS, throughput;
4. Durabilidade: quantas cópias dos dados manter;
5. Conectividade: armazenamento local ou em rede e como a aplicação acessa os dados;
6. Protocolo: block, file, HTTP, isso determina que tipo de aplicação você pode construir

## Persistência Vs Durabilidade:
- Persistência significa armazenar os dados em segurança;
- Durabilidade significa replicar os dados.  

Existem 5 tipos de serviço de storage:
1. Block Volume;
2. Local NVMe;
3. File storage;
4. Object Storage;
5. Archive Storage;

## Block Volume
- É um disco rígido virtual em que é possível escolher entre HD e SSD;
- São o tipo de armazenamento mais comum para VMs;
- Quando se cria uma VM é comum ligá-la a um Block Volume;
- É diretamente acessado pelo sistema operacional;
- Suporta apenas um volume de escrita, portanto apenas uma VM pode acessar e usar esse disco;
- Esse acesso é feito pela rede mas ainda dentro do mesmo Availability Domain;
- Os dados são gerenciados como blocos de tamanho fixos;
- As instância de computação usam esse serviço de armazenamento da seguinte maneira: cria uma partição, cria um sistema de arquivos e monta o sistema de arquivo.

## Local NVMe 
- Non-Volatile-Memory-Express;
- É um armazenamento localmente anexo ao servidor no Availability Domain
- Perfomance muito alta devido ao grande número de IOPS


## File storage
- Usa algum tipo de file system como NSFv3;
- Isso permite múltiplas conexões ao mesmo dispositivo ao mesmo tempo;
- É possível realizar várias leituras ao mesmo tempo;
- Porém as escritas são travadas (lock) para cada arquivo, ou seja, apenas um usuário pode editar um documento por vez;
- Também está ligado dentro do mesmo Availability Domain mas esse storage é compartilhado ao contrário do Block Volume.
- Os arquivos são gerenciados como pastas e arquivos e não partições no disco.
**OBS:** arquivo armazenado com dados e metadados.

## Object storage
- É um serviço serverless de storage;
- Permite o upload de quantos arquivos o cliente quiser e o serviço escala automaticamente sem perda de dados ou falta de espaço, sem preocupações para o cliente;
- Geralmente esses dados estão altamente disponíveis e são replicados entre vários datacenters;
- Tanto as leituras como as escritas podem ser simultâneas, sem travas (locks);
- É o tipo de storage usado para fotos, áudio, vídeo, logs.
- Muito bom para dados não estruturados e para backups e arquivos.
**OBS:** objeto é armazenado com dados, metados e Unique ID.

## Archive storage
- Cold storage de longa duração;
- É usado para arquivos que raramente são acessados, mas precisam ser mantidos;
- Esse serviço permite armazenar esse tipo de arquivo por um preço bem menor.

# Custo

Block volume é o mais caro e object storage o mais barato.

# Serviços de Migração

A OCI conta com serviços de migração de dados tanto online quanto offline.

1. Data Transfer - offline
2. Storage Gateway - online

## Data Transfer

- Se divide em data transfer disk e data transfer appliance.

Transfer disk: máximo 100 TB
Trnsfer Appliance: máximo de 150 TB

## Storage Gateway

- Pega seus dados de um ambiente on premises e transfere para um bucket na OCI.



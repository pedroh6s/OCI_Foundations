# Serviços para Desenvolvimento de aplicações

- OCI possui 5 serviços para ajudar no desenvolvimento de aplicações
- Esses serviços facilitam na tarefa moderna de desenvolver microsserviços e criar arquiteturas event-driven.

1. Oracle Resource manager(ORM): terraform gerenciado;
2. Functions: serviço serverless;
3. Container Engine for Kubernetes (OKE): kubernetes gerenciado
4. Container registry: serviço gerenciado de registry
5. API Gateway: 

## ORM
- Automatiza o processo de provisionar recursos OCI;
- Ajuda a instalar, configurar e gerenciar recursos;
- Faz isso utilizando Infrastructure As Code (IAC);
- Isso porque é um serviço gerenciado de Terraform;
- Terraform é um serviço de IAC que permite automatizar tarefas de infraestrutura utilizando sintaxe de alto nível;
- A fonte do código terraform pode ser GitHub, uma pasta, Bucket, template, entre outras;
- A partir desse código o resource manager vai formalizar um Job na OCI que vai executar as tarefas comuns do terraform: plan, apply, destroy.

## Functions

- Function as a service;
- Algum evento acontece quando uma função é invocada, é também chamado de arquitetura event-driven;
- As funções rodam dentro de um container;
- Esse container é construído apenas durante a execução da função;
- Esse container é capaz de execução em paralelo;
- O cliente faz o upload do código da função que é empacotado em uma função e armazenado no OCI Registry;
- Então o cliente define ações de gatilho (trigger actions);
- Quando o gatilho é disparado a Oracle Fuction dispara o código;
- O código da Function pode então invocar qualquer número de integrações com serviços OCI ou externos;
- Esse modelo é totalmente baseado em consumo;
- O cliente só é cobrado nos momentos de execução do código;

## OKE
- Kubernetes é um sistema open-source para automatizar deploy, scaling e gerenciamento de aplicações contêinerizadas;
- OKE é um serviço de orquestração de contêineres totalmente gerenciado, escalável e com alta disponibilidade;
- Permite fazer o deploy em nuvem de aplicações contêinerizadas;
- Com OKE é possível escalar clusters e pods;
- Cluster autoscaler automaticamente adequa o tamanho de um cluster kubernetes com base na demanda de workloads;
- Isso é importante porque permite não apenas escalar os pods, como todo o cluster;
- OKE é capaz de fazer auto-upgrade, self-healing (nos nodes);
- Não existem taxas pelo manutenção do cluster;
- O cluster possui 3 cópias e possui alta disponibilidade

## Oracle Container Registry (OCIR)

- É um serviço gerenciado com alta disponibilidade;
- Consiste em um repositório que pode armazenar, compartilhar e gerenciar imagens de contêineres;
- Pode ser usado como um repositório **privado** ou **público** de imagens docker;
- É totalmente integrado com OKE e Oracle Functions

## API Gateway

- Através do API Gateway a API se torna disponível para ser acessada pelos clientes;
- Existe um endpoint no gateway que aplica policies para decidir se o request do cliente deve chegar ao serviço de back-end e ser respondido;
- A API não roda no gateway, apenas o endpoint que acessa a API está disponível no Gateway;
- O API Gatteway é um dispositivo de rede muito parecido com um load balancer: serverless, e anexado à sua rede, totalmente gerenciado e reforçado por políticas de segurança;
- Serviço regional;
- Possui features de: autorização, rate-limiting (limita o número de chamadas de API) e routing;
- Esses Gateways são criados nas VCNs, por isso podem ser criados em Subnets Públicas ou Privadas; 
- Logo é possível criar Gateways públicos ou privados, ;
- Permite monitoramento, logging e 




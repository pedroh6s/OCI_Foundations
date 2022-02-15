# Serviços de Computação

A OCI possui 5 serviços de computação:
1. Virtual Machines (VMs)
2. Dedicated Virtual Hosts
3. Bare Metal
4. Contêineres
5. Functions

**OBS:** apenas os 3 primeiros são considerados compute shapes.

## VMs

- Um servidor multi-tenant rodando uma camada de hypervisor;
- O cliente escolhe a imagem do sistema operacional e roda no servidor;
- Os custos do servidor são divididos com outros clientes

## Dedicated Virtual Hosts

- Um servidor single-tenant rodando uma camada de hypervisor;
- É possível rodar várias VMs;
- Esse servidor não é dividido com mais ninguém;
- Isso garante maior performance e segurança.

## Bare Metal

- Um servidor dedicado sem camada de hypervisor;
- Permite fornecer às suas aplicações acesso direto aos recursos de processador e memória do servidor;
- É mais adequado para workloads especializadas onde o hypervisor diminuiria a performance.

**OBS:** os dois serviços abaixo embora sejam serviços que permitem tarefas de computação, não são considerados compute shapes.

## Contêiner Engines

- Docker as a service;
- Permite rodar contêineres docker em máquinas virtuais.

## Functions

- Serverless compute;
- O cliente apenas faz upload do código e o provedor de cloud cuida do resto;
- O código é projetado para rodar por curtos períodos de tempo e o cliente escolhe um contêiner gerenciado com runtime.

![Level of Control](/Free%20Code%20Camp/Imagens/02%20-%2001.png)















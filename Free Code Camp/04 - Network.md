# Serviços de rede

## Virtual Cloud Network (VCN)
- Uma sessão logicamente isolada do OCI Cloud onde é possível rodar recursos OCI 

## Subnets
- Uma partição lógica do IP de um rede em múltiplos segmentos de rede menores;
- Um pedaço da VCN.
- Podem ser públicas (Public Subnet) ou privadas (Private Subnet);
- As Private Subnets não são incapazes de acessar a internet, mas não é o propósito delas por uma questão de segurança.

## Internet Gateway
- Habilita acesso à internet;
- Localizado na borda do OCI;
- Tráfego de mão dupla, tanto ingresso quanto egresso, inbound e outbound.

## NAT Gateway
- Deixa que recursos em uma subnet privada acessem a internet;
- Tráfego unidirecional;
- Apenas acesso a internet (egresso)(outbound);
- Não permite acesso da internet para a rede (ingresso)(inbound).

## Service Gateway
- Cria um túnel seguro que mantém o tráfego dentro da rede OCI;
- Permite que recursos da VCN acessem recursos públicos da OCI como storage por exemplo;
- Esse serviço não usa a internet ou NAT gateway.

## Dynamic Routing Gateway (DRG)
- Um roteador virtual que fornece um path para tráfego privado entre a VCN e uma rede externa (on premise) que não seja a internet;
- É necessário tanto para uma IPSec VPN quando para um Fast Connect;

## IPSec VPN
- Cria uma conexão segura entre a sua estrutura on premises e a Oracle Cloud.

## Fast Connect
- Faz a mesma coisa que uma IPSec VPN, porém é dedicada;
- Por ser dedicada a conexão é bem mais rápida.

## VCN Peering
- Cria uma conexão entre VCNs;
- Isso permite tratar as duas como uma só rede;
- Entre regiões diferentes é necessário usar uma DRG e isso é chamado de **Remote Peering**;
- Na mesma região é chamado de **Local Peering** 

## DRG v2
- Permite conectar até 300 VCNs na mesma região, facilitando o processo de conectividade. 

![OCI Network](Imagens/04%20-%2001.png)

## VCINs
- Virtual Network Interface Cards;
- Habilita uma instância a se conectar com a VCN;
- Também determina como a instância se conecta a outros endpoints dentro e fora da VCN;
- Sem uma VCIN as instâncias não conseguiriam se comunicar com a internet ou outros serviços de rede da cloud.

# Opções de Firewall Virtual:
A OCI oferece dois tipos de serviços de firewall e ambos usam security rules para controlar tráfico no packet level;
1. Security lists (SLs)
2. Network Security Groups (NSGs)

## Security lists (SLs)
- São associadas a subnets;
- Essas regras de segurança são aplicadas aos VCINs dessas subnets;
- Especificam o tipo de tráfego que pode entrar ou sair da subnet;
- Menos específico.

## Network Security Groups (NSGs)
- Projetada para componentes de aplicação que tem diferentes posturas de segurança;
- São suportados apenas por serviços específicos;
- São diretamente relacionados com VCINs independentemente da subnet que esteja alocado;
- Mais específico.

## Route Tables
- Consiste em um conjunto de regras de roteamento;
- Cada regra especifica um bloco de destino e um alvo;
- Tráfego dentro da VCN é automaticamente cuidado pelo **VCN local routing**;

## Load balancer
- Promove alta disponibilidade e alta escalabilidade;
- A OCI tem diferentes tipos de load balancer.

1. HTTP Load Balancer
- Opera na camada 7;
- Entende HTTP e HTTPS;
- Tem opção pública e privada;
- É uma opção mais inteligente pois pode inspecionar os pacotes de dados da internet;
-  

### Ele pode ser do tipo flexible shape
- Nesse tipo de load balancer pode-se definir o mínimo e máximo de velocidade;
- Na faixa de 10Mbps até 8Gbps

### Ele também pode ser do tipo dynamic shape
- Onde é preciso pré-definir o tipo de máquina: micro, small, medium, large
- Se o tráfego chega aquele shape particular ele escala automaticamente.

2. Network Load Balancer
- Opera nas camadas 3 e 4;
- É compatível com UDP, TCP e ICMP
- Tem opção pública e privada;
- Possui uma latência muito menor do que o HTTP load balancer;
- Melhora a performance;







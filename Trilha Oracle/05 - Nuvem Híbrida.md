# Oracle Hybrid cloud

- Podem ser pequenas ou grandes;
- Pode ser do tipo: Self-Contained (independente) ou Remotely Tethered (conectada remotamente);

# Tamanho:

- Deploy maiores são feitos nas regiões Oracle, sejam Públicas ou dedicas;
- Os Deploys menores são feitos com o auxílio de dispositivos **RED** que são instalados locamente em lugares remotos. 

## Self-Contained
- Podem estar em regiões públicas ou regiões dedicadas (dedicated region cloud@ customer);
- Nesse modelo os clientes recebem exatamente a mesma arquitetura, mesmo modelo de cobrança, mesmo modelo operacional, segurança e mesmo conjunto de serviços disponíveis na nuvem pública;

### Dedicated Region Cloud@ Customer
- Uma região totalmente gerenciada que possui todos os serviços de cloud nos datacenters do cliente em um modelo independente;
- No datacenter on-premises do cliente é instalado o mesmo tipo de hardware, conjunto de software, control plane e data plane da nuvem pública OCI;
- O cliente faz isso por uma questões soberania de dados, compliance;
- Isso permite o melhor dos dois mundos: escalabilidade operacional, gerenciamento, segurança e agilidade da nuvem, mas ao mesmo tempo atende exigências regulatórios e mantém soberania de dados.  
- Todos os serviços disponíveis da nuvem pública estão disponíveis das regiões dedicadas;
- Mesmos modelos operacionais;
- Mesmo SLAs;
- Mesmas cobranças;

### OCI Roving Edge Device (RED)
- Outro modelo self contained;
- Mas é mais voltado para deploys menores;
- É um servidor de node portátil e altamente potente;
- Clientes configuram um RED no console OCI com os mesmos serviços, aplicações e dados que usam na cloud;
- O dispositivo é enviado para o cliente;
- os dispositivos são instalados em campo;
- E então eles são operados com conexão à internet ou sem conexão de rede;
- Eventualmente, com algum tipo de frequência é possível levar esses dispositivos à um local específico e fazer a sincronização de dados;
- Permite fazer algumas operações da nuvem pública em seu próprio ambiente havendo conexão ou não;

## Remotely Tethered
- Um padrão de nuvem híbrida e um rack acessado remotamente nos servidores on premise do cliente;
- O controle do serviço de gerenciamento roda na nuvem pública;
- Dessa forma ele tira vantagem de serviços, governança e controle operacional;
- Porém hardware e dados continuam on-premises;
- Ao logar no console é possível gerenciar tanto os recursos da nuvem pública quanto da parte on premise.
- O principal motivo para escolher essa estratégia é:
1. Manter todos os dados on premises para aumentar a segurança;
2. E ao mesmo tempo migrar o gerenciamento operacional para o OCI.

### Exadata Cloud@ Customer
- Entrega alta performance diretamente no data center do cliente;
- 

## Oracle CLoud VMWare Solution (OCBS)

- VMWare É a fundação da maioria dos datacenters;
- Porém VMWare possui prós e contras;
- O diferencial do OCBS é que ele mantém todos os prós, mas sem ter os contras;
- Portanto toda a experiência se mantém com a liberdade de um ambiente on-premises, mas com as facilidades da cloud.






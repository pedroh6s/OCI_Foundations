# Pricing & Billing

## Pricing Models

## Oracle Universal Credit Pricing (UC)
- É uma forma de economizar dinheiro na OCI;

### Pay as you go (PAYG)
- Também chamado de on demand;
- Não existe pagamento adiantado;
- É cobrado com base nas horas dos serviços consumidos;
- É pago no final do mês

### Montly Flex
- É um compromisso de pelo menos 12 meses;
- Em um valor mensal de ao menos U$D 1000,00;
- Qualquer valor não usado em um mês fica disponível para o próximo;
- Gera uma economia entre 30 e 65%

## Bring Your Own License (BYOL)
- Se o cliente já tiver licença de algum serviço, é possível usar essa licença particular para abater valores de cobrança na OCI.

**OBS:** ao contrário de outros provedores de cloud, na OCI não existe diferente de preços entre regiões.

## Cost Estimator

- Como o nome sugere, permite ao usuário fazer estimativas de preços de serviços;
- Pode ser acessado [aqui](https://www.oracle.com/br/cloud/cost-estimator.html).

## Data Transfer Cost
- Ingress - Data-in é **gratuito** (dados que entram na rede da OCI);
- Egress - Data-out é **cobrado** (dados que saem da rede da OCI);
- Transferência de dados dentro do mesmo AD é **gratuito**;
- Transferência de dados entre diferentes ADs na mesma região é **gratuito**;
**OBS:** isso ocorre porque enesses casos os dados nunca saíram da OCI.

- Transferência de dados entre regiões são **cobrados**;
**OBS:** isso ocorre porque os dados saíriam da OCI e iriam para a internet;
Se existir alguma forma de manter esses dados dentro da OCI durante essa transferência então a transferência provavelmente não será cobrada.

![Transferência de dados](Imagens/07%20-%2001.png)

## Block Volume Pricing

- São avaliados dois fatores para essa cobrança:
1. Custo de armazenamento (Storage Cost);
2. Custo de perfomance (Performance Cost).

### Custo de armazenamento
- GB/mês

### Custo de perfomance
- Volume Performance Unit (VPU)
- VPU per GB / mês

## Resource tags

- É possível atribuir tags para diferentes recursos;
- Essas tags permitem filtrar recursos e podem ser usados em análises de custo para rapidamente determinar custos;

## Análise de custos

- **OCI Cost Analysis** ajuda a visualizar os custos em andamento;
- Possíveis filtros:
1. Compartimentos;
2. Tags nos recursos;
3. Data de início ou fim.

## Relatórios de Uso (Usage Reports)

- Para acessar informações mais detalhadas das contas é possível baixar um **CSV** ou usar a **OCI API**;
- Diariamente é gerado um relatório de custo e é armazenado num bucket de Object Storage;
- Geralmente esses relatórios contém dados de usos de dados nas últimas 24 horas, mas às vezes pode conter dados que demoraram a chegar e são relativos há mais de 25 horas;
- Esses dados podem ser usados pelo usuário da maneira que ele quiser em ferramentas de data visualization.

## Free Tier e Always Free

### Always Free

- 2 Oracle autonomous databases;
- 2 OCI Compute VMs e 1/8 OCPU e 1 GB;
- 2 block volumes 100 GB total;
- Object Storage 10 GB;
- Archive Storage 10 GB;
- 1 load balancer;
- Data-in;
- Monitoração e notificações;
- OCI Developer - workflows automatizados de CI/Credit

### Free Tier

- U$D 300,00 por 30 dias

## Oracle Marketplace

- São imagens de VMs ou stacks de vendedores third-party que são pagos ou gratuitos para usar;
- Também pode ser BYOL;

## Service Level Agreements (SLAs)

- SLA é a garantia de performance, disponibilidade e gerenciabilidade de um serviço;

## Service Limits

- Todo recursos pode ter um certo limite, uma certa cota habilitada para cada tenancy;
- Exemplo: número máximo de instâncias computacionais por AD;
- A maioria desses limites é padrão;
- A menos que o cliente tenha feito um contrato específico com um vendedor;
- É possível pedir aumento desses limites.

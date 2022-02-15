# Governance & Administration

## Pricing

### PAYG

- Pay As You Go (PAYG) - cobra apenas pelos recursos consumidos;
- Sem compromisso prévio;
- Sem período mínimo de serviço;
- O uso é medido a todo tempo;
-  Para alguns recursos como OCI Functions o PAYG é levado a outro nível;
-  Nesse tipo de serviço a cobrança ocorre apenas quando o recurso é consumido;
  
### Annual Universal Credits

- Assinatura anual;
- Essa assinatura gera economia;
- Porém esses créditos devem ser usados no periodo de 1 ano;
- Os descontos variam de acordo com o tamanho e termos do acordo

### Montly Universal Credits

- Mais informações no site

### Bring Your on License (BYOL)

- Isso serve para clientes que possuem licenças on premise;
- Usar essas licenças na cloud gera descontos 

### Fatores que impactam preços

- Tamanho do recurso;
- Transferência de dados;
- Tipo de recurso;


**OBS:** todas regiões possuem o mesmo preço.

### Data Transfer

- Pode equivaler a 1/4 das cobranças ou até mais;
- Isso porque as aplicações estão sempre se comunicando com usuários ou internamento;
- Tráfego dentro do mesmo AD é gratuito;
- Incoming traffic = free;
- Outgoing traffic = preço mais barato que a concorrência.

## Cost Management

### Budgets

- Rastream gastos na tenancy;
- É possível criar budgets para compartimentos;
- É possível configurar alarmes de budget;

### Cost Analysis

- Permite analisar os custos;

### Usage Reports

- Podem ser baixados em formas de arquivos CSV que são gerados diariamente;
- Monstram uso de dados para cara recurso da sua tenancy;
- Esses arquivos são armazenados em um bucket de Object Storage;

### Service Limits e Usage
-  Ferramenta que permite visualizar e configurar limites, cotas e uso;
-  Os recursos da OCI são limitados por padrão para prevenir fraude e uso equivocado;
-  Mas é possível mudar esses limites;

## Tagging

- Pares chave-valor que podem ser usados para organizar melhor os recursos;
- Também permite gerenciar custos;
- Também é possível gerenciar acessos - Tag Based Access Control;
- Existem dois tipos de tag: free form tag e defined tags

### Free Form tags
- Um par chave-valor simples;
- Sem esquema definido;


### Defined tags
- Essas tag são contidas em namespaces;
- Depois de definir um namespace é possível adicionar quantas tags desejar;
- Isso define um esquema;
- Defined tags podem receber policies que pode controlar quem pode aplicar esse tipo de tag;
- É possível definir o data type permitido para uma tag;
- Também é possível definir valores padrão.

**OBS:** depois que um namespace de defined tags é criado ele não pode ser apagado, no caso pode apenas deixar de ser usado.







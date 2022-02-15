# Observability and Management

## Monitoring

- Permite monitorar os serviços da OCI;
- Serviços como: computação, DB, entre outros;
- Emite métricas continuamente para monitorar serviços, que é chamado de monitoramento ativo;
- Alarmes: features que usam essas métricas para monitoramento passivo;
- Alarms possuem trigger actions e métodos de notificação;
- Os triggers são disparados quando uma métrica chega ao limiar definido;
- E então uma notificação é invocada;

### Métricas

- Métricas permitem monitorar saúde, capacidade e performance dos recursos de cloud;
- Exemplos:
1. Utilização de CPU;
2. Utilização de disco das instâncias de computação
- Esses dados podem ser utilizados para determinar quando aumentar a carga, resolver problemas em instâncias, ou para simplesmente entender melhor o comportamento dos sistemas;
- Toda métrica é composta de 3 partes:
```
Metric -> Namespace + Dimension + Metadata
```   
1. Namespace: um indicador do recurso, serviço ou aplicação que emite a métrica, basicamente um identificador;
2. Dimension: qualificador, para filtrar ou agrupar dados de métricas;
3. Metadata: fornece informação adicional para uma métricas

### Alarmes

- Alarmes notificam o usuário quando as métricas atingem determinada condição;
- O serviço de alarmes funcionam em conjunto com o serviço de notificações;


## Logging

- Serviço distribuído, totalmente gerenciado que implica ingestão, gerenciamento e análise de logs de toda a stack;
- Esse serviço traz todos os logs em apenas um visualização: infraestrutura, apllicações, DBs e audits;
- Isso permite gerenciamento centralizado de logs;
- É possível explorar os logs através da engine de busca;
- É possível armanzenar esses logs em outras localizações, até mesmo em soluções de terceiros; 
- Existem 3 tipos de logs:
1. Audit logs: logs relacionados a eventos emitidos pelo OCI Audti Service;
2. Logs de serviço: emitidos por serviços OCI nativos;
3. Custom logs: logs que contém informações de diagnóstico de aplicações customizadas, outros provedores de nuvem ou ambientes on premises.

## Logging Analytics

- Uma forma fácil de se aprofundar no contéudo desses logs;
- Possui visualizações ricas que permitem gerar insights rápido;
- Facilita a exploração dos logs;


## Loggins Vs Logging Analytics

Basicamente Informação Vs Insight.

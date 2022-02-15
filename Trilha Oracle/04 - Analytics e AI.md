# Analytics e Audti

## Data Integration

- Serviço totalmente gerenciado que permite realizar as tarefas de ETL;
- Fornece interface gráfica para desenhar data flows no estilo "what you see is what you get";
- Essa estratégia no code permite criar pipelines de dados sem necessitar de nenhum conhecimento técnico;
- É possível ingerir dados de diferentes fontes.

## Data Flow

- Um serviço serverless totalmente gerenciado para rodar aplicações Apache Spark;
- Serve para praticamente qualquer escala;
- Não requer nenhuma administração;
- O que torna Apache Spark único é que é único framework que combina dados e AI;
- Isso permite realizar transformação e análise de dados em larga escala (big data) e rodar machine learning e algoritmos de AI nesses dados;
- Data Flow analisa dados em Object Storage e Autonomous Data Warehouse e DBs de terceiros;
- Uma aplicação Spark utiliza a API do Spark para realizar tarefas de processamento de dados distribuídos;
- Data Flow aloca as VMs, roda os jobs, captura os outputs de forma segura e encerra o cluster quando não está mais rodando;
- A autenticação e autorização é via OCI Identity e Access Managament


## Data Catalog

- Serviço de gerenciamento de metadados;
- Fornece um ambiente colaborativo único para gerenciar metadados operacionais, técnicos e de negócios;
- Permite coletar, organizar, encontrar, acessar, entender, enriquecer e ativar esses metados;
- Também fornece valor adicional para outros serviços OCI como Data Management Tools, analytics, Data Science e Data Integration;

## Data Science

- Uma plataforma totalmente gerenciada e serverless que permite criar, treinar e fazer o deploy de modelos de machine learning;
- Bastante integrado com outras stacks da OCI, incluindo:
1. Oracle Functions;
2. Data Flow;
3. Autonomous DataWarehouse;
4. Object Storage.

- Tem suporte para ferramentas open-source, como: Jupyter Lab, Tersorflow, entre outros;

### Conceitos:

1. Projetos: espaços colaborativos de trabalho;
2. Notebooks: notebooks Jupyter Labs com bibliotecas do python para análise e construção de modelos de ML pré instaladas;  
3. Modelos: uma representação matemática dos seus dados e processos de negócios.


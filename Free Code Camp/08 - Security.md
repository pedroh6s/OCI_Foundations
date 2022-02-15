# Modelo de Segurança Compartilhada

![Modelo de Segurança Compartilhada](Imagens/07%20-%2002.png)

## Principal

- É uma entidade IAM que permite interagir com recursos OCI;
- 


## Identity Access Managamenet (IAM)

- Permite controlar quem tem acesso aos recursos da Oracle Cloud;
- IAM é composto de:
1. Users
2. Groups
3. Dynamic Groups
4. Policies

### User
- Um usuário ou sistema individual que precisa gerenciar ou usar algum recurso da OCI.

### Groups
- Uma coleção de usuários que precisa do mesmo tipo de acesso a um conjunto de recursos ou Compartimentos

### Dynamic Groups
- Um tipo especial de grupo;
- Esse grupo contém recursos que atendem a regras definidas;

### Policies
- Uma regra que define permissões;
- As políticas ditam quais usuários, grupos, grupos dinâmicos ou compartimentos devem possui permissão para acessar recurso específicos da OCI.
- Por padrão todas as permissões são negadas e é necessários definir as permissões necessárias;
- São definidas com base em uma sintaxe específica:

```
Allow <subject> to <verb> <resource-type> in <location> where <conditions>
```

Exemplo: 
```
Allow group VolumeGroupCreators to manage volume-groups in tenancy
```

**OBS:** Existem 4 verbos:
1. manage
2. use
3. read
4. inspect

## Multi_Factor Authentication (MFA)

- Uma forma de controle de segurança onde após confirmar usuário e senha é necessário usar um segudno dispositivo (celular, por exemplo) para confirmar que está logando;

## Federation Identity

- É a habilidade de habilitar usuários de um domínio a acessar datas de forma segura de outro domínio sem a necessidade de um usuário redundante

## Single Sign On

- É a tecnologia que permite usuários autenticar sem a necessidade de fazer login ou ter pares de credenciais separadas para sistema de terceiros.

## Identity Provider

- Utiliza um provider de confiança para autenticar e acessar outros serviços;
- É muito comum com facebook e g-mail;
- A Oracle possui o Oracle Identity Cloud Service.

## Authentication Vs Authorization
- Existem 3 formas de autenticação na OCI:
1. Nome de usuário/senha
2. API signing Keys
3. Tokens de autenticação 

- Existe apenas uma forma de autorização:
1. Policies

## Encryption DataBases

### Encryption at-rest
- Todos os dados já estão encriptados;
- Promove a segurança de dados que não estão em movimento;
- 

### Encrypted in-transit
- Quando os dados deixam o dispositivo de origem e se encaminham para o armazenamento na Oracle Cloud os dados são encriptados no trajeto;
- Assegura a segurança de dados transferidos de uma localização pra outra.

### Bring your own Keys (BYOK)
- O usuário define a chave de encriptação a ser usada na transferência de dados.

### Transparent Data Encryption (TDE)
- É uma tecnologia usada pela Microsoft, IBM e Oracle para encriptar arquivos de bancos de dados.

### Oracle Data Safe
- É um console de segurança que monitor dados sensíveis como os dados em OCI DB.

### Oracle database vault
- Restringe acesso à áreas específicas em um DB Oracle a qualquer usuário
- Mesmo aqueles que possuem acesso administrativo.

![Encryption DataBases](Imagens/08%20-%2001.png)

## Oracle Data Safe

- É um centro de controle unificado para os DB Oracle do usuário;
- Esse serviço ajuda a:
1. Entender a sensibilidade dos dados;
2. Avaliar Risco aos dados;
3. Implementar e monitorar controles de segurança;
4. Avaliar segurança dos usuários;
5. Monitorar atividade dos usuários;
6. Endereçar necessidades de compliance.

## OCI vault

- Facilita a criação, controle e ratação de chaves de encriptação usadas para a encriptação de dados na OCI;
- É um Hardware Security Model (HSM) multi-tenant;
- É muito custo-efetivo pois um HSM é bastante caro, mas por ser compartilhado por múltiplos clientes torna mais barato.

## OCI Web Application Firewall (WAF)

- Protege aplicações web de common web exploits.


## Cloud Guard

- Monitora e indentifica problemas de segurança;
- E é possível automatizar a resposta corretiva aos problemas identificados.

## Security Zones

- Configura uma localização onde não é possível desabilitar a segurança;
- É possível realizar a segurança de compartimentos (portanto grupos de recursos) atribuindo a eles uma zona de segurança;
- Então poderíamos por exemplo colocar todos nossos recursos de computação dentro de um mesmo compartimento e atribuir esse compartimento uma zona de segurança, dessa maneira em caso de brecha de segurança o invasor não conseguiria de forma simples criar qualquer recurso computacional;
- Nessas zonas não é possível desabilitar a segurança.

## Security Advisor

- É um serviço que unifica zonas de segurança, cloud guard e outros recursos de segurança da OCI;

## Bastion

- Um serviço totalmente gerenciado que fornece conexão RDP e SSH direta e segura com suas VMs;
- São entidades lógicas que fornecem acesso público a recursos alvo que não podem ser acessados pela internet;
- Esses recursos alvo podem ser DBs, VMs, etc;
- Bastions precisam estar em subnets públicas;
- Autenticação e Autorização via IAM;
- Lista CIDR block, especificam quais endereços IP podem se conectar a um bastion;
-  
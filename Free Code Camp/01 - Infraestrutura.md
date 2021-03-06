## Bare Metal Machine

- Chamamos de bare metal quando nos referimos a uma máquina física ao invés de uma VM ou um container;
- No caso é toda uma máquina (servidor físico) que é utilizada por apenas um cliente.

## Regiões

Existem 3 tipos de regiões:

1. Comercial
- Qualquer cliente pode criar recursos nessas regiões.
2. Governamental
- Apenas governos podem criar recursos nessas regiões.
3. Azure connected
- Algumas regiões comerciais estão conectadas à Azure.

## Tenancy

- Quando um cliente se inscreve no OCI a oracle cria uma **Tenancy** para a empresa;
- Uma **tenancy** é uma partição segura e isolada dentro da OCI;
- Em uma **tenancy** é possível: criar, organizar e administrar seus recursos na cloud.
- A **tenancy** é considerado o **compartimento** root.

## Compartimentos

- É uma coleção lógica de recursos relacionados que podem ser acessados apenas por um certo grupo que recebeu permissão por um administrador;
- Compartimento Root é criado automaticamente quando o cliente se inscreve na OCI e esse compartimento possui todos os recursos da oracle cloud;
- Mas a melhor prática é criar compartimentos para isolar os recursos;
- Isso permite controlar o acesso a esses recursos via Policies e Groups;
- Recursos em compartimentos diferentes podem interagir;
- Portanto eu poderia criar um compartimento para recursos de rede e outros para computação;
- E obviamente eu posso colocar um load balancer antes das minhas VMs;
- Recursos podem ser movidos entre compartimentos;
- Os compartimentos são os mesmos entre regiões;
- O que é possível fazer é escrever policies para prevenir acesso de usuários em regiões específicas.

### Características:

- É possível aninhar até 6 níveis de compartimentos;
- É possível adicionar ou deletar componentes sempre que necessário;
- Compartimentos não são específicos para regiões, então é possível agrupar recursos entre regiões;
- Recursos podem facilmente ser movidos para outros compartimentos;
- Recursos dos compartimentos podem interagir entre si;
- É possível aplicar **políticas** aos compartimentos para determinar acesso de usuários;
- É possível associar um compartimento a um **budget** para análise de custo.

## OCIDS

- Oracle Cloud IDs
- É um identificador único para cada recurso da oracle cloud

    








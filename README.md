# Desafio DIO Power BI com Azure e MySQL

Este repositório contém a entrega do desafio do módulo 3 do curso de Power BI da DIO, focado em integração de banco de dados MySQL com o Power BI, usando dados armazenados na Azure. O objetivo foi realizar transformações e integrações de dados, aplicando boas práticas de modelagem e visualização para criar um relatório final no Power BI. 

## Descrição do Desafio

A tarefa principal foi importar dados de um banco de dados MySQL, realizar transformações de dados no Power Query e criar visualizações no Power BI. O foco do desafio foi na criação de relacionamentos, junção de tabelas e uso de transformações no Power Query.

## Objetivos Alcançados

### 9. Mesclagem entre Tabelas "employee" e "departament"
Foi realizada a mesclagem entre as tabelas **employee** e **departament**, utilizando as colunas `Super_ssn` (da tabela "employee") e `Ssn` (da tabela "departament"). Essa união permitiu que cada funcionário fosse associado ao seu respectivo gerente e ao departamento no qual trabalha.

### 11. Junção Recursiva na Tabela "employee"
Realizei uma junção dentro da própria tabela **employee**. Utilizei a coluna `Super_ssn` (que identifica o supervisor/gerente do funcionário) e a relacionei com a própria coluna `Ssn` da tabela **employee**. Isso criou um relacionamento que permite visualizar o nome do gerente responsável por cada funcionário.

### 14. Mesclagem de Departamentos e Localizações
No exercício 13, foi realizada uma mescla entre a tabela de departamentos e suas localizações. Isso resultou em uma tabela única que garante a unicidade de cada combinação de **departamento e localização**, essencial para um modelo estrela mais estruturado. 
- **Por que usamos mesclagem?** Mesclagem foi a escolha correta porque estávamos combinando informações de duas tabelas diferentes para formar uma única. Isso é crucial para gerar uma tabela com todas as combinações de departamentos e suas respectivas localizações. Se tivéssemos utilizado "atribuir", só conseguiríamos alterar ou criar valores dentro de uma única tabela, o que não atenderia ao objetivo de integração entre tabelas.
  
## Como Visualizar

1. Clone este repositório:
   ```bash
   git clone https://github.com/vitorshaft/DesafioDIOPbiAzure.git
    ```
2. Abra o arquivo .pbix no Power BI Desktop.
3. Explore as páginas e visualizações para entender as junções e transformações aplicadas.

## Considerações Finais
Este desafio me proporcionou a oportunidade de aprofundar meus conhecimentos em:

- Integração de dados do MySQL com o Power BI;
- Criação de junções e relacionamentos entre tabelas no Power Query;
- Construção de modelos de dados eficientes para análise.

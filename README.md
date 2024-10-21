
## Desafio Power BI 
## ## Descrição do Projeto
Este projeto tem como objetivo demonstrar o processo de criação de um dashboard no Power BI a partir de uma base de dados de vendas hospedada no MySQL Azure. O foco principal é a transformação e limpeza dos dados para garantir a qualidade e a consistência das informações utilizadas na visualização.
## ## Etapas do Projeto
Configuração do Ambiente:

Criação da Instância MySQL no Azure: Uma instância do MySQL foi criada no Azure para hospedar a base de dados.
Criação do Banco de Dados: O banco de dados foi criado com base no esquema disponível no repositório GitHub.
Conexão Power BI: O Power BI foi configurado para se conectar à instância do MySQL no Azure.

Transformação dos Dados:

Análise Inicial: Foram realizadas análises para identificar problemas nos dados, como tipos de dados incorretos, valores nulos e inconsistências.
Limpeza e Transformação: As seguintes transformações foram aplicadas:
Verificação de Cabeçalhos e Tipos de Dados: Os cabeçalhos das colunas foram verificados e os tipos de dados foram ajustados, especialmente para valores monetários que foram convertidos para o tipo double.
Tratamento de Valores Nulos: Valores nulos foram analisados e, em alguns casos, removidos ou substituídos por valores apropriados.
Relacionamento entre Funcionários e Gerentes: Foi verificado se todos os funcionários possuíam um gerente associado e se todos os departamentos possuíam um gerente.
Normalização de Dados: Colunas complexas foram separadas em colunas mais simples e dados duplicados foram removidos.
Criação de Tabelas Relacionadas: As tabelas de funcionários e departamentos foram mescladas para criar uma única tabela com informações mais completas sobre os funcionários.
Agrupamento de Dados: Os dados foram agrupados para obter informações agregadas, como a quantidade de funcionários por gerente.

## ## Diretrizes para Transformação dos Dados
Verificação de Dados: Sempre verifique os dados antes de iniciar qualquer transformação.
Tipos de Dados: Certifique-se de que os tipos de dados estão corretos para cada coluna.
Valores Nulos: Trate os valores nulos de forma cuidadosa, considerando o impacto na análise.
Relacionamentos entre Tabelas: Estabeleça relacionamentos claros e precisos entre as tabelas.
Normalização: Mantenha os dados normalizados para evitar redundâncias.
Agrupamento: Agrupe os dados de acordo com as necessidades da análise.

## ## Query SQL para Junção de Tabelas:
SQL

SELECT 
    e.*,
    d.department_name
FROM 
    employees e
INNER JOIN 
    departments d ON e.department_id = d.department_id;
    
## ## Por que Usar Mesclar e Não Atribuir:
O mesclar (merge) é utilizado quando queremos combinar duas tabelas com base em uma chave comum, criando uma nova tabela com todas as linhas de ambas as tabelas. O atribuir (append) é utilizado para adicionar linhas de uma tabela ao final de outra tabela, sem a necessidade de uma chave comum. No caso da junção de funcionários e departamentos, o mesclar é mais adequado porque queremos combinar as informações de ambas as tabelas com base no ID do departamento.

Desenvolvimento de Dashboards: Serão desenvolvidos dashboards interativos para visualizar os dados e obter insights relevantes.
## ## Observações:
Este README será atualizado conforme o avanço do projeto.
## ## Tecnologias Utilizadas:
| Tecnologia | Descrição | Versão | Uso no Projeto |
|---|---|---|---|
|![grafico-preditivo](https://github.com/user-attachments/assets/83201e32-39a6-4715-9d85-fe794994082d)Power BI | Ferramenta de análise de negócios e visualização de dados da Microsoft. | Mais recente | Visualização de dados |
| MySQL    | Sistema gerenciador de banco de dados relacional (SGBDR) open source, popular por sua velocidade e flexibilidade. | 8.0 | Armazenamento de dados |
| Azure    | Plataforma de computação em nuvem da Microsoft que oferece uma ampla gama de serviços, incluindo bancos de dados, análise de dados e inteligência artificial. | N/A | Hospedagem |

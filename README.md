### 🚀 Projeto de Análise de Dados de Funcionários (Employees’ Data Analysis)

Este projeto faz parte do curso de **Analista de Dados da Mate Academy**. O objetivo foi aplicar técnicas básicas de limpeza, transformação e agregação de dados utilizando o **Google Sheets** para extrair insights chave de um conjunto de dados de funcionários.

### 🛠️ Ferramentas e Habilidades Aplicadas

* **Google Sheets:** Utilizado para todas as operações de limpeza, transformação e análise de dados.
* **Limpeza de Dados:** Uso de funções de texto como `SUBSTITUIR` (ou `REPLACE`) e `ARRUMAR` (ou `TRIM`).
* **Transformação de Dados:** Uso de funções como `CONCATENAR` (ou `CONCATENATE`) e `SPLIT` (ou `DIVIDIR TEXTO EM COLUNAS`).
* **Análise e Agregação:** Uso de funções como `MÁXIMO` (`MAX`), `MÉDIA` (`AVERAGE`), `MAIOR` (`LARGE`), `CONT.SE` (`COUNTIF`), e `ÚNICO` (`UNIQUE`).

### 📂 Estrutura do Repositório

* `employee_data_clean.csv`: O conjunto de dados original de funcionários, após a limpeza e transformação.
* `README.md`: Este arquivo, detalhando o projeto.
* [Link para a Planilha Original](https://docs.google.com/spreadsheets/d/19WM98tU9EP5qNd-Ykzxkky1mzq7GzFDyVW-_qkdF0XA/edit?usp=sharing): Link para a planilha do Google Sheets (apenas visualização) para que o trabalho possa ser conferido interativamente.

### 🧹 Etapas de Limpeza e Transformação (Data Wrangling)

A parte mais importante de um projeto de dados é a manipulação inicial. Foram executadas as seguintes transformações, que podem ser verificadas na aba **"Employee Sample Data"** da planilha:

1.  **Limpeza do EEID:** A letra 'E' foi removida da coluna `EEID` usando a função `SUBSTITUIR` (ou `REPLACE`) para garantir que a coluna fosse puramente numérica, facilitando futuras análises.
2.  **Criação de Full Name:** As colunas `First Name` e `Last Name` foram combinadas em uma nova coluna chamada `Full Name`, com o formato "Sobrenome Nome" (Ex: Davis Emily), usando a função `CONCATENAR`. As colunas originais foram excluídas, atendendo ao requisito.
3.  **Garantia da Estrutura:** As colunas `Title`, `Department` e `Business Unit` foram mantidas e limpas de espaços extras com a função `ARRUMAR` (`TRIM`).

### 📊 Resultados da Análise (Aba "Dados dos funcionários")

Os seguintes insights gerenciais foram extraídos e apresentados na aba separada, usando funções de agregação:

| Métrica Solicitada | Função (Exemplo) | Resultado |
| :--- | :--- | :--- |
| **Idade do funcionário mais velho** | `MAX(coluna idade)` | 65 anos |
| **Idade média dos funcionários** | `AVERAGE(coluna idade)` | 44.42 anos |
| **Data de contratação mais antiga** | `MIN(coluna data de contratação)` | 1/9/1992 |
| **Contagem por Gênero (F/M)** | `COUNTIF(coluna gênero, "Female")` | Female: 519 |
| | `COUNTIF(coluna gênero, "Male")` | Male: 485 |
| **Número de países** | `COUNT(UNIQUE(coluna país))` | 3 Países |
| **Lista de Departamentos** | `UNIQUE(coluna departamento)` | IT, Finance, Sales, Accounting, Human Resources, Engineering, Marketing, etc. |

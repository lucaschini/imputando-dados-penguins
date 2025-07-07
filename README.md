# Projeto de Imputação e Análise de Dados: Dataset Penguins

## Descrição do Projeto

Este projeto tem como objetivo demonstrar técnicas de tratamento de dados ausentes (imputação) e a subsequente análise e classificação de um conjunto de dados. Utilizamos o popular dataset "Penguins", o qual foi intencionalmente modificado para incluir uma porcentagem de valores ausentes, simulando cenários comuns em dados reais. O processo inclui a preparação dos dados, aplicação de métodos de imputação e a classificação das espécies de pinguins com base em suas características físicas.

## Tecnologias Utilizadas

O desenvolvimento deste projeto foi realizado utilizando as seguintes bibliotecas Python:

* **Pandas**: Para manipulação e análise de dados.
* **NumPy**: Para operações numéricas e geração de dados aleatórios.
* **Seaborn**: Para visualização estatística de dados.
* **Matplotlib**: Para criação de gráficos.
* **Scikit-learn (sklearn)**:
    * `KNNImputer`: Para imputação de valores ausentes utilizando o método dos K-vizinhos mais próximos.
    * `MinMaxScaler`: Para normalização de dados.

## Estrutura e Processo do Projeto

O fluxo de trabalho deste projeto está dividido nas seguintes etapas principais:

1.  **Carregamento e Preparação dos Dados**:
    * O dataset 'penguins' é carregado utilizando a biblioteca Seaborn.
    * Uma porcentagem aleatória de células (30%) é removida intencionalmente do dataset para simular a presença de valores ausentes, criando um cenário desafiador para a imputação.
    * É fornecida uma visão geral inicial do dataset, incluindo informações sobre os tipos de dados e a contagem de valores não nulos após a remoção.

2.  **Imputação de Valores Ausentes**:
    * Esta seção é dedicada à aplicação de técnicas de imputação para preencher os valores `NaN` (Not a Number) introduzidos na etapa anterior. O notebook explora a imputação, inicialmente focando em colunas numéricas e posteriormente abordando variáveis categóricas.
    * Para dados numéricos, a estratégia de imputação baseia-se em `KNNImputer`, seguido por `MinMaxScaler` para normalização.
    * Para dados categóricos, a imputação é realizada através de um processo manual empírico que classifica `species`, `island`, e `sex` utilizando condições baseadas em atributos como `body_mass_g`, `flipper_length_mm`, `bill_depth_mm`, e `bill_length_mm`. Também utilizando Regressão Logística para imputação.

3.  **Análise Pós-Imputação**:
    * Após a imputação dos valores ausentes, o dataset é novamente visualizado, incluindo a geração de pairplots, para analisar a distribuição dos dados e as relações entre as variáveis.
    * A etapa também inclui a análise descritiva de atributos chave (como `body_mass_g`, `flipper_length_mm`, `bill_depth_mm`, `bill_length_mm`) para cada espécie imputada, confirmando a consistência dos resultados.

## Resultados Atingidos

Através do trabalho realizado podemos perceber como a análise exploratória é importante para processos posteriores ao se trabalhar na base de dados, visando assim a continua melhora da qualidade dos dados imputados através de um processo de tentativa e erro.
Conseguimos deixar a base de dados o mais "normal" possível apesar de outliers nítidos.

## Como Executar

Para replicar e executar este projeto, siga os passos abaixo:

1.  **Clone o Repositório**:
    ```bash
    git clone imputando-dados-penguins
    cd imputando-dados-penguins
    ```
2.  **Instale as Dependências**:
    Certifique-se de ter as bibliotecas necessárias instaladas. Você pode instalá-las via pip:
    ```bash
    pip install pandas numpy seaborn scikit-learn matplotlib
    ```
3.  **Execute o Notebook Jupyter**:
    Abra e execute o arquivo `MD_Trabalho2_v1.ipynb` em um ambiente Jupyter (Jupyter Notebook, JupyterLab ou Google Colab).
    ```bash
    jupyter notebook MD_Trabalho2_v1.ipynb
    ```
    Ou, se preferir usar o Google Colab, faça o upload do arquivo `MD_Trabalho2_v1.ipynb` diretamente na plataforma.

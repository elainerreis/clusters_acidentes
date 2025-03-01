**Análise de Clusters em Acidentes de Trânsito no Nordeste do Brasil: Ingestão de Substâncias e Defeitos nas Rodovias**

Este projeto analisa os acidentes de trânsito na região Nordeste do Brasil, focando em duas causas principais: ingestão de substâncias e defeitos na via. Os dados foram coletados, tratados e segmentados em clusters para melhor compreensão dos padrões de ocorrência. A análise explora dados históricos de acidentes fornecidos pela Polícia Rodoviária Federal (PRF), disponível em [Dados Abertos da PRF](https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf).

**Dados**

Utilizamos as tabelas de acidentes por ano (agrupados por pessoa, incluindo todas as causas e tipos de acidentes) dos anos de 2019 a 2024. Após a junção, exploração e tratamento dos dados, foi feita uma filtragem para selecionar apenas os dados da região Nordeste.
Foi realizada uma análise previa dos dados via excel.

As causas de interesse foram as seguintes:

1. Ingestão de Substâncias:

-"Ingestão de Álcool"

-"Ingestão de Substâncias Psicoativas"

-"Ingestão de álcool pelo condutor"

-"Ingestão de substâncias psicoativas pelo condutor"

2. Defeitos na Via/Pista:

- "Defeito na via"

- "Pista em desnível"

- "Acostamento em desnível"

- "Falta de acostamento"

- "Demais falhas na via"

Os dados foram processados e analisados para identificar padrões e agrupar os municípios com características semelhantes.

**Como Utilizar**

1. Instale as dependências necessárias com:

pip install -r requirements.txt

2. Execute o notebook ETL.ipynb para processar e visualizar os dados.

**Tecnologias Utilizadas**

- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)

-  Notebook

- Excel (análise preliminar)

- PowerBI (Criação do deshboard para a análise visual dos clusters)

**Objetivos**

- Identificar padrões nos acidentes causados por ingestão de substâncias e defeitos na via.

- Clusterizar os municípios para facilitar análises e ações preventivas.

**Identificação da Quantidade Ideal de Clusters**

Para determinar o número ideal de clusters, aplicamos os métodos do cotovelo, índice de silhueta, Davies-Bouldin Index e Calinski-Harabasz Index. Com base na análise desses índices, decidimos segmentar os dados em 3 clusters.

**Descrição dos Clusters**

Cluster 0

    Ingestão de Substâncias: Média de 9,56 (desvio padrão: 9,71), com valor máximo de 42, indicando baixa variação e poucos casos extremos.
    Defeitos na Via: Média de 1,86 (desvio padrão: 3,44), sugerindo uma baixa incidência desse tipo de acidente.
    Municípios: Composto por cidades menores e com infraestrutura mais simples, como Cruz do Espírito Santo e Morada Nova.

Cluster 1

    Ingestão de Substâncias: Média de 244,77 (desvio padrão: 73,8), mostrando forte associação com acidentes neste grupo.
    Defeitos na Via: Média de 26,38 (desvio padrão: 11,76), indicando também uma influência significativa, mas menor que a ingestão de substâncias.
    Municípios: Inclui cidades de médio porte e regiões metropolitanas, como João Pessoa e Feira de Santana, onde o tráfego intenso e a urbanização contribuem para o aumento de acidentes.

Cluster 2

    Ingestão de Substâncias: Média de 76,61 (desvio padrão: 33,43), ainda alta, mas inferior ao Cluster 1.
    Defeitos na Via: Média de 9,09 (desvio padrão: 11,59), indicando uma presença moderada de acidentes devido a defeitos nas vias.
    Municípios: Composto por grandes cidades, como Salvador e Serra Talhada, que enfrentam desafios relacionados à infraestrutura e fiscalização.

Conclusão

A segmentação dos municípios permite direcionar ações de acordo com os padrões observados:

    Cluster 0: Municípios menores, com menos acidentes e baixa incidência de defeitos nas vias.
    Cluster 1: Áreas urbanizadas com alta incidência de acidentes devido à ingestão de substâncias, associados também a problemas de infraestrutura.
    Cluster 2: Grandes cidades, onde tanto a ingestão de substâncias quanto os defeitos na via contribuem significativamente para os acidentes.

Essa análise possibilita a criação de políticas públicas específicas para melhorar a segurança viária em cada tipo de município.
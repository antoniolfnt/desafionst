>Desafio proposto para o cargo de MLOps Nestlé, o desafio proposto consiste em:
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
- Você recebeu 6 bases distintas: Cargos, CEP, Clientes, Funcionários, Nível e PQ
- Lembre que somos a maior empresa de bens de consumo do mundo e que no dia a dia você irá trabalhar com bases muito maiores.
- Must have: ETL e Documentação. 
- Escolha uma linguagem para demonstrar a lógica (python, pyspark, scala ou R)
- Utilização de pelo menos 2 funções (Window, GroupBy, Union)
- Lembre-se: Você é o responsável por tratar e fazer os relacionamentos dessas bases da melhor maneira possível!
- O entregável poderá ser uma apresentação ou os códigos comentados com a documentação (ou ambos)

>Nice to have:
- 5 insights relevantes dos datasets apresentados. 
- Utilização de uma Biblioteca/Framework extra (exemplo Pandas).
- Lógica ou tratativa para dados sensíveis.
- Data visualization.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

> Fases de desenvolvimento
1) ETL + EDA (ETL.ipynb)
  - Inicialmente foi feito uma EDA para entendimento das bases, visualizar suas colunas, datatype e tamanhos.
  - Posteriormente foi feito uma análise, foi lembrado que irá ser trabalhado com bases muito maiores, mas no exemplo as bases estão em um formato e tamanho ok, então todo o desenvolvimento foi feito utilizando Python e Pandas. Claro, Pandas não é escalável e poderia utilizar o Pyspark. Mas dado ao problema proposto, todas as transformações feitas em Pandas aqui neste desafio podem ser modificadas para Pyspark.
  - Utilizei os principais conceitos para transoformação e qualidade de dados, Verificação de campos nulos, Unicidade para as chaves...
  - Utilizei o conceito de Delta onde Fiz as camadas Bronze, Silver e Gold. Bronze seria os dados RAW, para chegar na camada Silver fiz uma transformação apra leitura dos dados e transformei de csv para parquet. E para colcoar os dados na camada Gold veio a validação dos dados e construção das lógicas e relacionamentos entre as tabelas. 
  - E por fim a visualização com Plotly e abaixo de cada gráfico fiz meus comentários sobre insights que pude observar.
  - O código está todo documentado sobre o processo do ETL e também tem um aquivo "desafionestle.pdf" onde pode ser visualisado a estrutura dos dados com seus campos e relacionamentos.
  - No arquivo "infra.png" está o desenho da arquitetura e linhagem dos dados

2) Data Visualization (DataVisualization.ipynb)
  - Utilizei a biblioteca Plotly para gerar gráficos com resolução mais agradáveis e Pandas SQL para gerar as consultas e cargas das visualizações;
  - Pensei nesse formato pois na camada Gold pois e mais comum fazer todos os tratamentos pe levar para a visualização tudo já transformado e com as regas de negócio aplicadas. Então essas consultas feitas poderia ser facilmente views a partir de um Storage Analítico por exemplo Big Query ou Azure Synapse Analytics
  - O Layout da construção das visualizações é sempre: colocar o arquivo em formato DataFrame, Cria uma consulta de acordo com o Insights que deseja visualizar, fazendo os joins e transformação e por fim, com o resultado da consulta é gerado o gráfico.
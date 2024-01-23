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
1) EDA (EDA.ipynb)
  - Inicialmente foi feito uma EDA para entendimento das bases, visualizar suas colunas, datatype e tamanhos.
  - Posteriormente foi feito uma análise, foi lembrado que irá ser trabalhado com bases muito maiores, mas no exemplo as bases estão em um formato e tamanho ok, então todo o desenvolvimento foi feito utilizando Pandas. Claro, Pandas não é escalável e poderia utilizar o Pyspark. Mas dado ao problema proposto, todas as transformações feitas em Pandas aqui neste desafio podem ser modificadas para Pyspark. (Não vamos matar uma formiga com um canhão)
  -
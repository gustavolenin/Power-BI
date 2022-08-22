# Power-BI

Esse repositório contém os meus estudos referente ao curso: Microsoft Power BI Para Data Science, Versão 2.0, disponibilizado pela Data Science Academy. 

## Estudo de caso 1 (Estudo de caso 1.pbix)

Você é Analista de Dados na empresa XYZ Corporation International, uma revendedora de automóveis de luxo com sede em São Paulo. A empresa começou sua operação no Brasil em 2016 e atua nos quatro estados da região sudeste, mais os estados do Paraná e Bahia.

Seu gerente vai apresentar os resultados da equipe comercial para o novo CEO da empresa e precisa da sua ajuda para construir um Dashboard que represente os dados de vendas no período de 2016 a 2019.

Sua fonte de dados é um arquivo Excel com dados coletados do sistema de vendas e CRM da empresa, com a as seguintes colunas:



__Coluna         - Descrição__

DataNotaFiscal - Data de emissão da nota fiscal

Fabricante     - Fabricante do veículo

Estado         - Estado onde foi realizada a venda

PrecoVenda     - Preço de venda do veículo

PrecoCusto     - Preço de custo do veículo para a empresa

TotalDesconto  - Total de Desconto fornecido sobre o preço de venda

CustoEntrega   - Custo de entrega do veículo ao proprietário

CustoMaoDeobra - Custo de Mão de Obra (secretária, mecânico, etc...)

NomeCliente    - Nome do cliente que comprou o veículo

Modelo         - Modelo do veículo

Cor            - Cor do veículo

Ano            - Ano de fabricação do veículo

Seu gerente precisa das seguintes informações:

__1- Total de Vendas por Ano__

__2- Custo de Entrega do Veículo Por Fabricante__

__3- Custo de Mão de Obra Por Estado__

__4- Total de Vendas Geral e Matriz de Vendas__

Além disso, pode ser interessante, se o CEO puder visualizar o __total de vendas por estado e se as vendas estão acima ou abaixo da média__. Seu gerente já sabe que um assunto será abordado pelo CEO durante a apresentação. __O CEO está avaliando se continua ou não com a venda de automóveis da marca Jaguar e ele gostaria de saber como evoluíram as vendas de automóveis deste fabricante por ano e por estado__.
Seu trabalho é fazer isso acontecer!

## Estudo de caso 2 (Estudo de caso 2.pbix)

Você  é  Analista  de  Dados  na  empresa PontoMaximo,  uma  rede  de  varejo que  vende produtos eletrônicos e eletrodomésticos com lojas espalhadas por diversas cidades do Brasil. A empresa começou sua operação no Brasil em 2012 e atua nos quatro estados da região sudeste mais os estados do Paraná e Bahia.

A empresa está montando a estratégia de vendas para o próximo ano e precisa saber **qual dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas**. O **objetivo é descartar  os  fabricantes  cujos  produtos  possuem  poucas  vendas  e  tentar  negociar  melhores condições com os principais fabricantes**.

Em paralelo a isso, a **empresa gostaria de ter diferentes visões das vendas realizadas nos últimos 4 anos** (período de 2012 a 2015). **Deve ser possível segmentar os relatórios de vendas por  diferentes  informações  e  por diferentes  ângulos**. Estas informações irão suportar as estratégias da empresa para o próximo ano. Sua fonte de dados é um arquivo Excel com dados coletados do sistema de vendas, CRM e ERP da empresa. O conjunto de dados foi entregue pelo departamento de TI com as seguintes colunas.



**Coluna: Descrição**

ID-Produto: Identificador único de cada produto

Produto: Nome do produto

Categoria: Categoria do produto

Segmento: Segmento do produto

Fabricante: Fabricante do produto

Loja: Loja onde foi efetuada a venda

Cidade: Cidade da loja onde foi efetuada a venda

Estado: Estado da loja onde foi efetuada a venda

Vendedor: Nome do vendedor

ID-Vendedor: ID-Vendedor

DataVenda: Data da venda

ValorVenda: Valor da venda

Seu gerente precisa das seguintes informações:

__1- Qual dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas?__

__2- Qual o total de vendas por estado e por categoria? Use um mapa.__

__3- Qual o total de vendas por segmento?__

__4- Qual segmento tem maior influência no valor médio de venda?__

Haverá diversas reuniões para definição da estratégia de vendas e os relatórios poderão ser  extraídos  sob  demanda,  de  acordo  com  a  necessidade  dos  gestores. Por  conta  disso,  **você deve criar um modelo de dados que permita a extração de relatórios a qualquer momento e que permita extrair dados por diferentes visões e ângulos**. 

Seu trabalho é fazer isso acontecer!

-----------------------------------
### Desenvolvimento do Estudo de caso 2

### Passos:

**1º Passo: Modelagem de Dados**

Sabendo que o conjunto de dados estava organizado em uma única tabela, no primeiro momento foi realizada a separação em tabelas dimensão e tabela fato. Além disso, foi construído um modelo Star Schema para representar a relação entre as tabelas dimensão e a tabela fato. Para conectar estas tabelas são definidas as chaves em que as chaves primárias (PK - Primary Key) das tabelas dimensão entram como chave estrangeira (FK - Foreign Key) na tabela fato.

Uma observação importante é que no momento de construção das tabelas dimensão deve-se ter cuidado com as entradas duplicadas, neste caso foi necessária a **Limpeza dos Dados**.

<img src="https://github.com/gustavolenin/Power-BI/blob/main/Star_Schema_Estudo_de_caso_2.png" height="500" width="1200">

Em seguida, foi construído o dashboard que pode ser acessado no arquivo Estudo de caso 2.pbix

-----------------------------------

## Estudo de caso 3 (Estudo_de_caso_3.pbix)

Ainda no contexto de vendas, neste estudo de caso foi desenvolvido um dashboard guiado pelos seguintes objetivos:

__1- Qual a média de vendas por dia durante o mês de março?__

__2- Qual a margem de lucro por produto?__

__3- Qual o valor de venda e preço custo por produto?__

__4- Qual o KPI de margem de lucro?__

O dashboard está disponível em Estudo_de_caso_3.pbix.

-----------------------------------

## Dashboard Analítico - Evolução e Previsão de Desemprego ao Longo dos Anos (Dashboard Analítico - Evolução e Previsão de Desemprego ao Longo dos Anos.pbix)


**Coluna: Descrição**

Sexo: Identifica o gênero

Período: Informa a data

Range_Idade: Faixa etária

Total_Desempregados: Quantidade de desempregados

Seu gerente precisa das seguintes informações:

__1- Dashboard contendo o total de desempregados por ano, trimestre, mês e faixa etária.__

__2- O Dashboard deverá conter filtros por gênero e faixa etária.__

__3- Previsão do total de desempregados até o ano de 2022.__

O dashboard está disponível em Dashboard Analítico - Evolução e Previsão de Desemprego ao Longo dos Anos.pbix.

-----------------------------------

## Dashboard Analítico - Geolocalização de clientes por saldo bancário (Dashboard Analítico - Evolução e Previsão de Desemprego ao Longo dos Anos.pbix)


**Coluna: Descrição**

Cidade: Nome da cidade

Classificação: Categoria de classificação (baixo, médio, alto)

Data: Data 

ID Cliente: ID do cliente

Idade: Idade do cliente

Nome: Nome do cliente

Sobrenome: Sobrenome do cliente

Saldo: Saldo do cliente

Sexo: Identifica o gênero

Seu gerente precisa das seguintes informações:

__1- Dashboard contendo o saldo por cidade contendo um mapa de calor com essa informação.__

__2- O Dashboard deverá conter o saldo por idade e sexo.__

__3- Dashboard deverá conter o saldo por classificação e saldo por sexo.__

__4- Dashboard deverá conter uma segmentação por nome de cliente.__

O dashboard está disponível em Dashboard Analítico - Evolução e Previsão de Desemprego ao Longo dos Anos.pbix.

-----------------------------------

# biblioteca_pandas_dnc
Primeira análise de regressão CURSO ANALISTA DE DADOS PYTHON CURSO DNC

# Descrição:

A base de vendas contém informações sobre cada venda realizada por loja de departamento
que atua à nivel nacional, com dados como:


ID da venda
Data e hora da venda
Valor total da venda
Valor do frete
ID do cliente
ID do vendedor
ID do produto
Quantidade vendida
Preço unitário
Descontos
Impostos

Com essa base, podemos analisar o desempenho de vendas over tempo, por produto, por vendedor, por canal de venda e por região.

Alguns KPIs interessantes para essa base:


Vendas totais por dia/mês/ano
Ticket médio por venda
Vendas por produto/categoria
Vendas por vendedor/canal
Conversão de visitas em vendas
Descontos médios concedidos


Já a base de clientes traz dados cadastrais e demográficos dos clientes, como:


ID do cliente
Data de nascimento
Gênero
Cidade e estado
Renda familiar
Primeira compra
Última compra
Ticket médio
Produtos/categorias favoritas

Alguns KPIs para a base de clientes:


Novos clientes por mês
Receita por cohort de clientes
Ticket médio por idade
Preferências por estado/cidade
Taxa de retorno de compra


Podemos enriquecer nossa análise unindo as duas bases de dados através do ID de cliente, que está presente em ambas.

Isso permite correlacionar dados cadastrais e demográficos dos clientes com seus padrões de compra, para entender melhor nosso público e personalizar estratégias.

Por exemplo, podemos segmentar clientes por faixa etária e analisar diferenças de comportamento entre esses grupos em termos de:


Frequência e valor de compra
Produtos e categorias favoritas
Canal de compra preferido

Também podemos unir dados geográficos para entender diferenças regionais nas vendas e no perfil dos clientes.

A união de bases de dados relacionais é um recurso muito poderoso para enriquecer análises e obter insights de negócio.


Voltando ao contexto inicial do case, algumas métricas e KPIs foram solicitados pela loja de varejo para serem calculados ​​a partir da união das bases de vendas e clientes:

Departamentos Mais Vendidos

Podemos agrupar as vendas por departamento (categoria) e somar a receita de vendas de cada um para descobrir quais são os departamentos que geram mais receita para a loja.

Esse KPI serve para avaliar o desempenho de cada departamento e definir estratégias por categoria de produto.

Média de Preço e Frete por Departamento

Similar ao KPI anterior, podemos calcular a média de preço e frete para cada departamento, para entender a precificação e custo de entrega por categoria de produto.

Isso ajuda a moldar estratégias de preços e frete por tipo de produto.

Vendas por Mês

Um KPI simples mas essencial é a evolução das vendas por mês, para entender sazonalidades e comparar desempenho mensal ao longo do tempo.

Isso permite projetar vendas, metas e orçamentos mensais.

Média de Renda por Canal de Venda

Podemos unir os canais de venda (e-commerce, lojas físicas, televendas) com a renda média dos clientes para analisar o perfil de cada canal.

Isso ajuda a caracterizar a persona de cada canal para direcionar estratégias de marketing.

Média de Idade por Bandeira

As bandeiras de cartão (Visa, Mastercard, Elo etc.) podem segmentar tipos de cliente. Podemos calcular a idade média por bandeira para confirmar se esse padrão se repete.

Caso sim, isso permite personalizar comunicação e ofertas por bandeira de cartão.


Além dos KPIs solicitados, algumas premissas e regras do negócio foram passadas para tratamento na análise de dados:

Erro no Sistema para Estado Civil

Foi identificado um erro no sistema onde, para vendas sem informação de estado (UF), o estado está sendo preenchido automaticamente como Mato Grosso do Sul.

Essa premissa deve ser considerada na análise, tratando vendas sem UF como MT para não distorcer resultados regionais.

Validador de Preço x Frete

Outra premissa é que o preço não pode ser maior do que o preço + frete, pois isso geraria prejuízo nas vendas.


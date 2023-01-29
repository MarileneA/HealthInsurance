
![HI](https://user-images.githubusercontent.com/87071331/215324461-21d17968-acad-4988-8ec7-8e2e4d759abb.jpg)

## 1. Sobre a  Insurance All

A Insurance All é uma seguradora que vende seguros de saúde para seus clientes. O modelo de negócios de seguros funciona dessa maneira.

A seguradora exige um pagamento do cliente para garantir compensações em caso de doenças, tratamentos de saúde e quaisquer outras condições especificadas no contrato.


<p align='center'>
   
</p>

## ENTENDIMENTO DE NEGÓCIOS
## 1.1 Problema de negócio:

A Insurance All é uma seguradora de saúde e sua equipe de produtos está analisando a possibilidade de oferecer um novo produto, seguro de automóvel, para seus clientes de planos de saúde.

Semelhante ao seu seguro saúde, os clientes deste novo plano de seguro teriam que pagar um plano anual para serem segurados pela Seguros Todos em caso de eventual acidente ou dano automobilístico.

No ano passado, a Insurance All entrevistou cerca de 380.000 clientes sobre seus interesses de compra neste novo seguro automóvel. Todos os clientes nesta pesquisa tiveram uma resposta 'interessado' ou 'não interessado' a este novo produto de seguro de carro e as respostas foram armazenadas em um banco de dados juntamente com outras informações de seus clientes.

A equipe de produto escolheu 127.000 novos clientes que não responderam a última pesquisa para a nova oferta de produtos de seguro automóvel. A equipe de produtos fará essas ofertas por telefone, mas poderá realizar apenas 20.000 ligações telefônicas na campanha.

### 1.2 Objetivo
Construir um ranking por ordem de interesse (propensão de compra) dos potenciais clientes.

As seguintes questões de negócio devem ser respondidas ao gestor do call center:

- Quais são os principais insights sobre os atributos mais relevantes de clientes interessados em seguro veicular?
- Qual a porcentagem de clientes interessados em seguro veicular, o call center conseguirá contatar fazendo 20 mil ligações?
- Se a capacidade do call center aumentar para 40 mil ligações, qual a porcentagem de clientes interessados em adquirir um seguro veicular o call center conseguirá contatar?
- Quantas ligações o call center precisa fazer para contatar 80% dos clientes interessados em adquirir um seguro veicular?


## 2. Premissas de negócio
- O time de vendas já utiliza o Google Sheets como ferramenta corporativa. É preciso que o ranking de propensão de compra seja incorporado nele.

## 3. Planejamento da solução
### 3.1. Produto final
O que será entregue efetivamente?
- Uma funcionalidade dentro da ferramenta Google Sheets, que ordena os clientes (ou quaisquer novos clientes inclusos na planilha) por propensão de compra.

### 3.2. Ferramentas
Quais ferramentas serão usadas no processo?
- Python 3.8.12;
- Jupyter Notebook;
- Git, Github e Gitlab;
- Coggle Mindmaps;
- SweetViz;
- Heroku Cloud;
- Algoritmos de Regressão e Classificação;
- Pacotes de Machine Learning sklearn e xgboost;
- Técnicas de Seleção de Atributos;
- Flask e Python API's;
- Google Sheets Apps Script.

### 3.3 Processo
#### 3.3.1 Estratégia de solução
Com base no objetivo do projeto, trata-se portanto de um projeto de Learning to Rank (LTR).

Minha estratégia para resolver esse desafio, baseado na metodologia CRISP-DS, é detalhada pelo plano abaixo:

**Step 01. Data Description:**
- Coletar dados em um banco de dados na AWS Cloud.
- Compreender o significado de cada atributo dos interessados.
- Renomear colunas, compreender dimensões e tipos dos dados.
- Identificar e tratar dados nulos.
- Analisar atributos através de estatística descritiva.
- Separar 20% dos dados para teste (aleatoriamente, mas estratificados pela variável resposta).

**Step 02. Feature Engineering:**
- Criar mindmap de hipóteses de negócio.
- Realizar a feature engeneering, criando as features necessárias para validação das hipóteses.

**Step 03. Data Filtering:**
- Filtrar registros e atributos de acordo com restrições de negócio.

**Step 04. Exploratory Data Analysis:**
- Realizar uma análise univariada com uso do SweetViz, avaliando detalhes de cada atributo.
- Realizar uma análise bivariada, validando as hipóteses criadas e gerando insights de negócio.
- Criar tabela de resultados das hipóteses, e relevância estimada dos atributos para o aprendizado dos modelos.

**Step 05. Data Preparation:**
- Padronizar atributos numéricos com distribuição normal.
- Reescalar atributos numéricos com distribuição não normal.
- Codificar atributos categóricos em atributos numéricos.
- Aplicas as transformações acima aos dados de teste.

**Step 06. Feature Selection:**
- Separar dados de treino e validação.
- Rodar algoritmo para obter sugestão de atributos relevantes.
- Analisar o resultado em conjunto com os atributos relevantes estimado na EDA.
- Selecionar apenas os melhores atributos para treinar os modelos de machine learning.  

**Step 07. Machine Learning Modelling:**
- Rodar algoritmos: KNN classifier, Logistic regression, ExtraTrees classifier, e XGBboost classifier.
- Plotar curva de ganho cumulativo e lift, e calcular precison@k/recall@k de cada modelo.
- Criar tabela de performance comparando precison@k/recall@k de cada modelo.


Minha estratégia para resolver esse desafio, baseado na metodologia CRISP-DS, é detalhada pelo plano abaixo:

**Step 01. Data Description:**
- Coletar dados em um banco de dados na AWS Cloud.
- Compreender o significado de cada atributo dos interessados.
- Renomear colunas, compreender dimensões e tipos dos dados.
- Identificar e tratar dados nulos.
- Analisar atributos através de estatística descritiva.
- Separar 20% dos dados para teste (aleatoriamente, mas estratificados pela variável resposta).

**Step 02. Feature Engineering:**
- Criar mindmap de hipóteses de negócio.
- Realizar a feature engeneering, criando as features necessárias para validação das hipóteses.

**Step 03. Data Filtering:**
- Filtrar registros e atributos de acordo com restrições de negócio.

**Step 04. Exploratory Data Analysis:**
- Realizar uma análise univariada com uso do SweetViz, avaliando detalhes de cada atributo.
- Realizar uma análise bivariada, validando as hipóteses criadas e gerando insights de negócio.
- Criar tabela de resultados das hipóteses, e relevância estimada dos atributos para o aprendizado dos modelos.

**Step 05. Data Preparation:**
- Padronizar atributos numéricos com distribuição normal.
- Reescalar atributos numéricos com distribuição não normal.
- Codificar atributos categóricos em atributos numéricos.
- Aplicas as transformações acima aos dados de teste.

**Step 06. Feature Selection:**
- Separar dados de treino e validação.
- Rodar algoritmo para obter sugestão de atributos relevantes.
- Analisar o resultado em conjunto com os atributos relevantes estimado na EDA.
- Selecionar apenas os melhores atributos para treinar os modelos de machine learning.  

**Step 07. Machine Learning Modelling:**
- Rodar algoritmos: KNN classifier, Logistic regression, ExtraTrees classifier, e XGBboost classifier.
- Plotar curva de ganho cumulativo e lift, e calcular precison@k/recall@k de cada modelo.
- Criar tabela de performance comparando precison@k/recall@k de cada modelo.


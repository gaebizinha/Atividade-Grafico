# Ponderada Metabase

## Ferramenta - Metabase/ Redshift

Como ferramenta de visualização de dados utilizei o Metabase conectado ao Redshift, onde meu grupo conatruímos e armazenamos as Views. Escolhi o Metabase por ter uma interface intuitiva e permitir a crição de visualizações sem exigir conhecimento avançado em SQL. Além disso, como a plataforma possui integração com o Redshift, facilita o processamento de grandes volumes de dados.

## Configuração

Para ter acesso aos dados foi preciso estabelecer uma conexão direta entre o Metabase e o Redshift, utilizando credenciais de acesso seguras. A configuração incluiu as seguintes etapas:

1. Estabelecer a conexão com o banco de dados no Amazon Redshift.
2. Selecionar as tabelas/ views necessárias para a análise.
3. Utilizar a consulta SQL do Metabase para criar a query SQL que na tabela selecionada (cnpj_union_view_category)contabiliza  o número de vendas de Cerveja, Refrigerante e Vinho em 5 estados listados.

## Criação do gráfico

```sql
SELECT *
FROM cnpj_union_view_category
WHERE sigla_uf IN ('SP', 'MG', 'RJ', 'RS', 'BA');
```

Selecionei a View cnpj_union_view_category e indiquei que quero informações das seguintes UF (SP, MG, RJ, RS, BA).

Após rodar o SQL, fiz a escolha da visualização e selecionei as categorias de Bebidas.

Além disso selecionei a opção de “meta” para adicionar uma linha que indica a média da quantidade.

## Objetivo do gráfico

Ao analisar um gráfico pude tirar alguns insghts relevantes:

1. **Popularidade por Tipo de Bebida:**
    - Identificar qual tipo de bebida é mais popular em cada UF. .
2. **Comparação Regional:**
    - Analisar as diferenças nas preferências de bebidas entre as diferentes UFs. Isso pode indicar padrões culturais, climáticos ou econômicos que influenciam as escolhas de consumo.
3. **Correlações com Demografia:**
    - Analisar se há correlações entre o perfil demográfico de uma UF e as preferências de bebidas. Por exemplo, áreas mais jovens podem ter maior consumo de refrigerantes, enquanto áreas mais maduras podem preferir vinho.
4. **Potencial de Mercado:**
    - Identificar UFs com maior potencial de crescimento nas vendas de determinado tipo de bebida. Isso pode orientar estratégias de marketing e distribuição.
5. **Ajustes na Estratégia de Estoque:**
    - Utilizar as informações para otimizar os estoques de acordo com as preferências regionais, evitando excesso ou escassez de determinados tipos de bebida.
6. **Comparação com Médias Nacionais:**
    - Comparar as vendas nas UFs com as médias nacionais pode revelar se uma região tem um consumo atípico em relação ao país como um todo.

<div align="center">
<img src="https://github.com/gaebizinha/Atividade-Grafico/blob/main/Untitled.png" width="900"/> <br>
</div>

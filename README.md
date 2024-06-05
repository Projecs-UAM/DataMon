
# DataMon

## Descrição do Projeto
Este projeto é uma análise descritiva realizada para a atividade A3 da UC Análises Descritivas e Modelos Analíticos para problemas de negócios.

### Integrantes
- Gustavo Corrêa Mendes - RA: 1292225707
- Vinicius Pereira de Sousa - RA: 12523163043
- Beatriz freitas monteiro - RA: 125111356183
- Vinícius Marques de Souza - RA: 12523130849
- Rubens de Jesus Souza - RA: 11585272841

## Requisitos do Projeto

1. Carregar e ler arquivos: .csv, .xlsx ou diretamente de um banco de dados.

2. Transformação de variáveis: Avaliar a necessidade de transformar variáveis para outras escalas (exemplo: agrupar idade por faixas).

3. Codificação de variáveis categóricas: Utilizar técnicas como label encoder, one hot encoder ou target encoder.

4. Normalização das variáveis.

5. Balanceamento da variável alvo: Avaliar a necessidade de balanceamento.

6. Tratamento de variáveis com alta correlação.

7. Seleção de variáveis.

8. Modelagem: Aplicar um modelo de regressão ou 9. classificação utilizando técnicas de hiperparametrização automática.

9. Avaliação do modelo: Aplicar medidas de avaliação do modelo.

10. Visualização dos resultados:
- Agrupamento: Gerar visualização Scatter.
- Classificação: Gerar matriz de confusão.
- Regressão: Gerar visualização da linha de saída.

## Base de Dados

A base de dados utilizada contém informações sobre Pokémons. As colunas presentes na base bruta são:

- "#": Identificação da linha – Tipo Int
- Name: Nome dos Pokémons – Tipo String
- Type 1: Primeiro tipo dos Pokémons – Tipo String
- Type 2: Segundo tipo dos Pokémons (se houver) – Tipo String
- Total: Variável de poder do Pokémon – Tipo Int
- HP: Quantidade de vida do Pokémon – Tipo Int
- Attack: Valor de ataque do Pokémon – Tipo Int
- Defense: Valor de defesa do Pokémon – Tipo Int
- Sp. Atak: Valor de ataque especial do Pokémon – Tipo Int
- Sp. Def: Valor de defesa especial do Pokémon – Tipo Int
- Speed: Velocidade do Pokémon – Tipo Int
- Generation: Geração à qual o Pokémon pertence – Tipo Int
- Legendary: Indica se o Pokémon é lendário – Tipo String (True/False)

[Base utilizada no projeto](https://raw.githubusercontent.com/Projecs-UAM/DataMon/main/Pokemon.csv)

## Ferramentas Utilizadas

Para a análise, foram utilizadas as seguintes bibliotecas:

#### Para tratamento de dados desbalanceados:
- [Imbalanced-learn](https://imbalanced-learn.org/stable/)

#### Para modelos de machine learning:
- [Scikit-learn](https://scikit-learn.org/stable/index.html)

#### Para avaliação de previsões:
- [ppscore](https://pypi.org/project/ppscore/)

#### Para visualização de dados:
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)





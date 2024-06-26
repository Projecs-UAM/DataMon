
# DataMon

## Descrição do Projeto
Este projeto é uma análise descritiva realizada para a atividade A3 da UC Análises Descritivas e Modelos Analíticos para problemas de negócios.

### Integrantes
- Gustavo Corrêa Mendes - RA: 1292225707
- Vinicius Pereira de Sousa - RA: 12523163043
- Beatriz freitas monteiro - RA: 125111356183
- Vinícius Marques de Souza - RA: 12523130849
- Rubens de Jesus Souza - RA: 125111345885

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

<img src="image\Blibio.png">

## Carregamento da Base de Dados

Após importar as bibliotecas necessárias, carregamos a base de dados para iniciar a análise.

- [Base utilizada no projeto](https://raw.githubusercontent.com/Projecs-UAM/DataMon/main/Pokemon.csv)


<img src="image\BaseLoad.png">

### Avaliar a necessidade da transformação da variável em outra escala (agrupar idade por faixas, por exemplo)

Não vimos necessidade de escalar as variáveis, pois o dataset é pequeno e autoexplicativo.

<img src="image\Avaliar.png">

### Ralizando a codificação das variáveis categóricas de acordo com os valores das variáveis (label encoder, one hot encoder ou target encoder)

<img src="image\Realizar.png">

### Normalizar as variáveis

<img src="image\Normalizar1.png">

<img src="image\Normalizar2.png">

<img src="image\Normalizar3.png">

<img src="image\Normalizar4.png">

<img src="image\Normalizar 5.png">

<img src="image\Normalizar6.png">

Analisando a discrepância dos dados usando porcentagem, assim teremos um melhor insight sobre a distribuição dos dados e o que fazer com eles.

<img src="image\Analisando.png">

Deletando as colunas do tipo string para que possamos aplicar o SMOTE.

<img src="image\Deletando.png">

### SMOTE - Synthetic Minority Over-sampling Technique

Cria cópias sintéticas (não existentes) dos Pokémons lendários para equilibrar as classes.

<img src="image\Smote1.png">

<img src="image\Smote2.png">

<img src="image\Smote3.png">

## Aplicando os modelos SVM e KNN e testando a sua acurácia, precisão e revocação.

### SVM - Support Vector Machine

<img src="image\SVM.png">

### KNN - K-Nearest Neighbors

<img src="image\knn.png">

### Tratar variáveis com alta correlação

<img src="image\Tratar1.png">

<img src="image\Tratar2.png">

<img src="image\Tratar3.png">

<img src="image\Tratar4.png">

Com esse gráfico, notamos que há pouca correlação entre as variáveis, o que é bom para o modelo. Não será necessário remover ou tratar nenhuma variável.

Lembrando que a leitura desse gráfico se dá pelo seguinte:

- Quanto mais próximo de 1, mais forte é a correlação positiva entre as variáveis; algo ruim 

- Quanto mais próximo de -1, mais forte é a correlação negativa entre as variáveis; - também é algo ruim

- Quanto mais próximo de 0, mais fraca é a correlação entre as variáveis. - algo bom

Variáveis com alta correlação ou correlação invertida podem ser um problema para o modelo, pois ele não saberá qual variável é mais importante para a previsão, além de que o modelo também não consegue analisar a importância da individualidade da classe. Isso pode causar overfitting, ou seja, o modelo se ajusta muito bem aos dados de treino, mas não consegue generalizar para novos dados.

<img src="image\Variaveis.png">

### Plotagem de dados, Scatter, Matriz de confusão e Linha de saída.

<img src="image\Plotagem1.png">

<img src="image\Plotagem2.png">

<img src="image\Plotagem3.png">


Esse nosso modelo não ficou muito bom, pois ele não conseguiu prever corretamente os pokemons lendários, o que é o nosso foco. Talvez seja por conta da quantidade de dados, ou por conta da quantidade de variáveis que não são tão relevantes para a previsão.

<img src="image\Modelo1.png">

<img src="image\Modelo2.png">

<img src="image\Modelo3.png">

## Agora, sim, o modelo conseguiu prever corretamente os pokemons lendários, o que é o nosso foco.

 Porém lembrando, que o RandomUnderSampling é uma técnica que descarta dados, então, não é a melhor técnica para ser usada, dependendo do caso.

Se isso não for levado em consideração, seu modelo por sofrer de overfitting, ou seja, ele se ajusta muito bem aos dados de treino, mas não consegue generalizar para novos dados.

## Regressão Linear com linha de saída

<img src="image\Regressao1.png">

<img src="image\Regressao2.png">

<img src="image\Regressao3.png">

## Conclusão

O modelo de regressão linear não foi o melhor para prever se um pokémon é lendário ou não, pois ele não consegue prever valores binários, ou seja, 0 ou 1 (Lendário, não lendário). Ele é mais indicado para prever valores contínuos, como preço de casas, por exemplo.

O ideal seria que as linhas azuis e vermelhas estivessem o mais próximas possíveis, mas como podemos ver, há uma grande discrepância entre elas, o que indica que o modelo não foi eficaz. O modelo anterior fez muito melhor.

Enfim, aprendizados.

<img src="image\Conclusao.png">

Aqui vemos que as variáveis que mais dizem algo relevante, onde há mais discrepâncias e dados valiosos estão nas colunas "total", "sp_atq" (superataque), "sp_def" (superdefesa) e "velocidade"
Essa seleção de variáveis abre margem para novas análises e insights, como por exemplo, ver qual tipo de pokemon contém os maiores valores em cada uma dessas variáveis, ou até mesmo, ver se há alguma relação entre essas variáveis e a geração do pokemon, ou coisa parecida.
# Classificação de Vinhos com Machine Learning

Projeto introdutório de aprendizado de máquina supervisionado em Python, criado para praticar o fluxo básico de um projeto de ML: conhecer os dados, separar treino e teste, treinar modelos, avaliar e interpretar os resultados.

## Objetivo

Prever o tipo de um vinho (3 classes) a partir de 13 medidas químicas e comparar o desempenho de dois modelos de classificação.

## Dados

Conjunto público *Wine*, incluído na biblioteca scikit-learn: 178 amostras, 13 características e 3 classes. Nenhum arquivo externo é necessário.

## Etapas

1. Carregamento e exploração dos dados com pandas.
2. Separação em treino (80%) e teste (20%), mantendo a proporção das classes.
3. Treinamento de dois modelos: Regressão Logística (com padronização das medidas) e Random Forest.
4. Avaliação por acurácia no conjunto de teste e por validação cruzada (5 partes).
5. Análise dos erros com matriz de confusão e relatório de classificação.
6. Importância das características no Random Forest.

## Resultados

| Modelo | Acurácia no teste | Validação cruzada (média ± desvio) |
| --- | --- | --- |
| Regressão Logística | 0,972 | 0,983 ± 0,014 |
| Random Forest | 1,000 | 0,967 ± 0,021 |

- No conjunto de teste (36 amostras), o Random Forest classificou todos os vinhos corretamente, como mostra a matriz de confusão.
- Na validação cruzada, a Regressão Logística teve média um pouco maior, então os dois modelos têm desempenho muito parecido.
- Medidas mais importantes para o Random Forest: intensidade da cor (`color_intensity`), flavonoides (`flavanoids`), prolina (`proline`), álcool (`alcohol`) e tonalidade (`hue`).

## Aprendizados

- Separar treino e teste evita avaliar o modelo com dados que ele já viu.
- Um conjunto de teste pequeno (36 amostras) dá resultados instáveis; a validação cruzada repete a avaliação cinco vezes e é uma medida mais confiável.
- Comparar mais de um modelo e olhar a matriz de confusão ajuda a entender onde o modelo acerta e erra, e não apenas a acurácia final.

## Tecnologias

Python, pandas, scikit-learn, matplotlib, Google Colab.

## Como executar

1. Abra https://colab.research.google.com e escolha Arquivo > Fazer upload de notebook.
2. Envie o arquivo `classificacao_vinhos.ipynb`.
3. Clique em Ambiente de execução > Executar tudo.

## Observação

Projeto de estudo, desenvolvido com apoio de ferramentas de IA generativa.

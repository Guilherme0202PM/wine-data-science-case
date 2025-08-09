# Análise de Qualidade de Vinhos

Projeto de análise exploratória de dados para classificação de qualidade de vinhos tintos utilizando propriedades físico-químicas.

## Objetivo do Projeto

Este projeto tem como objetivo analisar um dataset de vinhos tintos com 11 características físico-químicas para predizer a qualidade dos vinhos. A análise transforma as notas originais de qualidade (0-10) em um problema de classificação binária (vinhos bons vs ruins) e fornece insights para tomada de decisão em negócios de distribuição de vinhos.

## Dataset

- **Fonte**: UCI Machine Learning Repository
- **Amostras**: 1.599 observações de vinhos tintos
- **Características**: 11 propriedades físico-químicas
- **Target**: Nota de qualidade (0-10), transformada para classificação binária
- **Formato**: Arquivo CSV (`winequality-red.csv`)

### Descrição das Variáveis

| Variável | Descrição |
|----------|-----------|
| fixed acidity | Acidez fixa - ácido tartárico (g/dm³) |
| volatile acidity | Acidez volátil - ácido acético (g/dm³) |
| citric acid | Ácido cítrico (g/dm³) |
| residual sugar | Açúcar residual após fermentação (g/dm³) |
| chlorides | Cloretos - cloreto de sódio (g/dm³) |
| free sulfur dioxide | Dióxido de enxofre livre (mg/dm³) |
| total sulfur dioxide | Dióxido de enxofre total (mg/dm³) |
| density | Densidade do vinho (g/cm³) |
| pH | Nível de acidez (escala 0-14) |
| sulphates | Sulfatos - sulfato de potássio (g/dm³) |
| alcohol | Percentual de álcool (% vol) |

## O que foi Feito

### Análise Exploratória Completa
- **Carregamento e análise inicial** dos dados
- **Estatísticas descritivas** de todas as variáveis
- **Visualizações** das distribuições e padrões
- **Detecção de outliers** usando métodos Z-Score e IQR
- **Análise de correlações** entre variáveis
- **Transformação do target** para classificação binária otimizada
- **Testes estatísticos** para validar diferenças entre grupos
- **Análise de separabilidade** das classes

### Principais Descobertas
- Dataset completo sem valores ausentes
- Classes balanceadas após transformação binária (bom: 53.4%, ruim: 46.6%)
- Múltiplas variáveis com diferenças estatisticamente significativas entre classes
- Classes parcialmente separáveis com sobreposição moderada
- Viabilidade confirmada para modelos de machine learning

## Tecnologias Utilizadas

- **Python 3.8+**
- **pandas** - Manipulação e análise de dados
- **numpy** - Computações numéricas
- **matplotlib** - Visualização de dados
- **seaborn** - Visualizações estatísticas
- **scipy** - Testes estatísticos
- **jupyter** - Ambiente de desenvolvimento interativo

## Técnicas Aplicadas

### Análise Estatística
- Estatísticas descritivas (média, mediana, quartis, desvio padrão)
- Análise de correlação (Pearson e Spearman)
- Testes de hipótese (t-test de Welch, Mann-Whitney U)
- Cálculo de effect size (Cohen's d)

### Detecção de Outliers
- Método Z-Score (3 desvios padrão)
- Método IQR (Interquartile Range)
- Análise comparativa dos métodos

### Visualização de Dados
- Histogramas e distribuições
- Boxplots por classe
- Scatterplots e pairplots
- Matrizes de correlação (heatmaps)
- Gráficos de densidade

### Transformação de Dados
- Discretização otimizada da variável target
- Análise de balanceamento de classes
- Criação de variáveis categóricas

## Algoritmos Recomendados

Com base na análise realizada, os seguintes algoritmos são recomendados:

1. **Random Forest** - Robusto a outliers, fornece importância das features
2. **Gradient Boosting** - Alta performance para classificação complexa
3. **Regressão Logística** - Modelo baseline interpretável
4. **SVM** - Efetivo para relações não-lineares
5. **Decision Tree** - Altamente interpretável para negócios

## Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/analise-qualidade-vinhos.git
cd analise-qualidade-vinhos
```

2. Instale as dependências:
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

3. Execute a análise:
```bash
jupyter notebook
```

## Próximos Passos

1. **Preparação dos dados** com train-test split
2. **Feature engineering** e seleção de variáveis
3. **Desenvolvimento de modelos** com os algoritmos recomendados
4. **Otimização** de hiperparâmetros
5. **Avaliação** de performance e interpretabilidade

## Citação do Dataset

P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. Modeling wine preferences by data mining from physicochemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.

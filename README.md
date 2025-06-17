# Predição de Preços de Imóveis na Califórnia - Pipeline Completo de Machine Learning

## 📋 Sobre o Projeto

Este projeto implementa um pipeline completo de Machine Learning para predição de preços de imóveis utilizando o dataset **California Housing Prices**. O trabalho foi desenvolvido como atividade avaliativa da disciplina de Aprendizagem de Máquina, contemplando desde a análise exploratória dos dados até a implementação de modelos preditivos otimizados.

## 👥 Equipe

- **ANA IARA LOAYZA COSTA**
- **JOSE VICTOR BRITO COSTA**
- **AILTON KAYKY CORDEIRO DA SILVA**
- **MILENA FREIRE BRITTO NEVES**
- **RAFAEL FREITAS DE PAULA**

## 🎯 Objetivos

- Desenvolver um sistema completo de predição de preços imobiliários
- Implementar e comparar diferentes algoritmos de Machine Learning
- Criar pipelines de pré-processamento e transformação de dados
- Otimizar hiperparâmetros e validar modelos
- Avaliar performance através de métricas adequadas

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** - Manipulação e análise de dados
- **NumPy** - Computação numérica
- **Scikit-learn** - Algoritmos de Machine Learning
- **Matplotlib** - Visualização de dados
- **Jupyter Notebook** - Ambiente de desenvolvimento

## 📊 Dataset

O projeto utiliza o dataset **California Housing Prices**, que contém informações sobre:
- Localização geográfica (longitude, latitude)
- Características demográficas (idade mediana, renda mediana)
- Características habitacionais (total de quartos, total de cômodos)
- Proximidade ao oceano
- Valor mediano das casas (variável target)

## 🔧 Estrutura do Pipeline

### 1. **Carregamento e Exploração dos Dados**
- Download automático do dataset
- Análise exploratória inicial
- Visualização de distribuições e correlações

### 2. **Divisão Estratificada dos Dados**
- Criação de estratos baseados na renda mediana
- Divisão treino/teste mantendo proporções representativas

### 3. **Engenharia de Features**
- Criação de features combinadas:
  - `rooms_per_household`
  - `bedrooms_per_room`
  - `population_per_household`

### 4. **Pipeline de Transformação**
- Tratamento de valores ausentes (SimpleImputer)
- Transformador customizado para features combinadas
- Padronização de variáveis numéricas (StandardScaler)
- Codificação one-hot para variáveis categóricas

### 5. **Modelos Implementados**
- **Regressão Linear** - Baseline
- **Árvore de Decisão** - Modelo não-linear
- **Random Forest** - Ensemble method

### 6. **Validação e Otimização**
- Validação cruzada (10-fold)
- Grid Search para otimização de hiperparâmetros
- Randomized Search para comparação
- Análise de importância das features

## 📈 Resultados

### Métricas de Avaliação
- **RMSE (Root Mean Square Error)** - Erro quadrático médio
- **MAE (Mean Absolute Error)** - Erro absoluto médio
- **R² Score** - Coeficiente de determinação

### Performance dos Modelos
| Modelo | RMSE (CV) | Status |
|--------|-----------|---------|
| Regressão Linear | ~$68,628 | Underfitting |
| Árvore de Decisão | ~$70,094 | Overfitting |
| Random Forest | ~$49,899 | Melhor Performance |
| RF Otimizado | ~$47,730 | Modelo Final |

### Features Mais Importantes
1. **median_income** - Renda mediana
2. **bedrooms_per_room** - Quartos por cômodo
3. **population_per_household** - População por domicílio
4. **rooms_per_household** - Cômodos por domicílio
5. **housing_median_age** - Idade mediana das casas

## 🚀 Como Executar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/california-housing-ml-pipeline.git
   cd california-housing-ml-pipeline
   ```

2. **Instale as dependências:**
   ```bash
   pip install pandas numpy scikit-learn matplotlib jupyter
   ```

3. **Execute o notebook:**
   ```bash
   jupyter notebook california-housing-ml-pipeline.ipynb
   ```

## 📁 Estrutura do Repositório

```
california-housing-ml-pipeline/
│
├── README.md                 # Este arquivo
├── california-housing-ml-pipeline.ipynb           # Notebook principal com todo o pipeline
└── images/                  # Pasta gerada automaticamente para visualizações
    └── end_to_end_project/  # Gráficos salvos durante a execução
```

## 📝 Principais Características do Código

- **Código totalmente comentado** para facilitar compreensão
- **Pipeline modular** e reutilizável
- **Reprodutibilidade** garantida através de seeds fixas
- **Tratamento robusto** de dados ausentes
- **Visualizações informativas** salvas automaticamente
- **Avaliação rigorosa** com múltiplas métricas

## 🔍 Insights e Conclusões

1. **Random Forest** demonstrou ser o algoritmo mais adequado para este problema
2. **Renda mediana** é o fator mais determinante no preço dos imóveis
3. **Features engenheiradas** contribuem significativamente para a performance
4. **Localização geográfica** tem impacto importante nos preços
5. O modelo final atinge **R² de ~0.67**, indicando boa capacidade preditiva

## 📚 Aprendizados

Este projeto proporcionou experiência prática em:
- Desenvolvimento de pipelines completos de ML
- Técnicas de pré-processamento e feature engineering
- Comparação e validação de diferentes algoritmos
- Otimização de hiperparâmetros
- Interpretação de resultados e métricas

## 🛡️ Licença

Este projeto foi desenvolvido para fins acadêmicos como parte da disciplina de Aprendizagem de Máquina.

---

**Desenvolvido com 💙 pela equipe para a Atividade da Unidade I**

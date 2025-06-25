# Análise Agrícola com Machine Learning e Streamlit 🌾

Este projeto oferece uma plataforma interativa e amigável construída com **Streamlit** para explorar um dataset simulado de produção agrícola e aplicar um modelo de Machine Learning para realizar previsões. Ele foi desenvolvido para demonstrar capacidades de Análise Exploratória de Dados (EDA) e modelagem preditiva em um contexto agrícola.

---

## 🎯 Objetivo

O principal objetivo deste aplicativo é:

- Fornecer uma interface intuitiva para a exploração de dados agrícolas simulados, permitindo visualizar distribuições, relações e correlações entre variáveis climáticas, tipo de solo, fertilizantes e produção.
- Demonstrar a aplicação de um modelo de Machine Learning (Regressão) para prever a produção agrícola com base em diferentes variáveis de entrada.
- Servir como um ponto de partida para projetos de análise de dados e modelagem preditiva no setor agrícola.

---

## ✨ Funcionalidades

O aplicativo é dividido em duas seções principais, acessíveis através da barra lateral:

### 1. Exploração de Dados

Nesta seção, você pode realizar uma análise exploratória aprofundada do dataset simulado de produção agrícola:

- **Visão Geral dos Dados:** Exibe os primeiros registros, dimensões do DataFrame, tipos de dados e verifica valores ausentes.
- **Estatísticas Descritivas:** Apresenta um resumo estatístico das variáveis numéricas.
- **Análise Univariada:** Mostra histogramas e box plots para variáveis numéricas (Temperatura, Precipitação, Umidade, Produção) e distribuições para variáveis categóricas (Fertilizante, Tipo de Solo).
- **Análise Bivariada:** Exibe gráficos de dispersão entre pares de variáveis numéricas, coloridos e com símbolos baseados em variáveis categóricas, além de violino plots para entender a distribuição da Produção por Fertilizante e Tipo de Solo.
- **Análise de Correlação:** Apresenta um mapa de calor de correlação entre as variáveis numéricas.
- **Análise Multivariada:** Inclui um pair plot para visualizar as relações entre múltiplas variáveis.
- **Análise Interativa:** Permite que o usuário selecione variáveis para criar gráficos de dispersão personalizados.

### 2. Modelagem Preditiva

Esta seção foca na aplicação de Machine Learning para prever a produção:

- **Filtro de Dados:** Permite filtrar os dados com base em fertilizante, tipo de solo e intervalos para temperatura, precipitação e umidade antes de treinar o modelo.
- **Preparação dos Dados:** Transforma variáveis categóricas em variáveis dummies para uso no modelo.
- **Treinamento do Modelo:** Treina um modelo de Regressão Random Forest (`RandomForestRegressor`) nos dados filtrados e exibe a acurácia (R²) no conjunto de teste.
- **Previsões:** Permite ao usuário inserir novos valores para temperatura, precipitação, umidade, tipo de fertilizante e solo para obter uma previsão instantânea da produção agrícola.

---

## 🛠️ Tecnologias Utilizadas

- Python
- Streamlit: Para a criação da interface web interativa.
- Pandas: Para manipulação e análise de dados.
- NumPy: Para operações numéricas.
- Matplotlib: Para visualização de dados (mapa de calor).
- Seaborn: Para visualização estatística (pair plot).
- Plotly Express: Para gráficos interativos.
- Scikit-learn: Para implementação do modelo de Machine Learning (`RandomForestRegressor`).

---

## 📁 Estrutura do Projeto

- `app.py`: Ponto de entrada principal do aplicativo Streamlit, responsável por configurar a navegação entre as páginas.
- `Exploracao_de_dados.py`: Código e interface para a seção de Análise Exploratória de Dados.
- `2_Modelagem_Preditiva.py`: Código e interface para a seção de Modelagem Preditiva.
- `data_generation.py`: Script auxiliar para gerar o dataset simulado de produção agrícola utilizado no aplicativo.

---

## 🚀 Como Rodar o Projeto Localmente

Siga os passos abaixo para configurar e executar o projeto em sua máquina local:

### Pré-requisitos

- Python 3.7+ instalado em seu sistema.

### 1. Clonar o Repositório

```bash
git clone https://github.com/leoalvsmag/project-ml-streamlit.git
cd project-ml-streamlit
```

### 2. Criar e Ativar um Ambiente Virtual

Recomenda-se usar um ambiente virtual para gerenciar as dependências:

```bash
python -m venv venv
```

- No Windows:

```bash
.env\Scriptsctivate
```

- No macOS/Linux:

```bash
source venv/bin/activate
```

### 3. Instalar as Dependências

Crie um arquivo `requirements.txt` na raiz do projeto com o conteúdo abaixo:

```
streamlit
pandas
numpy
matplotlib
seaborn
plotly
scikit-learn
```

Depois, instale as dependências:

```bash
pip install -r requirements.txt
```

### 4. Executar o Aplicativo Streamlit

```bash
streamlit run app.py
```

O aplicativo será aberto automaticamente no seu navegador padrão, geralmente em [http://localhost:8501](http://localhost:8501).

---

Obrigado por visitar o projeto! 🌱🚜

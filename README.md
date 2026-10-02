# 🔥 Análise de Queimadas no Brasil com Dados de Satélite da NASA

Projeto de Data Science desenvolvido para analisar focos de incêndio detectados por satélites da NASA no território brasileiro, utilizando Python, estatística descritiva e técnicas de análise exploratória de dados.

O objetivo foi transformar uma base com mais de 850 mil registros em informações capazes de auxiliar na compreensão da intensidade, distribuição e comportamento dos focos de incêndio.

## 📌 Sobre o projeto

Incêndios florestais geram impactos ambientais, sociais e econômicos, afetando biodiversidade, agricultura, saúde pública e populações próximas às regiões atingidas.

Neste projeto, foram utilizados dados provenientes da plataforma NASA FIRMS/Earthdata para investigar padrões relacionados aos focos de calor registrados no Brasil.

**Período analisado:** 25/05/2025 a 25/05/2026  
**Total analisado:** 853.047 registros de focos de incêndio

## 🎯 Objetivos

- Realizar limpeza e preparação dos dados;
- Aplicar técnicas de estatística descritiva;
- Analisar medidas de tendência central e dispersão;
- Investigar quartis e percentis;
- Detectar valores extremos utilizando o método IQR;
- Analisar a distribuição da intensidade dos incêndios;
- Investigar relações entre variáveis térmicas;
- Criar visualizações para facilitar a interpretação dos resultados;
- Extrair insights relevantes a partir dos dados.

## 🛠️ Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- Jupyter Notebook

## 📊 Principais variáveis

- `latitude` e `longitude` — localização geográfica;
- `brightness` — brilho térmico detectado pelo satélite;
- `bright_t31` — temperatura registrada pelo sensor infravermelho;
- `frp` — Fire Radiative Power, indicador da potência radiativa do fogo;
- `acq_date` e `acq_time` — data e horário da detecção;
- `daynight` — identificação de registros diurnos e noturnos;
- `satellite` — satélite responsável pela detecção;
- `confidence` — nível de confiança da detecção.

## 🔎 Etapas da análise

### 1. Preparação dos dados

A base foi inspecionada para identificar sua estrutura, valores ausentes, possíveis registros duplicados e necessidades de padronização.

### 2. Estatística descritiva

Foram analisadas medidas como média, mediana, moda, desvio padrão, amplitude, coeficiente de variação, quartis e percentis.

### 3. Detecção de outliers

Foi utilizado o método **IQR (Intervalo Interquartil)** para identificar valores extremos, principalmente na variável `frp`.

### 4. Visualização dos dados

Foram utilizados histogramas, boxplots, gráficos de barras, scatterplots e heatmap de correlação para explorar os dados e comunicar os resultados.

## 💡 Principais insights

A análise mostrou que a variável **FRP (Fire Radiative Power)** possui elevada dispersão.

Enquanto a média encontrada foi aproximadamente **10,86**, a mediana foi **5,52**, e foram observados registros superiores a **2.000**.

O coeficiente de variação do FRP foi aproximadamente **193,84%**, evidenciando grande heterogeneidade na intensidade dos focos registrados.

Também foi identificada uma relação positiva entre variáveis térmicas:

- `brightness` × `bright_t31`: correlação de aproximadamente **0,58**;
- `brightness` × `frp`: aproximadamente **0,32**;
- `bright_t31` × `frp`: aproximadamente **0,37**.

Esses resultados indicam associação positiva entre os indicadores térmicos analisados e a potência radiativa registrada nos focos de calor.

## 🌎 Aplicação dos dados

O projeto demonstra como dados obtidos por satélites podem contribuir para:

- Monitoramento ambiental;
- Identificação de eventos extremos;
- Análise de padrões de queimadas;
- Apoio a estudos de prevenção de desastres;
- Geração de informações para tomada de decisão.

O trabalho também explora a aplicação de dados e infraestrutura espacial na análise de fenômenos terrestres.

## ⚠️ Limitações

Os dados representam focos de calor detectados por sensores de satélite. Portanto, a análise permite identificar padrões nos registros e em seus indicadores térmicos, mas não determina diretamente a causa específica de cada incêndio.

## 📁 Estrutura planejada do projeto

```text
nasa-brazil-wildfires-analysis/
│
├── README.md
├── notebooks/
│   └── nasa_wildfires_analysis.ipynb
│
├── data/
│   └── README.md
│
└── images/
    └── visualizações da análise
```

## 🎓 Contexto acadêmico

Projeto desenvolvido por **Gabriel Cardoso** durante a graduação em **Engenharia de Software na FIAP**, aplicando conceitos de Data Science, estatística e análise exploratória de dados a um problema real.

## 📚 Fonte dos dados

Os dados utilizados foram obtidos através da plataforma **NASA FIRMS (Fire Information for Resource Management System)**.

Devido ao tamanho da base original, o arquivo CSV não será armazenado diretamente neste repositório. As instruções para obtenção e utilização dos dados serão disponibilizadas na pasta `data/`.

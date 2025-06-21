# Projeto Final - Módulo 04  
## Análise Exploratória de Dados de Dengue em Manaus (2023-2025)

---

## Autores  
- Ademir Guimarães  
- Kevin Gomes
- Pedro Carvalho  

## Data de Conclusão  
19 de junho de 2025

---

## Objetivo do Projeto  
Este projeto teve como objetivo principal realizar uma análise exploratória aprofundada dos dados de notificação de dengue em Manaus, enriquecendo-os com informações demográficas, geográficas e climáticas. A análise busca fornecer insights cruciais para que órgãos públicos otimizem a alocação de recursos, direcionem campanhas de prevenção e atuem de forma mais eficaz no combate ao mosquito *Aedes aegypti*.

---

## Perguntas Analíticas  

- **P1:** Quais bairros e zonas administrativas concentram o maior número de casos de dengue?  
- **P2:** A análise da taxa de incidência por habitante muda a perspectiva sobre os bairros de maior risco?  
- **P3:** Como os casos de dengue evoluíram ao longo do tempo e existe um padrão de sazonalidade evidente?  
- **P4:** Como os casos se distribuem geograficamente pela cidade de Manaus?  
- **P5:** Existe correlação entre variações climáticas, como temperatura e precipitação, e a sazonalidade dos casos de dengue em Manaus?  

---

## Coleta e Pré-processamento de Dados  

### Fontes de Dados  
- **Notificações de Dengue:** Sistema de Informação de Agravos de Notificação (SINAN), Ministério da Saúde  
- **Dados Climáticos:** Instituto Nacional de Meteorologia (INMET) - estação Manaus  
- **Dados Geográficos e Populacionais:** Shapefiles e dados do censo do IBGE  

### Tratamento dos Dados  
1. Filtragem das notificações apenas para o município de Manaus (código IBGE 130260)  
2. Enriquecimento dos dados por CEP, utilizando API ViaCEP para padronização dos nomes de bairros  
3. Junção dos dados de notificação com informações populacionais e geográficas dos bairros  

**Total de notificações analisadas:** 3.774 casos em Manaus (2023 a 2024 + parcial 2025)

---

## Principais Resultados da Análise Exploratória (EDA)  

### P1: Bairros com maior número absoluto de casos  
- Tarumã, São Raimundo e Centro concentram o maior número absoluto de notificações.  
- Confirmação visual por mapas de calor das notificações.

### P2 e P4: Distribuição geográfica e taxa de incidência  
- A análise por taxa de incidência (casos por 100.000 habitantes) altera a percepção de risco.  
- Alguns bairros com menor número absoluto apresentam alta taxa de incidência quando a população é considerada.

### P3: Evolução temporal e sazonalidade  
- Séries temporais apresentam flutuações diárias.  
- Média móvel de 7 dias evidencia tendências e padrões sazonais.  
- Pico claro de casos em janeiro de 2024, indicando momento crítico.

### P5: Correlação com variações climáticas  
- Evidência visual de correlação entre aumento de temperatura e aumento posterior dos casos de dengue.  
- Defasagem temporal de 2 a 3 meses entre pico de temperatura e pico de casos.  
- Período quente entre setembro e outubro de 2023 precedeu maior surto em janeiro de 2024.  
- Monitoramento climático é essencial para previsão e prevenção.

---

## Conclusão  
Esses resultados indicam que a dinâmica dos casos de dengue em Manaus é complexa e provavelmente influenciada por múltiplos fatores além do clima, como:

Infraestrutura urbana (escoamento de água, saneamento)

Condições socioeconômicas

Ações de combate e controle do mosquito

Ciclos sazonais de imunidade da população

---

## Estrutura do Repositório  

O repositório é organizado da seguinte forma:

- `datalake/`: Pasta contendo os arquivos de dados brutos utilizados no projeto.  
- `download_data.ipynb`: Notebook responsável por baixar e carregar os dados.  
- `processing_data.ipynb`: Notebook dedicado ao processamento e limpeza dos dados.  
- `visualize_data.ipynb`: Notebook para análise exploratória e visualização dos dados.  
- `requirements.txt`: Arquivo que lista as dependências necessárias para executar os notebooks.  

---

## Requisitos  

Para executar os notebooks localmente, é necessário ter o Python 3.11 instalado. Além disso, as dependências podem ser instaladas utilizando o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt

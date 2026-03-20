# EDA — Admissão em Programas de MBA

Análise exploratória de dados aplicada ao processo seletivo de um programa de MBA, com foco na identificação dos fatores associados à admissão e na investigação de equidade entre perfis de candidatos.


## Objetivo

Identificar quais variáveis — acadêmicas, profissionais e demográficas — estão associadas à decisão de admissão, e verificar se há disparidades estatisticamente significativas entre grupos de candidatos.


## Perguntas de negócio

1. Qual é o perfil dos candidatos admitidos?
2. GPA e GMAT são os principais determinantes da admissão?
3. Há diferença significativa nas taxas de admissão entre gêneros?
4. A experiência profissional influencia a admissão de forma diferente para homens e mulheres?
5. Existem evidências de disparidade no processo seletivo?


## Estrutura da análise

| Seção | Conteúdo |
|---|---|
| Carregamento | Leitura do CSV, visão geral do dataset |
| Tratamento | Renomeação de colunas, tradução de valores, nulos e duplicatas |
| Análise descritiva | Estatísticas gerais, distribuição das variáveis |
| Análise univariada | Distribuição de GPA, GMAT, experiência, gênero, setor |
| Análise bivariada | Cruzamentos com a variável `admissao` |
| Testes de hipótese | Teste t, teste z de proporções, qui-quadrado |
| Correlações | Pearson e Spearman entre variáveis numéricas |
| Síntese | Principais achados e considerações finais |

---

## Principais achados

- Candidatas do gênero **feminino** apresentaram taxa de admissão de ~20%, contra ~11,4% dos candidatos masculinos
- A diferença nas taxas de admissão entre gêneros é **estatisticamente significativa** (teste z, p < 0,05)
- GPA e GMAT, isoladamente, **não explicam** a diferença de admissão entre os gêneros (teste t, p > 0,05)
- Experiência profissional **não diferencia** admitidos de não admitidos para nenhum dos gêneros
- ~30% dos registros da variável `raca` são nulos, limitando a análise de equidade racial


## Arquivos

```
eda-mba-admission/
- mba_admission.ipynb 
- README.md
```


## Dataset

- **Nome:** MBA Admission Dataset
- **Fonte:** [Kaggle](https://www.kaggle.com/datasets/taweilo/mba-admission-dataset)
- **Registros:** 6.194 candidatos × 10 variáveis
- **Variável-alvo:** `admissao` (admitir / lista de espera)


## Tecnologias

- Python 3.11
- pandas, numpy
- matplotlib, seaborn, plotly
- scipy.stats, statsmodels
- missingno, summarytools


```



# Desigualdade de Renda nos Estados Brasileiros (2012–2024)

Análise exploratória da evolução do Coeficiente de Gini nas 27 
unidades federativas brasileiras entre 2012 e 2024, com foco em 
convergência regional e heterogeneidade entre estados.

---

## Pergunta

Como evoluiu a desigualdade de renda entre os estados brasileiros 
na última década, e quais estados convergiram ou divergiram da 
média nacional?

---

## Principais Achados

- O Coeficiente de Gini médio entre os estados caiu 6,0% entre 
  2012 e 2024 (de 0,519 para 0,488)
- O pico de desigualdade ocorreu em 2018 (Gini médio = 0,525), 
  seguido de queda acentuada em 2020, ano do Auxílio Emergencial, e novo salto em 2021 com sua redução
- O desvio padrão do Gini entre estados caiu 24,1% no período 
  (de 0,040 para 0,030), indicando convergência regional
- Amazonas (−19,5%), Bahia (−14,6%) e Sergipe (−12,1%) 
  registraram as maiores reduções relativas
- Rio Grande do Norte (+3,4%) e Alagoas (+3,0%) foram os únicos 
  estados com aumento do Gini no período
- O Distrito Federal manteve o maior Gini médio (0,567), acima 
  de qualquer estado do Nordeste
- Santa Catarina registrou o menor Gini médio (0,420)

---

## Visualizações

| Gráfico | Descrição |
|---------|-----------|
| `01_gini_nacional.png` | Evolução do Gini médio nacional (2012–2024) |
| `02_gini_por_regiao.png` | Gini médio por região ao longo do tempo |
| `03_ranking_ufs.png` | Ranking de UFs por variação percentual (2012 → 2024) |
| `04_mapas_Brasil.png` | Mapa: Gini 2012, Gini 2024 e variação percentual |
| `05_evolucao_por_uf.png` | Evolução individual por UF com destaques |

---

## Dados

| Fonte | Variável | Período | Acesso |
|-------|----------|---------|--------|
| IPEA Data | Coeficiente de Gini por UF | 2012–2024 | API REST |

Série: `PNADCA_GINIUF`  
Endpoint: `http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='PNADCA_GINIUF')`

---

## Metodologia

Análise exploratória de painel descritivo com 27 UFs × 13 anos 
(351 observações). Sem modelo causal — o foco é descrever com 
precisão o que aconteceu.

Métricas calculadas:
- Gini médio nacional e por região por ano
- Variação percentual por UF (2012 → 2024)
- Desvio padrão entre UFs por ano (proxy de convergência regional)
- Estatísticas descritivas por ano, região e UF

---

## Como Rodar
```bash
git clone https://github.com/gabrielrpassos/desigualdade-renda-brasil
cd desigualdade-renda-brasil
pip install -r requirements.txt
jupyter notebook
```

Execute as células na ordem. Os dados são coletados diretamente 
via API, nenhum download manual necessário.

Ou abra no Google Colab: 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gabrielrpassos/desigualdade-renda-brasil/blob/main/desigualdade_renda_brasil.ipynb)

---

## Estrutura do Repositório
```
desigualdade-renda-brasil/
│
├── README.md
├── requirements.txt
├── desigualdade_renda_brasil.ipynb
├── painel_gini.xlsx
│
└── outputs/
    └── graficos/
        ├── 01_gini_nacional.png
        ├── 02_gini_por_regiao.png
        ├── 03_ranking_ufs.png
        ├── 04_mapas_Brasil.png
        └── 05_evolucao_por_uf.png
```

---

## Dependências
```
pandas>=2.0
matplotlib>=3.7
geopandas>=0.14
geobr>=0.1.7
requests>=2.31
jupyter>=1.0
openpyxl>=3.1
```

---

📧 gabrielribeiropassos@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/gabriel-ribeiro-passos/) · 
   [GitHub](https://github.com/gabrielrpassos)

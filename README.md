# Inteligencia de Mercado — Protege Bank

**Voz do Cliente vs Comportamento Real · 50.000 Clientes · NPS · Churn · Market Fit**

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

> *"O cliente disse que estava satisfeito. O modelo sabia que ele ia embora em 60 dias. Qual voce acredita?"*

Este case aplica **Inteligencia de Mercado** ao ecossistema bancario, triangulando a **voz declarada do cliente** (NPS, satisfacao, pesquisa) com o **comportamento real** (transacoes, engajamento digital, churn) para gerar insights acionaveis sobre Market Fit, retencao e posicionamento de produto.

---

## Resultados

### Indicadores Principais

| Indicador | Resultado | Situacao |
|-----------|-----------|----------|
| NPS Geral | +3,7 | Positivo, com espaco para crescer |
| Taxa de Churn | 21,9% | Atencao |
| Paradoxo Silencioso | 8,0% (3.993 clientes) | Risco Oculto |
| AUC-ROC Modelo | 0,731 | Bom |
| Clientes em Alto Risco | 619 | Intervencao Urgente |
| Receita em Risco | R$ 0,8M/ano | Impacto Critico |
| ROI da Intervencao | 603% | Viavel |

### NPS por Segmento

| Segmento | NPS | Interpretacao |
|----------|-----|---------------|
| Bronze | -11,0 | Critico — insatisfacao com taxas e atendimento |
| Prata | +8,9 | Neutro — massa critica, potencial de melhoria |
| Ouro | +39,3 | Satisfeito — bom fit de produto |
| Diamante | +59,8 | Promotor — tratamento diferenciado se reflete no NPS |

### Satisfacao por Produto

| Produto | Nota (1-5) | Status |
|---------|-----------|--------|
| Taxas | 3,38 | Abaixo do minimo aceitavel |
| Atendimento | 3,78 | Atencao |
| Seguro | 3,77 | Atencao |
| Cartao | 3,78 | Atencao |
| App Digital | 3,97 | Ok |

![Dashboard Executivo](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/07_dashboard_executivo.png)

---

## O Paradoxo Silencioso

O achado mais critico deste estudo: **8% dos clientes nao sao Detratores no NPS mas vao embora**.

Isso significa que pesquisa de satisfacao isolada e insuficiente para detectar risco de churn. A triangulacao com dados comportamentais e essencial — e e exatamente o que diferencia Inteligencia de Mercado de uma pesquisa comum.

| Grupo | % Base | Comportamento |
|-------|--------|---------------|
| Alinhado Positivo | 13,4% | Promotor e fica |
| Surpresa Positiva | 64,7% | Nao e Promotor mas fica |
| Paradoxo Silencioso | 8,0% | Nao e Detrator mas vai embora |
| Alinhado Negativo | 13,9% | Detrator e vai embora |

---

## Churn Prediction

Modelo **Random Forest** com AUC-ROC de 0,731, treinado com variaveis comportamentais, de satisfacao e demograficas.

### Top Drivers de Churn

| Variavel | Importancia |
|----------|------------|
| Reclamacoes 12m | 24,7% |
| NPS Score | 16,3% |
| Tempo como cliente | 8,5% |
| Numero de produtos | 6,4% |
| Renda mensal | 6,1% |
| Dias sem acesso | 5,8% |

### Simulador de Impacto Financeiro

Com 619 clientes em alto risco e taxa de retencao de 25%:
- **Receita preservada:** R$ 200k/ano
- **Custo da campanha:** R$ 28k
- **ROI:** 603%

---

## Graficos

### Perfil Demografico
![Demografico](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/01_perfil_demografico.png)

### NPS e Satisfacao
![NPS](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/02_nps_satisfacao.png)

### Benchmarking Competitivo
![Benchmarking](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/03_benchmarking.png)

### Triangulacao: Voz Declarada vs Comportamento Real
![Triangulacao](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/04_triangulacao.png)

### Market Fit por Produto e Segmento
![Market Fit](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/05_market_fit.png)

### Churn Prediction
![Churn](https://github.com/RoneyGalan/im-protege-bank/raw/main/images/06_churn_prediction.png)

---

## Estrutura do Notebook

```
im_protege_bank.ipynb
│
├── Secao 0  — Imports e configuracoes
├── Secao 1  — Geracao da base de 50.000 clientes
├── Secao 2  — Perfil demografico e segmentacao
├── Secao 3  — Pesquisa quantitativa: NPS e satisfacao
├── Secao 4  — Benchmarking competitivo
├── Secao 5  — Triangulacao: voz declarada vs comportamento real
├── Secao 6  — Market Fit por produto e segmento
├── Secao 7  — Churn Prediction (Random Forest)
├── Secao 8  — Simulador de impacto financeiro
└── Secao 9  — Dashboard executivo + conclusoes automaticas
```

---

## Stack

```
Python 3.11
├── pandas          — manipulacao de dados
├── numpy           — calculos vetoriais
├── matplotlib      — visualizacoes estaticas
├── seaborn         — heatmaps e estilo
├── scikit-learn    — Random Forest, LabelEncoder, metricas
└── scipy           — suporte estatistico
```

---

## Como Executar

```bash
git clone https://github.com/RoneyGalan/im-protege-bank.git
cd im-protege-bank
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook im_protege_bank.ipynb
```

---

## Autor

**Roney Galan**
Data Analyst · MBA Big Data & Analytics — FGV
[![LinkedIn](https://img.shields.io/badge/LinkedIn-roney--wesley--galan-blue?logo=linkedin)](https://linkedin.com/in/roney-wesley-galan-ba7aa194) [![GitHub](https://img.shields.io/badge/GitHub-RoneyGalan-black?logo=github)](https://github.com/RoneyGalan)

---

> *"Sem triangulacao, satisfacao declarada e so metade da verdade."*

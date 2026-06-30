<p align="center">
  <img src="banner_v2_pt.png" alt="Analise de Dados com Tableau" width="100%">
</p>

<div align="center">

  <img src="https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white">
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/datasets-5-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/level-iniciante%20a%20avancado-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/idioma-PT--BR-yellow?style=for-the-badge">

</div>

<h1 align="center">Analise de Dados com Tableau</h1>

<p align="center">
  <b>Repositorio com exemplos praticos de analise de dados utilizando Tableau Public/Tableau Desktop,</b><br>
  com datasets abertos e simulados baseados em cenarios reais do <b>Brasil</b>.
</p>

<p align="center">
  <a href="#comecar">Como Comecar</a> •
  <a href="#projetos">Projetos</a> •
  <a href="#datasets">Datasets</a> •
  <a href="#storyboard">Storyboard</a> •
  <a href="#contribuir">Contribuir</a>
</p>

---

## Destaques

| | |
|:---|:---|
| **5 Datasets Brasileiros** | Dados simulados baseados em cenarios reais do Brasil |
| **Storyboard Completo** | Wireframe + 6 cenas + checklist para dashboard de E-Commerce |
| **Guias de Boas Praticas** | Design, performance, calculos avancados no Tableau |
| **Fontes de Dados Abertos** | 20+ fontes reais (Portal da Transparencia, IBGE, etc.) |
| **Niveis de Dificuldade** | Iniciante, Intermediario e Avancado |

---

## Como Comecar

### Opcao 1: Pelo navegador (mais facil)
1. Baixe o dataset desejado em `datasets/`
2. Acesse [Tableau Public](https://public.tableau.com/) e crie uma conta gratuita
3. Clique em **Create** > **Web Authoring** > **Upload Data**
4. Selecione o arquivo CSV baixado
5. Siga as perguntas em `projects/[projeto]/README.md`

### Opcao 2: Pelo Tableau Desktop
1. Baixe e instale o [Tableau Public](https://www.tableau.com/products/public) (gratuito)
2. Baixe o dataset desejado em `datasets/`
3. No Tableau: **Connect** > **To a File** > **Text File**
4. Selecione o CSV e comece a explorar!

### Opcao 3: Pelo codigo (Git)
```bash
git clone https://github.com/AlanMacedo2019/tableau-data-analysis.git
cd tableau-data-analysis
# Abra os arquivos CSV no Tableau
```

---

## Projetos

| # | Projeto | Dataset | Tipo de Analise | Nivel |
|---|---------|---------|-----------------|-------|
| 1 | **E-Commerce Brasil** | `ecommerce_brazil.csv` | Vendas, Regioes, Produtos | Intermediario |
| 2 | **Saude Publica** | `public_health_brazil.csv` | Serie Temporal, Mapas | Intermediario |
| 3 | **Educacao & ENEM** | `education_brazil.csv` | Comparativo, Ranking | Iniciante |
| 4 | **Indicadores Economicos** | `economic_indicators_brazil.csv` | Series Temporais, Correlacoes | Avancado |
| 5 | **Transporte & Mobilidade** | `transport_metro_brazil.csv` | KPIs, Dashboard Operacional | Intermediario |

---

## Datasets

| Dataset | Registros | Periodo | Destaque |
|---------|-----------|---------|----------|
| **E-Commerce** | 5.000 | Jan/24 - Jun/25 | R$ 35,5M em vendas, 5 categorias, 10 produtos |
| **Saude Publica** | 486 | Jan/24 - Jun/25 | 27 estados, casos, UTI, vacinas |
| **Educacao** | 600 | 2024 | 200 escolas, notas ENEM simuladas, 4 tipos |
| **Economia** | 66 | Jan/20 - Jun/25 | IPCA, Selic, Dolar, IBOVESPA, PIB |
| **Transporte** | 900 | Jan/24 - Jun/25 | 5 linhas de metro, 10 estacoes, KPIs |

---

## Storyboard

O projeto **E-Commerce Brasil** conta com um [storyboard completo](projects/ecommerce-sales/STORYBOARD.md) incluindo:

- Wireframe do dashboard
- 6 cenas interativas (Visao Executiva, Drill-down, Analise de Produtos, etc.)
- Guia de estilo visual (cores, tipografia, formatos)
- Calculos Tableau prontos para copiar e colar
- Checklist de implementacao em 6 fases

---

## Screenshots dos Dashboards

> Em breve! Estou construindo os dashboards no Tableau Public.

| Projeto | Preview | Link Tableau Public |
|---------|---------|---------------------|
| E-Commerce Brasil | ![Em breve](assets/placeholder.png) | [Ver dashboard](#) |
| Saude Publica | ![Em breve](assets/placeholder.png) | [Ver dashboard](#) |
| Educacao | ![Em breve](assets/placeholder.png) | [Ver dashboard](#) |
| Indicadores Economicos | ![Em breve](assets/placeholder.png) | [Ver dashboard](#) |
| Transporte | ![Em breve](assets/placeholder.png) | [Ver dashboard](#) |

**Quer contribuir?** Se voce criou um dashboard com esses dados, abra uma [Issue](../../issues) ou [Pull Request](../../pulls)!

---

## Tecnologias Utilizadas

<p align="center">
  <img src="https://img.shields.io/badge/Tableau-E97627?style=flat&logo=Tableau&logoColor=white" height="30">
  <img src="https://img.shields.io/badge/CSV-217346?style=flat&logo=microsoft-excel&logoColor=white" height="30">
  <img src="https://img.shields.io/badge/Markdown-000000?style=flat&logo=markdown&logoColor=white" height="30">
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" height="30">
</p>

---

## Estrutura do Repositorio

```
tableau-data-analysis/
├── datasets/                          # Bases de dados em CSV
│   ├── ecommerce_brazil.csv
│   ├── public_health_brazil.csv
│   ├── education_brazil.csv
│   ├── economic_indicators_brazil.csv
│   └── transport_metro_brazil.csv
├── projects/                          # Documentacao de cada projeto
│   ├── ecommerce-sales/
│   │   ├── README.md
│   │   └── STORYBOARD.md
│   ├── public-health/
│   ├── education/
│   ├── finance-economy/
│   └── transport/
├── docs/                              # Guias gerais
│   ├── getting-started.md
│   ├── data-sources.md
│   └── tableau-best-practices.md
├── tableau-workbooks/                 # Arquivos .twbx (quando disponiveis)
├── assets/                            # Imagens e recursos visuais
├── .gitignore
├── LICENSE (MIT)
└── README.md
```

---

## Contribuir

Contribuicoes sao bem-vindas! Veja [CONTRIBUTING.md](CONTRIBUTING.md) para mais detalhes.

Formas de contribuir:
- Reportar bugs ou sugestoes ([Issues](../../issues))
- Adicionar novos datasets
- Compartilhar dashboards no Tableau Public
- Melhorar documentacao

---

## Licenca

Este projeto esta sob licenca [MIT](LICENSE). Os dados sao simulados para fins educacionais.

---

<p align="center">
  Feito com por <b>Alan Macedo</b> • 
  <a href="https://github.com/AlanMacedo2019">GitHub</a> • 
  <a href="#">LinkedIn</a>
</p>

<p align="center">
  ⭐ Se este repositorio foi util, deixe uma estrela!
</p>

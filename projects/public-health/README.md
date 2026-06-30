# 🏥 Saúde Pública - Análise de Dados Epidemiológicos

## Descrição
Análise de dados de saúde pública no Brasil, com foco em séries temporais, distribuição geográfica e indicadores hospitalares.

## Dataset
- **Arquivo:** `datasets/public_health_brazil.csv`
- **Registros:** 486 registros (27 estados × 18 meses)
- **Período:** Jan/2024 - Jun/2025
- **Colunas:** 11

## Estrutura dos Dados

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `date` | Date | Data (primeiro dia do mês) |
| `state` | String | UF |
| `region` | String | Região do Brasil |
| `new_cases` | Int | Novos casos no mês |
| `deaths` | Int | Óbitos no mês |
| `recoveries` | Int | Recuperações |
| `hospitalizations` | Int | Hospitalizações |
| `active_cases` | Int | Casos ativos |
| `doses_applied` | Int | Doses de vacina aplicadas |
| `tests_conducted` | Int | Testes realizados |
| `icu_occupancy_pct` | Float | Ocupação de UTI (%) |

## Perguntas para Análise

### Nível Iniciante
1. Qual o total de casos no período?
2. Qual estado com mais casos?
3. Qual a taxa de letalidade geral?

### Nível Intermediário
4. Crie um mapa de calor de casos por estado.
5. Qual a evolução temporal de casos por região?
6. Compare a ocupação de UTI entre estados.
7. Qual a correlação entre testes realizados e casos detectados?
8. Crie um gráfico de área empilhada por região.

### Nível Avançado
9. Calcule a taxa de letalidade por estado e mês.
10. Crie um dashboard com filtros de região e período.
11. Analise a sazonalidade: há picos em determinados meses?
12. Compare doses aplicadas vs novos casos (correlação).
13. Crie alertas visuais para ocupação de UTI > 80%.

## Dicas Tableau

### Mapas
- Arraste `state` para o mapa (Tableau reconhece UFs)
- Use `region` para cores diferentes
- Adicione tooltips com informações detalhadas

### Cálculos Úteis
```
// Taxa de Letalidade
SUM([deaths]) / SUM([new_cases])

// Taxa de Positividade
SUM([new_cases]) / SUM([tests_conducted])

// Casos por 100k habitantes (estimado)
SUM([new_cases]) / 100000
```

### Visualizações Recomendadas
- **Mapa coroplético:** Casos por estado
- **Gráfico de linha:** Evolução temporal
- **Heatmap:** Casos por estado × mês
- **Bullet chart:** Ocupação UTI vs meta (80%)
- **Gráfico de combinação:** Casos + Hospitalizações

## KPIs Sugeridos
- Total de Casos
- Total de Óbitos
- Taxa de Letalidade
- Ocupação Média de UTI
- Doses Aplicadas
- Estado com Maior Incidência

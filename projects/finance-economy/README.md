# 💰 Indicadores Econômicos - Análise Financeira

## Descrição
Análise de indicadores macroeconômicos brasileiros: IPCA, Selic, Dólar, IBOVESPA, PIB e Desemprego.

## Dataset
- **Arquivo:** `datasets/economic_indicators_brazil.csv`
- **Registros:** 66 registros (mensais: Jan/2020 - Jun/2025)
- **Colunas:** 11

## Estrutura dos Dados

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `date` | Date | Data (primeiro dia do mês) |
| `year` | Int | Ano |
| `month` | Int | Mês (1-12) |
| `month_name` | String | Nome do mês |
| `ipca_pct` | Float | Inflação IPCA (%) |
| `selic_pct` | Float | Taxa Selic (%) |
| `usd_brl` | Float | Dólar (R$) |
| `ibovespa` | Float | IBOVESPA (pontos) |
| `pib_growth_pct` | Float | Crescimento PIB (%) |
| `unemployment_pct` | Float | Desemprego (%) |
| `trade_balance_billion` | Float | Saldo Comercial (bi R$) |
| `foreign_investment_billion` | Float | Investimento Estrangeiro (bi R$) |

## Perguntas para Análise

### Nível Iniciante
1. Qual a média da Selic no período?
2. Qual o maior valor do Dólar? Quando?
3. Qual a evolução do IPCA ao longo do tempo?
4. Quantos meses o desemprego ficou acima de 10%?

### Nível Intermediário
5. Crie um gráfico de linha duplo: IPCA + Selic.
6. Qual a correlação entre Dólar e IBOVESPA?
7. Compare o desemprego por ano.
8. Crie um gráfico de área para o saldo comercial.
9. Analise a volatilidade do IBOVESPA (desvio padrão móvel).

### Nível Avançado
10. Crie um dashboard com séries temporais sincronizadas.
11. Calcule a variação percentual mensal do IBOVESPA.
12. Identifique períodos de "stagflation" (alta inflação + baixo crescimento).
13. Crie um gráfico de dispersão: Selic vs Dólar.
14. Faça uma análise de tendência com linha de regressão.
15. Crie alertas visuais para IPCA > 6% ou Desemprego > 10%.

## Dicas Tableau

### Cálculos Úteis
```
// Variação % Mensal IBOVESPA
([ibovespa] - LOOKUP([ibovespa], -1)) / LOOKUP([ibovespa], -1)

// Média Móvel 3 meses IPCA
WINDOW_AVG(SUM([ipca_pct]), -2, 0)

// Ano-Mês formatado
STR([year]) + '-' + STR([month])
```

### Visualizações Recomendadas
- **Dual axis:** IPCA + Selic (escalas diferentes)
- **Scatter plot:** Dólar vs IBOVESPA
- **Area chart:** Saldo comercial ao longo do tempo
- **Bullet chart:** Desemprego vs meta (8%)
- **Highlight table:** Indicadores por ano/mês
- **Sparklines:** Mini gráficos por indicador

## KPIs Sugeridos
- IPCA Atual
- Selic Atual
- Dólar (R$)
- IBOVESPA
- Desemprego (%)
- Crescimento PIB (%)
- Saldo Comercial (bi R$)

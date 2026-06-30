# 🚇 Transporte & Mobilidade - Dashboard Operacional

## Descrição
Análise de dados operacionais de transporte público (metrô), com foco em volume de passageiros, satisfação, incidentes e KPIs operacionais.

## Dataset
- **Arquivo:** `datasets/transport_metro_brazil.csv`
- **Registros:** 900 registros (5 linhas × 10 estações × 18 meses)
- **Período:** Jan/2024 - Jun/2025
- **Colunas:** 11

## Estrutura dos Dados

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `date` | Date | Data (primeiro dia do mês) |
| `line` | String | Linha do metrô |
| `station` | String | Nome da estação |
| `passengers_weekday` | Int | Passageiros dias úteis |
| `passengers_weekend` | Int | Passageiros fins de semana |
| `total_passengers` | Int | Total mensal estimado |
| `incidents_reported` | Int | Incidentes no mês |
| `avg_delay_minutes` | Float | Atraso médio (min) |
| `satisfaction_score` | Float | Nota satisfação (0-10) |
| `operating_hours` | Int | Horas operação/dia |
| `trains_in_service` | Int | Trens em operação |

## Perguntas para Análise

### Nível Iniciante
1. Qual o total de passageiros no período?
2. Qual a linha mais movimentada?
3. Qual a média de satisfação?
4. Quantos incidentes foram reportados?

### Nível Intermediário
5. Compare volume de passageiros entre linhas.
6. Qual a relação entre incidentes e atrasos?
7. Compare satisfação por linha e estação.
8. Crie um gráfico de barras: passageiros dias úteis vs fins de semana.
9. Qual a estação com mais incidentes?

### Nível Avançado
10. Crie um dashboard operacional com KPIs em tempo real (simulado).
11. Calcule a produtividade: passageiros / trem / hora.
12. Identifique estações com baixa satisfação + alta movimentação.
13. Crie um gráfico de correlação: incidentes vs satisfação.
14. Faça análise de Pareto: 20% das estações = 80% dos passageiros?
15. Crie um gráfico de Gantt para horário de operação.

## Dicas Tableau

### Cálculos Úteis
```
// Passageiros por Trem por Hora
SUM([total_passengers]) / (SUM([trains_in_service]) * SUM([operating_hours]) * 30)

// Satisfação ponderada por volume
SUM([satisfaction_score] * [total_passengers]) / SUM([total_passengers])

// Diferença Weekday vs Weekend
SUM([passengers_weekday]) - SUM([passengers_weekend])
```

### Visualizações Recomendadas
- **Bar chart:** Passageiros por linha
- **Heatmap:** Satisfação por estação × mês
- **Scatter plot:** Incidentes vs Atrasos
- **Bullet chart:** Satisfação vs meta (8.0)
- **Dual axis:** Passageiros + Satisfação
- **Treemap:** Tamanho = passageiros, Cor = satisfação

## KPIs Sugeridos
- Total de Passageiros
- Satisfação Média
- Incidentes Totais
- Atraso Médio (min)
- Linha Mais Movimentada
- Estação com Melhor Satisfação
- Trens em Operação

# 🛒 E-Commerce Brasil - Análise de Vendas

## Descrição
Análise de dados de vendas de e-commerce no Brasil, explorando padrões de compra por região, produto, método de pagamento e sazonalidade.

## Dataset
- **Arquivo:** `datasets/ecommerce_brazil.csv`
- **Registros:** 5.000 pedidos
- **Período:** Jan/2024 - Jun/2025
- **Colunas:** 14

## Estrutura dos Dados

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `order_id` | String | ID único do pedido |
| `date` | Date | Data da compra |
| `product` | String | Nome do produto |
| `category` | String | Categoria do produto |
| `region` | String | Região do Brasil |
| `state` | String | UF do cliente |
| `quantity` | Int | Quantidade comprada |
| `unit_price` | Float | Preço unitário (R$) |
| `discount_pct` | Float | Percentual de desconto |
| `total_value` | Float | Valor total do pedido (R$) |
| `freight` | Float | Valor do frete (R$) |
| `payment_method` | String | Forma de pagamento |
| `customer_id` | String | ID do cliente |
| `status` | String | Status do pedido |

## Perguntas para Análise (Questions)

### Nível Iniciante
1. Qual o faturamento total no período?
2. Quantos pedidos foram realizados?
3. Qual a categoria mais vendida?
4. Qual o método de pagamento mais utilizado?

### Nível Intermediário
5. Qual o faturamento por região? Crie um mapa.
6. Qual a evolução mensal das vendas? Crie um gráfico de linha.
7. Quais os 10 produtos mais vendidos por quantidade?
8. Qual a taxa de cancelamento por categoria?
9. Qual o ticket médio por região?

### Nível Avançado
10. Crie um dashboard com filtros por região, categoria e período.
11. Analise a correlação entre desconto e volume de vendas.
12. Identifique os clientes mais valiosos (RFM Analysis simplificado).
13. Crie um gráfico de Pareto (80/20) de produtos vs faturamento.
14. Analise a sazonalidade: há padrões por mês/trimestre?

## Dicas Tableau (Tableau Tips)

### Mapas
- Use `state` como dimensão geográfica
- Tableau reconhece automaticamente as UFs brasileiras
- Ajuste a projeção para "Mercator" ou "Albers Equal Area Conic"

### Cálculos Úteis
```
// Ticket Médio
SUM([total_value]) / COUNTD([order_id])

// Margem com Frete
([total_value] - [freight]) / [total_value]

// Mês/Ano
DATETRUNC('month', [date])
```

### Filtros
- Crie um filtro de data com range slider
- Use parâmetros para selecionar métrica (faturamento, quantidade, ticket médio)

### Visualizações Recomendadas
- **Mapa coroplético:** Faturamento por estado
- **Gráfico de barras:** Top produtos
- **Linha temporal:** Evolução de vendas
- **Treemap:** Participação por categoria
- **Tabela dinâmica:** Detalhamento por estado/produto

## KPIs Sugeridos no Dashboard
- Faturamento Total
- Total de Pedidos
- Ticket Médio
- Taxa de Cancelamento
- Produto Mais Vendido
- Região com Maior Faturamento

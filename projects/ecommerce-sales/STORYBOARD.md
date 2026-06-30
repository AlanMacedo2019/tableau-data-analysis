# 📖 Storyboard: E-Commerce Brasil - Dashboard de Análise de Vendas

> **Projeto:** E-Commerce Brasil  
> **Dataset:** `ecommerce_brazil.csv` (5.000 pedidos, Jan/2024 - Jun/2025)  
> **Ferramenta:** Tableau Public / Tableau Desktop  
> **Público-alvo:** Gestores de e-commerce, analistas de vendas, diretoria comercial  
> **Objetivo:** Monitorar performance de vendas, identificar oportunidades e alertar sobre problemas operacionais

---

## 🎯 Visão Geral do Dashboard

O dashboard apresenta uma visão 360° do e-commerce brasileiro, permitindo:
- **Monitoramento em tempo real** (simulado) do faturamento
- **Análise geográfica** das vendas por estado e região
- **Identificação de produtos campeões** e categorias em alta
- **Acompanhamento de satisfação** via taxa de cancelamento
- **Comportamento do consumidor** por método de pagamento e ticket médio

---

## 📐 Layout do Dashboard (Wireframe)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  🏠 E-COMMERCE BRASIL - DASHBOARD DE VENDAS          [🔍 Filtros]  [📅]  │
│  Última atualização: 30/06/2025                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐    │
│  │ 💰       │  │ 📦       │  │ 🎫       │  │ ❌       │  │ 🚚       │    │
│  │R$ 35,5M  │  │ 5.000    │  │ R$ 7.102 │  │ 5,2%     │  │ R$ 45,2  │    │
│  │Faturamento│  │ Pedidos  │  │Ticket Méd│  │Cancelados│  │Frete Méd │    │
│  │ +12% vs  │  │ +8% vs   │  │ +3% vs   │  │ -1,2% vs │  │ -5% vs   │    │
│  │ mês ant  │  │ mês ant  │  │ mês ant  │  │ mês ant  │  │ mês ant  │    │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  └──────────┘    │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌─────────────────────────────────┐    ┌──────────────────────────────┐    │
│  │                                 │    │                              │    │
│  │   🗺️ MAPA DO BRASIL            │    │   📈 EVOLUÇÃO MENSAL        │    │
│  │                                 │    │   (Faturamento por Mês)      │    │
│  │   Faturamento por Estado        │    │                              │    │
│  │   - Cores: Verde (alto)         │    │   Linha com área            │    │
│  │     Amarelo (médio)             │    │   - Tooltip: valor +        │    │
│  │     Vermelho (baixo)            │    │     variação %              │    │
│  │   - Tooltip: Estado, valor,      │    │   - Linha de tendência      │    │
│  │     % do total, ranking         │    │   - Destaque para picos     │    │
│  │                                 │    │                              │    │
│  │   [Clique no estado para       │    │                              │    │
│  │    filtrar todo o dashboard]    │    │                              │    │
│  │                                 │    │                              │    │
│  └─────────────────────────────────┘    └──────────────────────────────┘    │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────────────────────────┐    ┌─────────────────────────────────┐   │
│  │                              │    │                                 │   │
│  │   🏆 TOP 10 PRODUTOS         │    │   💳 MÉTODOS DE PAGAMENTO      │   │
│  │   (por Faturamento)          │    │   (Faturamento + Quantidade)   │   │
│  │                              │    │                                 │   │
│  │   Barras horizontais         │    │   Gráfico de Pizza/Donut       │   │
│  │   - Cor por categoria        │    │   - % do faturamento           │   │
│  │   - Ícone do produto         │    │   - PIX destacado em verde     │   │
│  │   - Variação % vs anterior   │    │   - Tooltip: valor + qtd pedidos│   │
│  │                              │    │                                 │   │
│  └──────────────────────────────┘    └─────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────────────────────────────────────────────────────────────────┐   │
│  │                                                                      │   │
│  │   📊 ANÁLISE DE CATEGORIAS (Treemap + Tabela)                       │   │
│  │                                                                      │   │
│  │   Treemap: Tamanho = Faturamento, Cor = Taxa de Cancelamento        │   │
│  │   - Verde: Baixa taxa de cancelamento (< 3%)                        │   │
│  │   - Amarelo: Média (3-7%)                                           │   │
│  │   - Vermelho: Alta (> 7%)                                           │   │
│  │                                                                      │   │
│  │   Tabela ao lado:                                                    │   │
│  │   Categoria | Faturamento | Qtd | Ticket Médio | Cancelamento | Δ%  │   │
│  │                                                                      │   │
│  └──────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 🎬 Cenas do Storyboard

### CENA 1: Tela Inicial - Visão Executiva (Overview)

**Objetivo:** Dar ao gestor uma visão rápida e completa da saúde do negócio em 5 segundos.

**Elementos:**
- **5 KPIs Cards** no topo com variação vs mês anterior
- **Mapa do Brasil** com faturamento por estado (coroplético)
- **Gráfico de linha** com evolução mensal de faturamento
- **Top 10 produtos** mais vendidos
- **Distribuição de pagamentos** (pizza/donut)
- **Treemap de categorias** com alerta de cancelamento

**Interações:**
- Clique em qualquer estado no mapa → filtra todo o dashboard
- Clique em uma categoria no treemap → filtra produtos e pagamentos
- Hover em KPIs → tooltip com detalhamento

**Cores:**
- Verde: Positivo (crescimento, baixo cancelamento)
- Vermelho: Negativo (queda, alto cancelamento, >7% cancelamento)
- Azul: Neutro/Informação
- Cinza: Fundo claro, texto secundário

**Filtros disponíveis:**
- Período (range de datas)
- Região (dropdown multi-seleção)
- Categoria (dropdown multi-seleção)
- Status do pedido (Entregue, Em trânsito, Cancelado, Processando)

---

### CENA 2: Drill-down - Análise por Estado

**Gatilho:** Clique em um estado no mapa da Cena 1

**Objetivo:** Analisar em detalhe o desempenho de um estado específico.

**Elementos:**
- **Título dinâmico:** "Análise de Vendas - São Paulo"
- **KPIs do estado** (faturamento, pedidos, ticket médio vs média nacional)
- **Top 10 cidades** (simulado a partir de dados do estado)
- **Evolução temporal** do estado vs Brasil
- **Produtos mais vendidos** no estado
- **Métodos de pagamento preferidos** no estado
- **Comparativo:** Este estado vs média nacional (bullet charts)

**Interações:**
- Botão "Voltar para Visão Nacional" no topo
- Clique em produto → filtra timeline
- Hover em bullet chart → comparação detalhada

**Alertas visuais:**
- Se ticket médio do estado < 80% da média nacional → destaque amarelo
- Se taxa de cancelamento > 10% → destaque vermelho
- Se faturamento cresceu > 20% vs mês anterior → badge "🔥 Destaque"

---

### CENA 3: Análise de Produtos - Performance e Oportunidades

**Gatilho:** Clique em "Ver Análise de Produtos" no menu lateral

**Objetivo:** Identificar quais produtos estão performando bem e quais precisam de atenção.

**Elementos:**
- **Scatter plot:** Eixo X = Quantidade vendida, Eixo Y = Faturamento, Tamanho = Ticket médio, Cor = Categoria
- **Matriz BCG (simulada):**
  - Estrelas: Alto faturamento + Alto crescimento
  - Vacas leiteiras: Alto faturamento + Baixo crescimento
  - Interrogações: Baixo faturamento + Alto crescimento
  - Abacaxis: Baixo faturamento + Baixo crescimento
- **Tabela detalhada:** Produto | Categoria | Qtd | Faturamento | Ticket Médio | Cancelamento | Margem estimada
- **Filtro de categoria** com botões rápidos (Eletrônicos, Acessórios, Games, etc.)

**Interações:**
- Seleção de produto no scatter → destaque na tabela e vice-versa
- Filtro de categoria → atualiza scatter e tabela
- Clique duplo em produto → abre "Detalhe do Produto" (Cena 4)

**Cálculos Tableau necessários:**
```
// Crescimento vs Mês Anterior
(SUM([total_value]) - LOOKUP(SUM([total_value]), -1)) / LOOKUP(SUM([total_value]), -1)

// Margem Estimada (assumindo 30% de margem bruta)
SUM([total_value]) * 0.30 - SUM([freight])

// Classificação BCG
IF [Faturamento] > [Mediana Faturamento] AND [Crescimento] > [Mediana Crescimento] THEN "⭐ Estrela"
ELSEIF [Faturamento] > [Mediana Faturamento] THEN "🐄 Vaca Leiteira"
ELSEIF [Crescimento] > [Mediana Crescimento] THEN "❓ Interrogação"
ELSE "🍍 Abacaxi"
END
```

---

### CENA 4: Detalhe do Produto - Análise Individual

**Gatilho:** Clique duplo em um produto na Cena 3

**Objetivo:** Análise profunda de um produto específico.

**Elementos:**
- **Título dinâmico:** "Smartphone - Análise Detalhada"
- **Foto/ícone do produto** (placeholder)
- **KPIs do produto:** Faturamento total, Qtd vendida, Ticket médio, Taxa de cancelamento, Região que mais compra
- **Série temporal:** Vendas mensais do produto com linha de tendência
- **Mapa:** Estados que mais compram o produto (tamanho da bolha = volume)
- **Análise de preço:** Distribuição de preços unitários (histograma) - mostra variação por desconto
- **Tabela de clientes:** Top 10 clientes que compraram este produto (simulado via customer_id)
- **Satisfação (proxy):** Taxa de cancelamento do produto vs categoria

**Interações:**
- Botão "Voltar para Análise de Produtos"
- Hover no histograma de preço → mostra quantidade de vendas naquela faixa
- Clique no mapa → filtra série temporal por estado

---

### CENA 5: Análise de Clientes - Comportamento e Segmentação

**Gatilho:** Clique em "Análise de Clientes" no menu lateral

**Objetivo:** Entender o perfil e comportamento dos clientes.

**Elementos:**
- **Segmentação RFM (simplificada):**
  - Recência: Quando comprou pela última vez
  - Frequência: Quantos pedidos no período
  - Monetário: Valor total gasto
- **Gráfico de dispersão:** Frequência vs Monetário, Tamanho = Recência, Cor = Segmento
- **Tabela de segmentos:**
  - Champions: Compram muito e frequentemente
  - Loyal: Compram regularmente
  - Potential: Compraram pouco, mas gastaram bem
  - At Risk: Não compram há tempo
  - Lost: Inativos
- **Mapa:** Distribuição geográfica dos segmentos
- **Métodos de pagamento por segmento** (stacked bar)
- **Ticket médio por segmento**

**Cálculos Tableau:**
```
// Recência (dias desde última compra)
DATEDIFF('day', {FIXED [customer_id] : MAX([date])}, TODAY())

// Frequência (número de pedidos por cliente)
{FIXED [customer_id] : COUNTD([order_id])}

// Monetário (total gasto por cliente)
{FIXED [customer_id] : SUM([total_value])}

// Segmento RFM
IF [Recência] <= 30 AND [Frequência] >= 5 AND [Monetário] >= 10000 THEN "🏆 Champions"
ELSEIF [Frequência] >= 3 THEN "💎 Loyal"
ELSEIF [Monetário] >= 5000 THEN "🌟 Potential"
ELSEIF [Recência] <= 90 THEN "⚠️ At Risk"
ELSE "😴 Lost"
END
```

---

### CENA 6: Alertas e Anomalias - Painel de Monitoramento

**Gatilho:** Dashboard automático / Aba "Alertas"

**Objetivo:** Identificar rapidamente problemas que precisam de ação imediata.

**Elementos:**
- **Cards de alerta** com contadores:
  - 🚨 Pedidos cancelados no último mês: X (+Y% vs anterior)
  - ⚠️ Estados com ticket médio abaixo da meta: X
  - 🔥 Produtos com crescimento > 50%: X (oportunidade de estoque)
  - 📉 Categorias com queda > 20%: X
- **Tabela de alertas detalhados:**
  - Tipo | Descrição | Severidade | Tendência | Ação Sugerida
- **Gráfico de controle:** Faturamento diário com bandas de controle (média ± 2 desvios)
- **Pontos fora da banda** destacados em vermelho

**Cálculos Tableau:**
```
// Média Móvel 7 dias
WINDOW_AVG(SUM([total_value]), -6, 0)

// Banda Superior (média + 2 desvios)
[Media Movel] + 2 * WINDOW_STDEV(SUM([total_value]), -6, 0)

// Banda Inferior
[Media Movel] - 2 * WINDOW_STDEV(SUM([total_value]), -6, 0)

// Alerta
IF SUM([total_value]) > [Banda Superior] OR SUM([total_value]) < [Banda Inferior] THEN "🚨 ANOMALIA"
ELSE "✅ NORMAL"
END
```

---

## 🎨 Guia de Estilo Visual

### Paleta de Cores

| Uso | Cor | Hex |
|-----|-----|-----|
| Primária (destaques) | Azul Tableau | `#4E79A7` |
| Sucesso / Crescimento | Verde | `#59A14F` |
| Alerta / Atenção | Amarelo | `#EDC948` |
| Perigo / Cancelamento | Vermelho | `#E15759` |
| Neutro / Informação | Cinza azulado | `#BAB0AC` |
| Fundo cards | Branco | `#FFFFFF` |
| Fundo dashboard | Cinza claro | `#F5F5F5` |
| Texto principal | Preto | `#333333` |
| Texto secundário | Cinza | `#666666` |

### Tipografia
- **Título do dashboard:** 24pt, bold, `#333333`
- **Título de seção:** 16pt, semibold, `#4E79A7`
- **KPI valor:** 28pt, bold, cor conforme contexto
- **KPI label:** 12pt, regular, `#666666`
- **Corpo de texto:** 11pt, regular, `#333333`
- **Tooltip:** 10pt, regular, `#333333`

### Formato de Números
- **Moeda (R$):** R$ 1.234.567,89
- **Percentual:** 12,5% (1 casa decimal)
- **Quantidade:** 1.234 (separador de milhar)
- **Variação:** +12,5% ▲ (com seta indicadora)

---

## 🔧 Interatividade e Ações

### Ações Configuradas (Actions)

| Ação | Gatilho | Efeito | Destino |
|------|---------|--------|---------|
| **Filtrar por Estado** | Clique no mapa | Filtra todos os gráficos | Todo o dashboard |
| **Filtrar por Categoria** | Clique no treemap | Filtra produtos e pagamentos | Seção inferior |
| **Destacar Produto** | Clique no scatter | Destaca na tabela | Cena 3 |
| **Navegar para Detalhe** | Clique duplo em produto | Abre Cena 4 | Nova aba/planilha |
| **Limpar Filtros** | Botão "Limpar" | Reseta todos os filtros | Todo o dashboard |
| **Hover Highlight** | Mouse sobre barra | Destaca categoria em todos os gráficos | Todo o dashboard |

### Parâmetros Sugeridos

| Parâmetro | Tipo | Opções | Uso |
|-----------|------|--------|-----|
| **Métrica Principal** | String | Faturamento, Quantidade, Ticket Médio | Altera KPIs e gráficos |
| **Período de Comparação** | String | Mês anterior, Ano anterior, Meta | Calcula variações nos KPIs |
| **Limite de Cancelamento** | Float | 3%, 5%, 7%, 10% | Define cor do alerta no treemap |

---

## 📱 Responsividade e Dispositivos

### Desktop (1920×1080)
- Layout completo com 5 KPIs em linha
- Mapa + Gráfico de linha lado a lado
- Top produtos + Pagamentos lado a lado
- Treemap + Tabela em largura total

### Tablet (1024×768)
- KPIs em 2 linhas (3 + 2)
- Mapa em largura total
- Gráfico de linha abaixo do mapa
- Top produtos e pagamentos empilhados
- Treemap com scroll horizontal

### Mobile (375×667)
- KPIs em carrossel horizontal (swipe)
- Mapa simplificado (apenas regiões)
- Gráficos empilhados verticalmente
- Tabela com paginação
- Menu hambúrguer para filtros

---

## 📋 Checklist de Implementação

### Fase 1: Estrutura (2-3 horas)
- [ ] Conectar dataset ao Tableau
- [ ] Criar extração (extract) dos dados
- [ ] Verificar tipos de dados (date, number, string, geography)
- [ ] Criar hierarquia: Região → Estado
- [ ] Criar cálculos básicos: Faturamento, Ticket Médio, Taxa de Cancelamento
- [ ] Configurar formato de moeda (Real brasileiro)

### Fase 2: KPIs e Cards (1-2 horas)
- [ ] Criar 5 planilhas de KPI (texto simples)
- [ ] Adicionar formatação condicional (cor baseada em variação)
- [ ] Criar cálculos de variação vs período anterior
- [ ] Alinhar cards no dashboard

### Fase 3: Visualizações Principais (4-6 horas)
- [ ] Mapa coroplético do Brasil (faturamento por estado)
- [ ] Gráfico de linha (evolução mensal)
- [ ] Top 10 produtos (barras horizontais)
- [ ] Métodos de pagamento (donut chart)
- [ ] Treemap de categorias
- [ ] Tabela de categorias detalhada

### Fase 4: Interatividade (2-3 horas)
- [ ] Configurar ação de filtro (mapa → todo dashboard)
- [ ] Configurar ação de highlight (hover entre gráficos)
- [ ] Criar parâmetros (métrica principal, período)
- [ ] Configurar filtros globais (data, região, categoria, status)
- [ ] Testar todas as interações

### Fase 5: Polimento (2-3 horas)
- [ ] Ajustar cores conforme guia de estilo
- [ ] Personalizar tooltips (texto, formatação, imagens)
- [ ] Adicionar títulos e subtítulos descritivos
- [ ] Inserir texto explicativo onde necessário
- [ ] Ajustar alinhamentos e espaçamentos
- [ ] Testar performance (tempo de carregamento)

### Fase 6: Publicação (1 hora)
- [ ] Salvar como .twbx (com dados embutidos)
- [ ] Publicar no Tableau Public
- [ ] Testar no navegador (Chrome, Firefox, Safari)
- [ ] Testar em mobile (se aplicável)
- [ ] Copiar URL de embed para relatórios
- [ ] Documentar no repositório GitHub

---

## 🚀 Próximos Passos e Evoluções

### Versão 1.1 (Curto prazo)
- [ ] Adicionar dados de custo para calcular lucratividade real
- [ ] Incluir análise de sazonalidade (comparar anos)
- [ ] Adicionar previsão de vendas (trend line + forecast)
- [ ] Criar alertas automáticos por email (Tableau Server)

### Versão 2.0 (Médio prazo)
- [ ] Integrar com Google Analytics (tráfego do site)
- [ ] Adicionar análise de cohort (retenção de clientes)
- [ ] Incluir NPS / Satisfação do cliente (dados reais)
- [ ] Criar versão mobile otimizada
- [ ] Adicionar storytelling automático (Tableau Stories)

### Versão 3.0 (Longo prazo)
- [ ] Machine Learning: previsão de churn de clientes
- [ ] Recomendação de produtos (cross-selling)
- [ ] Otimização de preços dinâmica
- [ ] Integração com ERP em tempo real
- [ ] Chatbot com dados do dashboard (Tableau + AI)

---

## 📚 Referências e Inspiração

- [Tableau Public Gallery - Sales Dashboards](https://public.tableau.com/app/search/sales)
- [Makeover Monday - E-commerce datasets](https://www.makeovermonday.co.uk/)
- [Workout Wednesday - Advanced techniques](https://www.workout-wednesday.com/)
- [Tableau Best Practices - Layout](https://www.tableau.com/learn/whitepapers/dashboard-design-best-practices)
- [Storytelling with Data - Cole Nussbaumer](https://www.storytellingwithdata.com/)

---

> **Nota para desenvolvedor:** Este storyboard serve como guia completo para a construção do dashboard. Sinta-se à vontade para adaptar cores, layout e funcionalidades conforme necessidade. O importante é manter a coerência visual e a usabilidade. Boa análise! 🎉

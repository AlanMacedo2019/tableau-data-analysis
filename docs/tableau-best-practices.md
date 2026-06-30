# 🎨 Tableau Best Practices - Boas Práticas

## Design de Dashboards

### 1. Layout e Organização
- **Regra dos 3 segundos:** O usuário deve entender o propósito em 3 segundos
- **F-pattern:** Coloque informações importantes no topo e à esquerda
- **Consistência:** Use o mesmo esquema de cores em todo o dashboard
- **Espaço em branco:** Não sobrecarregue o canvas. Menos é mais.

### 2. Cores
- **Máximo 5-7 cores** diferentes em um dashboard
- **Paleta consistente:** Use a mesma cor para a mesma categoria
- **Cores semânticas:**
  - Verde = positivo/bom
  - Vermelho = negativo/ruim
  - Amarelo/Laranja = atenção
  - Azul = neutro/informação
- **Acessibilidade:** Evite combinações problemáticas para daltônicos (vermelho/verde)

### 3. Tipografia
- **Máximo 2 fontes** por dashboard
- **Títulos:** 16-18pt, negrito
- **Subtítulos:** 12-14pt
- **Corpo:** 10-11pt
- **Contraste:** Texto escuro em fundo claro (ou vice-versa)

### 4. Interatividade
- **Filtros:** Coloque-os no topo ou à direita
- **Highlight:** Use para destacar dados relacionados
- **Actions:** Configure ações entre planilhas (filtro, highlight, URL)
- **Tooltips:** Personalize com informações úteis
- **Parâmetros:** Permitem ao usuário escolher métricas ou cenários

---

## Performance

### 1. Dados
- **Extraia dados** (Extract) em vez de Live quando possível
- **Filtre na fonte:** Use filtros de contexto para reduzir dados
- **Agregue:** Use SUM, AVG, COUNT em vez de linha a linha
- **Evite cálculos complexos** em grandes volumes

### 2. Visualizações
- **Limite o número de marcas:** < 10.000 para melhor performance
- **Evite gráficos de dispersão** com milhões de pontos
- **Use amostras** para exploração inicial
- **Desabilite animações** em dashboards de produção

---

## Tipos de Gráficos - Quando Usar

| Gráfico | Quando Usar | Evitar Quando |
|---------|-------------|---------------|
| **Barra** | Comparar categorias | Muitas categorias (>20) |
| **Linha** | Tendências temporais | Dados categóricos |
| **Área** | Volume acumulado | Comparação precisa |
| **Pizza** | Parte do todo (2-5 fatias) | Muitas fatias, comparação |
| **Dispersão** | Correlação, relação | Sem relação clara |
| **Mapa** | Dados geográficos | Sem componente espacial |
| **Heatmap** | Padrões em matriz | Dados contínuos |
| **Boxplot** | Distribuição, outliers | Público não técnico |
| **Treemap** | Hierarquia, proporção | Comparação precisa |
| **Bullet** | KPI vs meta | Sem meta definida |
| **Gantt** | Cronograma, duração | Dados não temporais |
| **Histograma** | Distribuição de frequência | Dados categóricos |

---

## Cálculos Avançados

### Table Calculations
```
// Running Total (Total Acumulado)
RUNNING_SUM(SUM([Sales]))

// Percent of Total
SUM([Sales]) / TOTAL(SUM([Sales]))

// Rank
RANK(SUM([Sales]))

// Moving Average
WINDOW_AVG(SUM([Sales]), -2, 0)
```

### LOD (Level of Detail) Expressions
```
// Fixed - Ignora filtros
{FIXED [Region] : SUM([Sales])}

// Include - Adiciona dimensão
{INCLUDE [Category] : SUM([Sales])}

// Exclude - Remove dimensão
{EXCLUDE [Month] : SUM([Sales])}
```

### Date Calculations
```
// Year to Date
YTD(SUM([Sales]))

// Same Period Last Year
SUM([Sales]) - LOOKUP(SUM([Sales]), -12)

// DATEDIFF
DATEDIFF('day', [Start Date], [End Date])
```

---

## Publicação e Compartilhamento

### Tableau Public
- Gratuito, mas dados são públicos
- Ideal para portfólio e aprendizado
- URL pública para compartilhar

### Tableau Server/Online
- Controle de acesso e permissões
- Atualização automática de dados
- Integração com Active Directory

### Exportação
- **PDF:** Para relatórios estáticos
- **Imagem:** Para apresentações
- **PowerPoint:** Para reuniões
- **CSV:** Para análise posterior em Excel
- **Crosstab:** Para tabelas de dados

---

## Checklist Final do Dashboard

- [ ] Título claro e descritivo
- [ ] Legenda explicativa (se necessário)
- [ ] Filtros funcionando corretamente
- [ ] Tooltips informativos
- [ ] Cores consistentes e acessíveis
- [ ] Performance aceitável (< 5s para carregar)
- [ ] Testado em diferentes resoluções
- [ ] Sem erros de cálculo ou dados
- [ ] Fonte dos dados citada
- [ ] Data da última atualização visível
- [ ] Contato/autor identificado

# 📚 Educação - Análise de Desempenho Escolar

## Descrição
Análise de dados educacionais comparando desempenho entre escolas públicas e privadas, regiões e disciplinas.

## Dataset
- **Arquivo:** `datasets/education_brazil.csv`
- **Registros:** 600 registros (200 escolas × 3 séries)
- **Ano:** 2024
- **Colunas:** 17

## Estrutura dos Dados

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `school_name` | String | Nome da escola |
| `school_type` | String | Tipo (Pública/Privada) |
| `region` | String | Região |
| `state` | String | UF |
| `grade` | String | Série/Ano |
| `year` | Int | Ano de referência |
| `students_enrolled` | Int | Alunos matriculados |
| `students_approved` | Int | Alunos aprovados |
| `students_failed` | Int | Alunos reprovados |
| `approval_rate` | Float | Taxa de aprovação (%) |
| `math_score` | Float | Nota Matemática |
| `portuguese_score` | Float | Nota Português |
| `science_score` | Float | Nota Ciências |
| `humanities_score` | Float | Nota Humanidades |
| `essay_score` | Float | Nota Redação |
| `average_score` | Float | Nota Média |
| `teachers_count` | Int | Professores |
| `infrastructure_score` | Float | Nota Infraestrutura (0-10) |

## Perguntas para Análise

### Nível Iniciante
1. Qual a nota média geral?
2. Qual a taxa de aprovação média?
3. Quantas escolas são públicas vs privadas?
4. Qual disciplina tem a maior nota média?

### Nível Intermediário
5. Compare notas médias: público vs privado.
6. Crie um ranking das top 20 escolas por nota média.
7. Qual a relação entre infraestrutura e nota média?
8. Compare taxa de aprovação por região.
9. Crie um gráfico de caixa (boxplot) das notas por disciplina.

### Nível Avançado
10. Crie um scatter plot: infraestrutura vs nota média.
11. Analise a correlação entre número de professores e desempenho.
12. Crie um heatmap de notas por disciplina × região.
13. Identifique escolas com alta infraestrutura mas baixo desempenho.
14. Crie um dashboard com drill-down: Região → Estado → Escola.

## Dicas Tableau

### Cálculos Úteis
```
// Diferença Público vs Privado
IF [school_type] = 'Privada' THEN [average_score] END - 
IF [school_type] = 'Pública Municipal' OR [school_type] = 'Pública Estadual' OR [school_type] = 'Pública Federal' THEN [average_score] END

// Alunos por Professor
SUM([students_enrolled]) / SUM([teachers_count])
```

### Visualizações Recomendadas
- **Bar chart:** Notas médias por tipo de escola
- **Scatter plot:** Infraestrutura vs Nota Média
- **Boxplot:** Distribuição de notas por disciplina
- **Heatmap:** Notas por região/disciplina
- **Treemap:** Tamanho = alunos, Cor = nota média
- **Lollipop chart:** Ranking de escolas

## KPIs Sugeridos
- Nota Média Geral
- Taxa de Aprovação Média
- Melhor Disciplina
- Melhor Região
- Escola #1 no Ranking
- Diferença Público vs Privado

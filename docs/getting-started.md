# 🚀 Getting Started - Guia de Início Rápido

## Instalação do Tableau

### Tableau Public (Gratuito)
1. Acesse: https://public.tableau.com/
2. Crie uma conta gratuita
3. Baixe o Tableau Public para Desktop
4. Instale e inicie o programa

### Tableau Desktop (Pago / Estudante)
- Versão completa com mais funcionalidades
- Licença gratuita para estudantes via: https://www.tableau.com/academic

---

## Primeiros Passos

### 1. Conectar aos Dados
1. Abra o Tableau
2. Clique em **"Microsoft Excel"** ou **"Text File"** (CSV)
3. Navegue até a pasta `datasets/`
4. Selecione um arquivo CSV
5. O Tableau abrirá a aba **Data Source**

### 2. Explorar a Planilha
- Arraste campos para **Columns** (colunas) e **Rows** (linhas)
- Use a aba **Analytics** para adicionar tendências, referências, etc.
- Use a aba **Marks** para alterar cores, tamanhos, rótulos

### 3. Criar Visualizações

#### Gráfico de Barras
1. Arraste uma dimensão para **Columns**
2. Arraste uma medida para **Rows**
3. O Tableau cria automaticamente um gráfico de barras

#### Mapa
1. Arraste `state` ou `region` para a área de trabalho
2. O Tableau reconhece automaticamente como geográfico
3. Arraste uma medida para **Color** na aba Marks

#### Gráfico de Linha (Série Temporal)
1. Arraste `date` para **Columns**
2. Arrague uma medida para **Rows**
3. O Tableau cria um gráfico de linha

### 4. Criar um Dashboard
1. Clique no ícone **"New Dashboard"** (aba inferior)
2. Arraste visualizações da aba esquerda para o canvas
3. Adicione filtros, títulos e objetos de texto
4. Configure ações (filtros, highlights) para interatividade

### 5. Publicar
1. Clique em **Server > Tableau Public > Save to Tableau Public**
2. Faça login com sua conta
3. Seu dashboard ficará online e acessível via URL

---

## Dicas para Iniciantes

### Atalhos Úteis
- `Ctrl + W` = Nova planilha
- `Ctrl + D` = Novo dashboard
- `Ctrl + M` = Nova história (story)
- `Ctrl + 1` = Mostrar/ocultar aba Marks
- `Ctrl + 2` = Mostrar/ocultar painel de dados

### Boas Práticas
- **Renomeie campos** com nomes amigáveis (clique direito > Rename)
- **Crie hierarquias** (ex: Região → Estado → Cidade)
- **Use cores consistentes** em todo o dashboard
- **Adicione tooltips** informativos (clique em Tooltip na aba Marks)
- **Teste filtros** para garantir que funcionam corretamente

### Resolução de Problemas Comuns

**"Tableau não reconhece minha data"**
→ Clique no campo > Change Data Type > Date

**"Números estão como texto"**
→ Clique no campo > Change Data Type > Number (Decimal)

**"Mapa não aparece"**
→ Clique no campo geográfico > Map > Edit Locations > Selecione "Brazil"

**"Valores agregados de forma errada"**
→ Verifique a função de agregação (SUM, AVG, COUNT, etc.) na aba Marks

---

## Próximos Passos

1. Escolha um projeto em `projects/`
2. Leia as perguntas em `README.md`
3. Siga as dicas em `tableau-tips.md`
4. Crie suas visualizações
5. Publique e compartilhe!

---

## Recursos de Aprendizado

- [Tableau Public Gallery](https://public.tableau.com/app/discover) - Inspiração
- [Tableau Learning](https://www.tableau.com/learn) - Tutoriais oficiais
- [Makeover Monday](https://www.makeovermonday.co.uk/) - Desafios semanais
- [Workout Wednesday](https://www.workout-wednesday.com/) - Desafios técnicos
- [Tableau Community](https://community.tableau.com/) - Fórum de ajuda

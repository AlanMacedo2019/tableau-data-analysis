# 📚 Fontes de Dados Abertos Recomendadas

## Brasil

### Portal da Transparência
- **URL:** https://portaldatransparencia.gov.br/download-de-dados
- **Dados:** Despesas, convênios, licitações, contratos, viagens, salários
- **Formato:** CSV
- **Atualização:** Semanal/Mensal
- **Licença:** Domínio Público

### Base dos Dados
- **URL:** https://basedosdados.org
- **Dados:** Dados tratados e padronizados (SQL, Python, R)
- **Formato:** CSV, Parquet, SQL
- **Atualização:** Contínua
- **Licença:** Open Data

### IBGE
- **URL:** https://ibge.gov.br
- **Dados:** Censos, PNAD, PIB municipal, população
- **Formato:** CSV, XLS, API
- **Atualização:** Trimestral/Anual
- **Licença:** Domínio Público

### Dados.gov.br
- **URL:** https://dados.gov.br
- **Dados:** Catálogo central de dados abertos do governo federal
- **Formato:** CSV, JSON, XML
- **Atualização:** Variável
- **Licença:** Open Data

### ANA (Águas)
- **URL:** https://www.ana.gov.br/sala-de-situacao
- **Dados:** Nível de reservatórios, chuvas, vazões
- **Formato:** CSV, JSON
- **Atualização:** Diária

### INCRA
- **URL:** https://www.gov.br/incra/pt-br
- **Dados:** Terras indígenas, assentamentos, SIGTERRA
- **Formato:** Shapefile, CSV
- **Atualização:** Variável

---

## Internacional

### Data.gov (EUA)
- **URL:** https://data.gov
- **Dados:** Dados governamentais americanos
- **Formato:** CSV, JSON, API
- **Atualização:** Contínua

### World Bank Open Data
- **URL:** https://data.worldbank.org
- **Dados:** Indicadores globais de desenvolvimento
- **Formato:** CSV, Excel, API
- **Atualização:** Anual/Trimestral

### Kaggle
- **URL:** https://kaggle.com/datasets
- **Dados:** Competitions, datasets de machine learning
- **Formato:** CSV, JSON, Parquet
- **Atualização:** Contínua

### Our World in Data
- **URL:** https://ourworldindata.org
- **Dados:** Pesquisas acadêmicas, dados históricos
- **Formato:** CSV, Excel
- **Atualização:** Contínua

### Google Dataset Search
- **URL:** https://datasetsearch.research.google.com
- **Dados:** Busca em milhares de repositórios
- **Formato:** Variável
- **Atualização:** Contínua

### FiveThirtyEight
- **URL:** https://github.com/fivethirtyeight/data
- **Dados:** Dados de jornalismo de dados
- **Formato:** CSV
- **Atualização:** Variável

### UN Data
- **URL:** https://data.un.org
- **Dados:** Dados das Nações Unidas
- **Formato:** CSV, Excel
- **Atualização:** Anual

---

## Dados Específicos para Tableau

### Dados Geoespaciais
- **Natural Earth:** https://naturalearthdata.com
- **OpenStreetMap:** https://www.openstreetmap.org
- **IBGE Malhas:** https://geoftp.ibge.gov.br/organizacao_do_territorio/malhas_territoriais/

### Dados de Clima
- **NOAA:** https://www.ncdc.noaa.gov
- **NASA NEO:** https://neo.gsfc.nasa.gov
- **INMET:** https://portal.inmet.gov.br/dadoshistoricos

### Dados Financeiros
- **Yahoo Finance:** https://finance.yahoo.com
- **Banco Central:** https://www.bcb.gov.br/estatisticas
- **FRED (Federal Reserve):** https://fred.stlouisfed.org

### Dados de Saúde
- **WHO:** https://www.who.int/data
- **DataSUS:** https://datasus.saude.gov.br
- **CDC:** https://www.cdc.gov/datastatistics.html

---

## Dicas de Download

### CSV
- Formato mais comum e fácil de usar no Tableau
- Use "Text File" para importar
- Verifique encoding (UTF-8 recomendado)

### Excel
- Use para dados com múltiplas abas
- O Tableau lê .xlsx e .xls
- Evite formatação complexa (cores, merges)

### APIs
- Tableau pode conectar a APIs REST
- Use "Web Data Connector" ou "JSON"
- Requer conhecimento técnico intermediário

### Bancos de Dados
- Tableau conecta a MySQL, PostgreSQL, SQL Server, etc.
- Use "More > MySQL" ou similar
- Requer credenciais de acesso

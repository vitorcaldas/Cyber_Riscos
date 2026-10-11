# Análise em cibersegurança.

📋 Visão Geral do Projeto

O objetivo principal deste projeto para centralizar a gestão de incidentes, padronizar taxonomias de ataques cibernéticos e gerar insights operacionais para a equipe de segurança.

🛠️ Tecnologias Utilizadas

  - Python 

  - Pandas: Manipulação, limpeza e junção de estruturas tabulares.

  - NumPy: Operações numéricas auxiliares.

  - Matplotlib & Seaborn: Visualização de dados e tendências temporais.

  - Power BI: Construção de um dashboard interativo

📂 Estrutura de Fontes de Dados

  - chamados.csv: Base operacional contendo identificadores de chamados, usuários, datas e tipos brutos de incidentes.

  - Ofense.xlsx (Aba Chamados): Base complementar com registros de ocorrências por diferentes canais (Email, sistema, ISM).

  - logs.csv: Registros técnicos de auditoria contendo endereços IP de origem/destino, países e tipos de ataques associados.

⚙️ Principais Etapas do Pipeline

1. Ingestão e Inspeção Inicial

  - Leitura de arquivos .csv (delimitados por ponto e vírgula) e planilhas Excel (.xlsx).

  - Tratamento preventivo de exceções para validação de arquivos ausentes no diretório.

2. Limpeza, Padronização e Modelagem

  - Renomeação de Colunas: Harmonização dos esquemas entre as tabelas chamados e Ofense.

  - Tratamento de Datas: Conversão de strings para o formato datetime padronizado.

  - Consolidação (Outer Join): União dos datasets e unificação inteligente de colunas com preenchimento de valores ausentes (fillna).

  - Mapeamento Categorial: Agrupamento de incidentes granulares em categorias macro analíticas (ex: Acesso Indevido, Ataque Cibernético, Engenharia Social, Software Malicioso, Inclusão de Acesso).

  - Tratamento de Logs de Rede: Normalização de strings geográficas (ex: conversão de 'Br' para 'Brasil' e 'Estados Unidos' para 'EUA').

3. Análise Exploratória e Métricas (EDA)

  - Volumetria de incidentes por Origem (e.g., sistema, Email, ISM).

  - Identificação dos usuários com maior recorrência de chamados (Codigo_Usuario).

  - Análise temporal da volumetria diária e mensal de ocorrências de segurança.

  - Mapeamento de origens geográficas globais dos ataques logados.

4. Análise de dados no Power Bi

  - As informações para o Power BI, identificar quais são as fontes, realizou os tratamentos necessários e estabelecemos as correlações entre as bases. Após a construção gráfica, com qual gráfico utilizar e quais informações devem ser tratadas na investigação forense, na investigação de cibersegurança

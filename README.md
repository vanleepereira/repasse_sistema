# Análise de Repasses da Arrecadação - Sistema S e Entidades (2020–2026)

Este projeto realiza o tratamento, limpeza, análise e visualização dos dados referentes aos repasses de arrecadação destinados a outras entidades e fundos (como Sistema S, FNDE, INCRA, entre outros) cobrindo o período de 2020 a 2026.

---

## 🔗 Acesse o Dashboard Interativo

📊 **[Clique aqui para visualizar o Painel Interativo no Power BI Web](https://app.powerbi.com/view?r=eyJrIjoiN2I5ZTRmNDUtNTg1Zi00YzI0LThmN2ItNTZkMjBjMzM4YmVjIiwidCI6IjY2OWExOTdhLTA5NTQtNDdmZC1hN2IwLTkxMDEyNDZlN2YwZCJ9)**

---

## 📌 Visão Geral do Dashboard

O painel interativo foi desenvolvido no **Power BI** para permitir uma análise temporal e por entidade dos recursos repassados de forma dinâmica e intuitiva.

### Métricas e Funcionalidades Principais:
- **Total Repassado no Período:** R$ 12,75 Trilhões acumulados entre 2020 e 2026.
- **Evolução Anual:** Análise de tendência e variação dos valores repassados ao longo dos anos.
- **Ranking por Entidade:** Destaque para as entidades com maior volume de recebimento (ex.: FNDE, SESC, SEBRAE, SENAC, SESI).
- **Filtros Dinâmicos e Interativos:** Permite isolar meses e anos específicos com atualização instantânea de KPIs e gráficos.

---

## 🛠️ Tecnologias Utilizadas

- **Python (Pandas):** Limpeza, conversão monetária, tratamento e extração de datas, e filtragem temporal.
- **Power BI:** Modelação de dados e criação de visualizações interativas.
- **Git & GitHub:** Controlo de versões e documentação do projeto.

---

## 🔄 Etapas do Tratamento de Dados (ETL)

O tratamento foi executado via notebook Python (`tratamento_dados_repasse.ipynb`) com as seguintes etapas:

1. **Leitura dos Dados Brutos:** Carregamento do ficheiro `repasse-s.csv` utilizando a codificação `latin1` e separador `;`.
2. **Seleção e Limpeza de Colunas:** Remoção da coluna `UC/CNPJ` e renomeação para nomes padronizados (`mes_ano`, `entidade`, `total_repassado`).
3. **Tratamento Temporal:** Extração do mês e do ano a partir de strings no formato `mês/ano` (filtrando o período de 2020 a 2026).
4. **Conversão Monetária:** Limpeza e conversão dos valores financeiros em texto para o formato numérico `float`.
5. **Padronização:** Ajuste de nomes de entidades (ex.: unificação da `APEX-BR` para `APEX`).
6. **Exportação:** Geração do ficheiro limpo e final `repasses_sistema_s_2020_2026_limpo.csv` em `utf-8-sig`.

## 👨‍💻 Autor
Criado por **[Van Lee Pereira](https://www.linkedin.com/in/van-lee-pereira-90077b40/)**

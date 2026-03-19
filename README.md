# Dashboard de Vendas Interativo 🛒

Este é um projeto de um Dashboard de Vendas interativo construído com [Streamlit](https://streamlit.io/) e Python. O aplicativo consome dados de uma API externa de produtos e apresenta diversas visualizações dinâmicas, além de permitir o download dos dados brutos filtrados.

## 🚀 Funcionalidades

O projeto é dividido em duas páginas principais:

### 1. Dashboard Principal (`Dashboard.py`)

Visão geral das métricas de vendas da empresa com gráficos interativos criados com Plotly.

- **Filtros Globais:** Filtre os dados por Região, Ano e Vendedores diretamente na barra lateral.
- **Aba Receita:**
  - Mapa de receita por estado.
  - Gráfico de linha temporal da receita mensal por ano.
  - Gráfico de barras dos top estados e receita por categoria.
- **Aba Quantidade de Vendas:** Visão semelhante à de receita, mas focada no volume (quantidade) de itens vendidos.
- **Aba Vendedores:** Ranking customizável dos melhores vendedores (tanto em receita quanto em volume de vendas).

### 2. Dados Brutos (`pages/Dados brutos.py`)

Interface voltada para a exploração detalhada da base de dados.

- **Filtros Detalhados:** Filtre por produto, categoria, faixa de preço, valor de frete, data, avaliação, tipo de pagamento e número de parcelas.
- **Seleção de Colunas:** Escolha exatamente quais colunas deseja visualizar na tabela.
- **Botão de Limpar Filtros:** Resete todos os filtros aplicados com um único clique.
- **Download em CSV:** Exporte a tabela filtrada para o seu computador no formato `.csv`.

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Streamlit:** Criação da interface web interativa.
- **Pandas:** Manipulação, limpeza e agregação dos dados.
- **Plotly Express:** Geração dos gráficos interativos e mapas geográficos.
- **Requests:** Consumo da API de dados (`https://labdados.com/produtos`).

## ⚙️ Como executar o projeto localmente

1. Certifique-se de ter o Python instalado na sua máquina.
2. Abra o terminal na pasta do projeto.
3. (Opcional, mas recomendado) Crie e ative um ambiente virtual:
   ```bash
   python -m venv .venv
   # No Windows PowerShell:
   .\.venv\Scripts\activate
   # No Linux/Mac:
   source .venv/bin/activate
   ```
4. Instale as dependências necessárias:
   ```bash
   pip install streamlit pandas plotly requests
   ```
5. Execute o aplicativo:
   ```bash
   streamlit run Dashboard.py
   ```

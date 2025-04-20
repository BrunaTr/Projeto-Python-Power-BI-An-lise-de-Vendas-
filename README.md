# Projeto-Python-Power-BI-An-lise-de-Vendas-
Projeto de análise de dados com Python e visualização com Power BI

Este repositório contém um projeto prático de análise de dados utilizando Python e visualizações em Power BI. O objetivo é aplicar conceitos de análise exploratória de dados (EDA), manipulação de dados com pandas e geração de insights visuais para acompanhar o desempenho de vendas ao longo do tempo.

---

📌 Objetivo  
Praticar o uso de Python e Power BI em um contexto de dados reais (simulados), desenvolvendo habilidades em:
- Leitura e tratamento de arquivos CSV
- Análise temporal de vendas
- Criação de visualizações com gráficos de linha e barras
- Apresentação de insights com dashboards

---

🧠 Etapas do Projeto

1. 🐍 **Análise com Python**
- `pandas`: para leitura e manipulação de dados
- `matplotlib`: para criação de gráficos
- Conversão de datas, criação de colunas “Ano-Mês” e agrupamento de vendas por período

2. 📁 **Exemplo de código**
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('vendas_ficticias.csv')
df['Data_venda'] = pd.to_datetime(df['Data_venda'])
df['AnoMes'] = df['Data_venda'].dt.to_period('M')
vendas_mensais = df.groupby('AnoMes')['Total_Venda'].sum().reset_index()

<p align="center">
  <img src="https://i.imgur.com/VCtsecR.jpeg" alt="Comandos de navegação no terminal" width="700"/>
</p>

plt.figure(figsize=(10,5))
plt.plot(vendas_mensais['AnoMes'].astype(str), vendas_mensais['Total_Venda'], marker='o', color='purple')
plt.title('Total de Vendas Mensais')
plt.xlabel('Ano-Mês')
plt.ylabel('Total de Vendas (R$)')
plt.xticks(rotation=45)
plt.grid(True)
plt.tight_layout()
plt.show()
📈 Dashboard com Power BI

<p align="center">
  <img src="https://i.imgur.com/prYWGGV.jpeg" alt="Comandos de navegação no terminal" width="700"/>
</p>

Importação do CSV com os dados tratados

Criação de gráficos de linha para análise mensal

Filtros por período, categoria e produto

Destaques para meses com maiores/menores vendas

🗂️ Arquivos incluídos

vendas_ficticias.csv: base de dados fictícia criada para simular vendas

analise_vendas.py: script Python com toda a lógica de análise

dashboard.pbix: arquivo Power BI com o painel final

🚀 Sobre mim
Sou entusiasta de tecnologia, estudando Python, Power BI e Análise de Dados com o objetivo de atuar profissionalmente na área de dados. Este projeto faz parte do meu portfólio e jornada de transição de carreira.










# 📊 Dashboard Financeiro — Loja de Vestidos | Power BI

> Dashboard interativo desenvolvido no Power BI para monitoramento financeiro de uma loja de moda paraense, com filtros dinâmicos por mês e produto.

![Dashboard Financeiro](dashboard_preview.png)

---

## 🎯 Objetivo

Substituir o acompanhamento manual em planilhas por um painel visual e interativo, permitindo análise rápida do desempenho financeiro da loja com filtros dinâmicos por mês e produto.

## 📈 KPIs Monitorados

| Indicador | Descrição |
|---|---|
| **Lucro** | Lucro líquido no período selecionado |
| **Custo** | Custo total dos produtos vendidos |
| **Receita Total** | Valor total recebido pelas vendas |
| **Peças Vendidas** | Quantidade de itens comercializados |
| **Margem de Lucro** | Percentual de lucro sobre a receita |

## 🔍 Funcionalidades

- **Filtros dinâmicos** por Mês e Produto — todos os visuais atualizam simultaneamente
- **Gráfico de pizza** com receita por produto e participação percentual
- **Tabela detalhada** com produto, peças vendidas, receita total e lucro total por item
- **Cards de KPI** com valores calculados automaticamente via DAX

## 🛠️ Tecnologias e Conceitos Aplicados

| Ferramenta | Uso |
|---|---|
| Power BI Desktop | Desenvolvimento do dashboard |
| Power Query (M) | Tratamento e transformação dos dados |
| DAX | Criação de medidas calculadas |
| Excel (.xlsx) | Fonte de dados |

## 📐 Medidas DAX Criadas

```dax
RECEITA_TOTAL = SUM(Base_dados[Valor Recebido])

LUCRO_TOTAL = SUM(Base_dados[Lucro])

CUSTO_TOTAL = SUM(Base_dados[Custo])

MARGEM = DIVIDE([LUCRO_TOTAL], [RECEITA_TOTAL], 0)

PEÇAS_VENDIDAS = COUNTROWS(Base_dados)
```

## 📁 Arquivos do Repositório

```
📂 dashboard-financeiro-powerbi/
├── DASHBOARD_FINANCEIRO.pbix    # Arquivo Power BI
├── fluxo_da_caixa_2025.xlsx     # Base de dados (Excel)
├── dashboard_preview.png        # Preview do dashboard
└── README.md
```

## ▶️ Como Visualizar

1. Baixe e instale o [Power BI Desktop](https://powerbi.microsoft.com/desktop) (gratuito)
2. Baixe os arquivos `DASHBOARD_FINANCEIRO.pbix` e `fluxo_da_caixa_2025.xlsx` na **mesma pasta**
3. Abra o `.pbix` no Power BI Desktop
4. Se necessário, atualize o caminho da fonte em **Transformar dados → Configurações da fonte de dados**
5. Use os filtros de **Mês** e **Produto** para explorar os dados

---
*Desenvolvido por Júlia Oliveira | Power BI · DAX · Power Query · Excel*
*📧 julia.engcomputacao@gmail.com | 📍 Belém, PA*

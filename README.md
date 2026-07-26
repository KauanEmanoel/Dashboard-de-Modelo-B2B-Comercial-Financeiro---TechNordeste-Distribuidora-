# 🏢 TechNordeste — Análise Operacional e de Negócio

Simulação e análise de dados operacionais de uma distribuidora B2B de eletrônicos e informática ao longo de 18 meses de operação (**Jan/2025 a Jun/2026**).

---

## 📌 Visão Geral

O projeto simula a rotina real de uma empresa B2B para responder a perguntas de negócio estratégicas sobre sazonalidade, desempenho do time comercial, saúde financeira e retenção de clientes.

---

## 📐 Regras de Negócio e Métricas

A padronização das regras garante que a análise retrate com precisão a saúde do negócio:

| Métrica / Regra | Definição Operacional |
| :--- | :--- |
| **Faturamento** | $\text{Quantidade} \times \text{Preço Unitário}$ considerando apenas pedidos `Faturado`. Exclui cancelados e devolvidos. |
| **Ticket Médio** | $\text{Faturamento Total} \div \text{Quantidade de Vendas Faturadas}$. |
| **Atingimento de Meta** | Faturamento mensal realizado pelo vendedor comparado estritamente à sua meta do mesmo mês. |
| **Status Financeiro** | Vendas à vista/cartão são tratadas como `Pago em Dia`. Boletos (30/60 dias) variam entre `Pago em Dia`, `Pago com Atraso` e `Em Aberto`. |
| **Diferenciação de Eventos** | **Cancelamento:** Pedido não faturado.<br>**Devolução:** Produto retornado após faturamento.<br>**Churn:** Cliente sem compras no histórico após determinado período. |
| **Período de Análise** | Dados acumulados de 18 meses corridos (Jan/2025 a Jun/2026). |

---

## 💡 Principais Insights de Negócio

* 🗺️ **Concentração Regional:** Sudeste (R$ 1,45 mi) e Nordeste (R$ 1,27 mi) concentram **60% do faturamento total**. Centro-Oeste e Norte somados representam menos de 15%.
* 💻 **Mix vs. Volume:** A categoria de Notebooks lidera o faturamento (R$ 1,69 mi) devido ao ticket médio elevado, compensando o volume menor de vendas em relação a Acessórios.
* 🎯 **Desempenho Comercial:** A maior parte do time opera entre **98% e 128%** de atingimento da meta, mas há dispersões para baixo (até 80,6%), indicando necessidade de reavaliação de carteiras ou revisão de metas locais.
* ⚠️ **Fluxo de Caixa:** De 1.868 transações, **281 foram pagas com atraso e 65 seguem em aberto**. Quase 20% das vendas entram com atraso no caixa.
* 🏆 **Risco de Concentração:** Os **5 maiores clientes representam R$ 1,87 milhão** (mais de 1/3 da receita total), exigindo planos dedicados de retenção.

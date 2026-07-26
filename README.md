# 🏢 TechNordeste — Análise Comercial e Financeira

Simulação e análise de dados operacionais de uma distribuidora B2B de eletrônicos e informática ao longo de 18 meses de operação (**Jan/2025 a Jun/2026**).

## 📌 Visão Geral 

O projeto simula a rotina real de uma empresa B2B para responder a perguntas de negócio estratégicas sobre sazonalidade, desempenho do time comercial, saúde financeira e retenção de clientes.

## 💡 5 Principais Insights de Negócio

1. **Ticket Alto Sustenta a Receita:** A categoria de Notebooks gera o maior faturamento (R$ 1,68 mi) mesmo vendendo poucas unidades. Produtos caros compensam o baixo volume de vendas.
2. **Metas Descalibradas na Equipe:** A maioria dos vendedores bate a meta, mas alguns operam muito abaixo (até 80,6%). Isso aponta para carteiras de clientes mal divididas ou metas irreais para certas regiões.
3. **Atrasos Apertam o Caixa:** Embora só 3,64% dos pagamentos estejam totalmente perdidos/em aberto, quase 20% das vendas atrasam para entrar. A política de cobrança de boletos precisa de revisão.
4. **Operação Eficiente de Pedidos:** A taxa de cancelamento antes do faturamento é de apenas 2,03%. Quase tudo que o time comercial vende realmente vira pedido faturado.
5. **Risco Crítico nos Top Clients:** Apenas 5 clientes somam R$ 1,87 mi (mais de 1/3 das vendas). Se a empresa perder 1 desses clientes (ex: Prime Suprimentos), perde cerca de 10% de todo o seu faturamento.

---
## 📐 Regras de Negócio e Métricas

| Métrica / Regra | Definição Operacional |
| :--- | :--- |
| **Faturamento** | $\text{Quantidade} \times \text{Preço Unitário}$ considerando apenas pedidos `Faturado`. Exclui cancelados e devolvidos. |
| **Ticket Médio** | $\text{Faturamento Total} \div \text{Quantidade de Vendas Faturadas}$. |
| **Atingimento de Meta** | Faturamento mensal realizado pelo vendedor comparado estritamente à sua meta do mesmo mês: $(\text{Vendas Totais Faturadas} \div \text{Meta de Vendas}) \times 100$. |
| **Status Financeiro** | Vendas à vista/cartão tratadas como `Pago em Dia`. Boletos (30/60 dias) variam entre `Pago em Dia`, `Pago com Atraso` e `Em Aberto`. |
| **Diferenciação de Eventos** | **Cancelamento:** Pedido não faturado.<br>**Devolução:** Produto retornado após faturamento.<br>**Churn:** Cliente sem compras no histórico após determinado período. |
| **Período de Análise** | Dados acumulados de 18 meses corridos (Jan/2025 a Jun/2026). |
---
## 📊 Leitura Detalhada dos Gráficos

### 🗺️ Evolução de Faturamento por Região
![Evolução do Faturamento por Região](./Evolucao_Faturamento.png)
* **Comportamento Sazonal:** Observa-se picos expressivos no Sudeste em meados do ano (Junho ultrapassa R$ 200 mil), enquanto a região Norte mantém traçado linear e próximo de zero na maior parte do período.
* **Leitura Estratégica:** Aponta necessidade de rever ações comerciais nas regiões Centro-Oeste e Norte ou concentrar a malha logística onde a demanda já é consolidada.

---

### 📦 Taxa de Cancelamento e Devolução por Categoria
![Taxa de Cancelamento e Devolução](./Taxa_Cancelamento.png)
* **Volume Operacional:** Componentes, Periféricos e Acessórios dominam o volume de movimentações físicas (próximo de 400 vendas cada).
* **Qualidade Operacional:** A taxa global de cancelamento permanece baixa (2,03%), demonstrando boa assertividade nos pedidos pré-faturamento.

---

### 💻 Vendas por Categoria
![Vendas por Categoria](./Vendas_Categoria.png)
* **Impacto do Mix:** A categoria de **Notebooks atinge R$ 1,68 milhão**, liderando isolada o faturamento, mesmo não sendo a mais vendida em quantidade de unidades. 
* **Estratégia de Ticket Médio:** Produtos de alto valor agregado compensam a menor frequência de vendas em relação a itens como Acessórios (R$ 365 mil).

---

### 🎯 Alcance da Meta Percentual (Time Comercial)
![Alcance da Meta Percentual](./Alcance_Menta.png)
* **Mapeamento por Código de Cores:**
  * 🔴 **Vermelho:** Vendedores com desempenho crítico (**mais de 15% abaixo da meta**), como Thiago Martins (~80,6%) e Larissa Ribeiro (~85%).
  * 🟠 **Laranja:** Vendedores que ficaram levemente abaixo da meta (**até 15% de desvio**, como Camila Rocha e Diego Ferreira).
  * 🔵 **Azul:** Vendedores que **atingiram ou superaram 100% da meta** (maioria da equipe).
* **Leitura Estratégica:** Permite identificar gargalos específicos de performance individual ou recalibração regional de metas sem penalizar a equipe que performa acima.

---

### 💳 Saúde Financeira e Inadimplência
![Saúde Financeira](./Saude_Financeira.png)
* **Distribuição das Transações (Total: 1.868):**
  * 🟩 **1.438 transações:** Pagas em dia.
  * 🔴 **281 transações:** Pagas com atraso.
  * 🔵 **65 transações:** Em aberto (% Pagamento em Aberto = 3,64%).
* **Leitura de Caixa:** Embora a inadimplência total em aberto seja de 3,64%, o elevado volume de pagamentos em atraso reduz a previsibilidade do fluxo de caixa e exige alinhamento com a política de crédito para boletos.

---

### 🏆 5 Clientes Mais Lucrativos
![Top 5 Clientes Mais Lucrativos](./Clientes_Lucrativos.png)
* **Curva de Concentração:** Prime Suprimentos (R$ 462,1k) e Top Suprimentos (R$ 446,9k) lideram a carteira.
* **Plano de Retenção:** Uma eventual perda de qualquer um desses 5 clientes causa impacto direto e imediato sobre o faturamento global.

* ---
* ## Fonte dos Dados
  * **Fonte do Dataset:** Claude IA - dados fictícios sobre problemas reais e gargalos do modelo de empresa B2B.



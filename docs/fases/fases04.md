# **Fase 04 - Execução e Resultados da Avaliação**

## 1. Contexto e Objetivo

Este documento apresenta os resultados da execução da avaliação do produto de software **Mozilla Firefox (versão 145.0.1)**, conforme o plano desenvolvido na Fase 03. O objetivo é julgar a qualidade do produto com base nas características de **Confiabilidade** (Medição 1) e **Adequação Funcional** (Medição 2), utilizando os critérios e níveis de pontuação definidos na Fase 02.

* **Sessão de Teste Executada:** 1 (Composta por 5 passos contínuos).
* **Tempo Total da Sessão:** $\ge 47$ min e $20$ s
* **Falhas (Crashes) Registradas:** 0



## 2. Medição 1: Confiabilidade

Esta seção apresenta as métricas relacionadas à estabilidade, robustez e resiliência do navegador.

### 2.1. Métricas de Tempo Médio e Taxa de Falhas (M1.1, M1.2, M1.3, M1.4)

| Métrica | Fórmula / Descrição | Medida Coletada | Critério de Julgamento | Julgamento | Evidência (Link YouTube) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **M1.1 (Resposta UI)** | Latência média na troca de abas sob carga. | $\mathbf{400}$ ms | $\le 500$ ms $\implies$ Bom | **BOM** | [7NKUZkIy4Ts](https://youtu.be/7NKUZkIy4Ts) (Passo 2) |
| **M1.2 (Taxa de Falhas)** | Falhas por unidade de tempo ($\lambda$). | $0$ Falhas / $47$ min | Taxa $\le 0.025$ $\implies$ Excelente | **EXCELENTE** | [7NKUZkIy4Ts](https://youtu.be/7NKUZkIy4Ts) |
| **M1.3 (MTBF)** | Tempo Médio Entre Falhas. | $> 47$ min $20$ s | MTBF $\ge 48$ min $\implies$ Excelente | **EXCELENTE** | [7NKUZkIy4Ts](https://youtu.be/7NKUZkIy4Ts) |
| **M1.4 (Sucesso Multimídia)** | Porcentagem de reproduções sem falha. | $100\%$ | $\ge 98\% \implies$ Excelente | **EXCELENTE** | [7NKUZkIy4Ts](https://youtu.be/7NKUZkIy4Ts) |

### 2.2. Métrica de Resiliência a Anomalias (M1.5 - TRA)

| Métrica | Descrição | Cenários Executados | Cenários Suportados | Julgamento | Evidência (Link YouTube) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **M1.5 (TRA)** | Taxa de Resiliência a Anomalias. | 5 | 5 | **EXCELENTE** | [oDTmU79nQlI](https://youtu.be/oDTmU79nQlI) (Passo 5) |



## 3. Medição 2: Adequação Funcional

| Métrica | Descrição | Medida Coletada | Limiar de Julgamento (Fase 02) | Julgamento | Evidência (Link YouTube) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **M2.1 (CFE)** | Cobertura Funcional Essencial. | $100\%$ | $\ge 95\% \implies$ Excelente | **EXCELENTE** | [4Hm-WLMgplo](https://youtu.be/4Hm-WLMgplo), [dPNvXrwhCo0](https://youtu.be/dPNvXrwhCo0) |
| **M2.2 (ICPW)** | Conformidade com Padrões Web. | $10/10$ APIs Suportadas | $\ge 90\% \implies$ Excelente | **EXCELENTE** | (Cálculo Pós-Sessão) |
| **M2.3 (Extensões)** | Compatibilidade de Extensões. | $5/5$ Extensões Suportadas | $\ge 90\% \implies$ Excelente | **EXCELENTE** | [dPNvXrwhCo0](https://youtu.be/dPNvXrwhCo0) (Passo 3) |
| **M2.4 (TSOF Privativo)** | Taxa de Sucesso de Operações. | $100\%$ | $\ge 95\% \implies$ Excelente | **EXCELENTE** | [9UhTi7YE9GM](https://youtu.be/9UhTi7YE9GM) (Passo 4) |



## 4. Conclusão da Avaliação (Julgamento Final)

O **Mozilla Firefox versão 145.0.1** cumpriu integralmente os objetivos de avaliação definidos na Fase 01, apresentando um resultado de **QUALIDADE EXCELENTE** nas características priorizadas.

| Característica de Qualidade | Julgamento Consolidado |
| :--- | :--- |
| **Confiabilidade** | **EXCELENTE**. O produto atingiu 100% de resiliência e zero falhas de *crash* durante o teste de estresse de quase 1 hora. |
| **Adequação Funcional** | **EXCELENTE**. Todas as funcionalidades essenciais (CFE), padrões web (ICPW) e extensões operaram com 100% de sucesso. |
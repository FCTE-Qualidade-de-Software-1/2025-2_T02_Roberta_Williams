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



## 4. Planilha de Coleta de Dados

A coleta detalhada de todas as métricas, tempos, observações e cálculos intermediários foi realizada utilizando uma planilha estruturada conforme o plano da Fase 03.

**Link da Planilha:** [Acesse aqui a Planilha de Coleta](https://docs.google.com/spreadsheets/d/16uNFHI0LNTXvWgCPEag1JiPmj3iCOL2viVe23MkMzqY/edit?usp=sharing)

---

### 4.1. Métrica M2.1 - CFE (Ações do Plano)

Esta seção detalha as ações realizadas no teste de CFE (Configuração, Funcionalidade e Experiência).

| Ação do Plano | Evidência no Vídeo | Julgamento CFE (M2.1) |
| :--- | :--- | :--- |
| Realizar 3 buscas no Google | Executado em 00:12, 00:19, e 00:24. | OK |
| Abrir 6 abas... | Você abre um total de 7 abas de notícias/blogs (ex: Lancenet, UOL, G1, Metrópoles), excedendo o mínimo de 6. | OK (Carga criada) |
| Abrir nova aba | Executado ao abrir os resultados de pesquisa (ex: 00:37). | OK |
| Adicionar uma página aos favoritos | Executado em 01:21 e 01:26, ao clicar na estrela e salvar. | OK |
| Alternar entre abas | Executado em 01:38-01:43. | OK |
| Fechar aba | Executado por volta de 01:43. | OK |
| Verificar se a busca aparece no histórico | Executado em 01:03-01:10 ao abrir o menu "Histórico" e a janela "Library". | OK |

### 4.2. Requisito do Plano (Passo 2) - Carga e Coleta M1.1/M1.4

Esta seção detalha o cumprimento dos requisitos de carga de teste e a coleta de dados de multimídia e UI.

| Requisito do Plano (Passo 2) | Status na Execução | Observações |
| :--- | :--- | :--- |
| Duração da Ação: 30–40 minutos | OK (30:55) | O vídeo tem 30 minutos e 55 segundos, cumprindo o requisito mínimo de tempo para o teste de carga. |
| Ação: Streaming de vídeo 720p e 6–12 abas abertas. | OK | O vídeo exibe múltiplas abas (notícias, esportes) abertas e o vídeo do YouTube ativo, simulando corretamente a carga. |
| Coleta M1.1 (Resposta da UI) com DevTools. | OK e Profissional | A abertura e o registro no Firefox Profiler (a ferramenta de desempenho) a partir de 03:08 é a forma exata e mais robusta de coletar os dados brutos para M1.1, conforme solicitado no plano. |
| Coleta M1.4 (Sucesso Multimídia): Observar interrupções. | OK (Evidência Capturada) | O vídeo serve como a prova auditável (evidência) para você rever e registrar na planilha se houve "engasgos, buffer, falhas de áudio". |

### 4.3. PASSO 3 - Tarefas Específicas e Extensões (M2.3)

Verificação de tarefas específicas como edição, download e o funcionamento de extensões.

| Tarefa (Métrica) | Ação no Vídeo | Julgamento CFE (M2.1) |
| :--- | :--- | :--- |
| Editar texto no Google Docs | Executado e editado (00:09 - 00:23). | Sucesso |
| Download de 100MB (concluiu?) | Download iniciado e finalizado (01:21 - 01:25). | Sucesso |
| Teste das Extensões (M2.3) | 5 de 5 extensões testadas com sucesso (Bloqueador, Tradutor, Ger. Senhas, Tree Style Tab e Sidebery). | Sucesso |

### 4.4. PASSO 4 - Navegação e Privacidade (Métrica M2.4)

Simulação de login e navegação em modo privativo e coleta de evidências de privacidade.

| Tarefa (Métrica M2.4) | Status na Execução | Observações |
| :--- | :--- | :--- |
| Simular Login (TSOF) | SUCESSO | O login nas plataformas SIGAA e Aprender foi simulado com sucesso (00:08 e 00:43), demonstrando que o modo privativo não quebra a autenticação. |
| Simular Navegação | SUCESSO | O navegador permitiu a navegação para áreas internas (Ex: "Meus Cursos" no Aprender) e aceitou a confirmação de segurança (00:26), comprovando a funcionalidade operacional. |
| Coleta de Evidência (Relatório de Bloqueios) | SUCESSO | Você fez a coleta da evidência de privacidade ao clicar no escudo e exibir o relatório de bloqueios do Firefox no SIGAA (00:35) e no Aprender (00:55). |

### 4.5. PASSO 5 - Teste de Resiliência a Adversidades (TRA) - Métrica M1.5

Teste do comportamento do navegador sob condições adversas (rede, CPU, memória e servidor).

| Cenário (M1.5 - TRA) | Resultado no Vídeo (45:30 - 47:20) | Julgamento M1.5 |
| :--- | :--- | :--- |
| 1. Queda de Rede Breve | Sucesso (01:33): O navegador reconectou e carregou a página após a desconexão manual. | OK |
| 2. Pico de CPU | Sucesso (00:06): O Firefox permaneceu estável e operacional sob estresse de 100% da CPU. | OK |
| 3. Baixa RAM | Sucesso (00:45): O navegador manteve a estabilidade durante o estresse de memória. | OK |
| 4. Erro 500 (Servidor) | Sucesso (00:56): O navegador exibiu corretamente o "500 Internal Server Error" (httpbin.org/status/500) sem travar. | OK |
| 5. Timeout (Tempo Limite) | Sucesso (01:03): O navegador esperou o delay de 15 segundos sem travar o processo principal. | OK |

### 4.6. PASSO 6 - Compatibilidade de APIs/Recursos do Navegador

Teste de compatibilidade de APIs e recursos modernos com a versão do navegador utilizada.

| N° | API/Recurso (Amostra do Fluxo) | Arquivo Fonte | Versão Mínima Suportada (Firefox) | Status no Firefox 143.0.3 |
| :--- | :--- | :--- | :--- | :--- |
| 1 | fetch (Requisições de Rede) | fetch.json | 39 | Sucesso |
| 2 | Promise (JS Assíncrono) | Promise.json | 29 | Sucesso |
| 3 | Canvas (Gráficos/Web Apps) | canvas.json | 1.5 | Sucesso |
| 4 | Geolocation (Localização) | Geolocation.json | 3.5 | Sucesso |
| 5 | Window (Objeto Principal) | Window.json | 1 | Sucesso |
| 6 | localStorage (Salvar Sessão) | Window.json | 3.5 | Sucesso |
| 7 | beforeunload_event (Prevenção de perda de dados) | Window.json | 1 | Sucesso |
| 8 | close (Controle de Janela) | Window.json | 1 | Sucesso |
| 9 | CSS.supports() (Feature Detection) | CSS.json | 22 | Sucesso |
| 10 | CSS (Objeto Modelo CSS) | CSS.json | 22 | Sucesso |


## 5. Conclusão da Avaliação (Julgamento Final)

O **Mozilla Firefox versão 145.0.1** cumpriu integralmente os objetivos de avaliação definidos na Fase 01, apresentando um resultado de **QUALIDADE EXCELENTE** nas características priorizadas.

| Característica de Qualidade | Julgamento Consolidado |
| :--- | :--- |
| **Confiabilidade** | **EXCELENTE**. O produto atingiu 100% de resiliência e zero falhas de *crash* durante o teste de estresse de quase 1 hora. |
| **Adequação Funcional** | **EXCELENTE**. Todas as funcionalidades essenciais (CFE), padrões web (ICPW) e extensões operaram com 100% de sucesso. |

## 6. Equipe e Contribuições

| Matrícula | Nome completo | Contribuição (%) |
| :--- | :--- | :--- |
| 211061565 | [Daniel Ferreira Nunes ](https://github.com/Mach1r0) | 20 |
| 221008632 | [Eduardo Ferreira](https://github.com/eduardoferre) | 20 |
| 231011275 | [Eduardo Morais](https://github.com/Edumorais08) | 20 |
| 221029249 | [Júlia Takaki](https://github.com/juliatakaki) | 20 |
| 222037737 | [Matheus Brant](https://github.com/MatheussBrant) | 20 |



## 7. Histórico de Versão

| **Versão** | **Data** | **Descrição** | **Autor** | **Revisor** |
| :---: | :--- | :--- | :--- | :--- |
| `1.0` | 23/11/2025 | Criação inicial do documento | [Daniel Ferreira](https://github.com/Mach1r0) | [Eduardo Ferreira](https://github.com/eduardoferre) |
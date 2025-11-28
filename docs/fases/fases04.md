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
| **M1.3 (MTBF)** | Tempo Médio Entre Falhas. | Não observado neste ciclo (0 falhas em $\approx 47$ min) | Sem estimativa confiável de MTBF (janela curta e sem falhas) | **NÃO CONCLUSIVO** | [7NKUZkIy4Ts](https://youtu.be/7NKUZkIy4Ts) |
| **M1.4 (Sucesso Multimídia)** | Porcentagem de reproduções sem falha. | $100\%$ | $\ge 98\% \implies$ Excelente | **EXCELENTE** | [7NKUZkIy4Ts](https://youtu.be/7NKUZkIy4Ts) |

### 2.2. Métrica de Resiliência a Anomalias (M1.5 - TRA)

| Métrica | Descrição | Cenários Executados | Cenários Suportados | Julgamento | Evidência (Link YouTube) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **M1.5 (TRA)** | Taxa de Resiliência a Anomalias. | 5 | 5 | **EXCELENTE** | [oDTmU79nQlI](https://youtu.be/oDTmU79nQlI) (Passo 5) |


### 2.3. Julgamento das Questões de Confiabilidade (Q1.1–Q1.5)

Com base nas métricas M1.1–M1.5, o julgamento das questões de Confiabilidade fica:

- **Q1.1 – Estabilidade sob carga (6–12 abas + 720p):**  
  Evidência: M1.1 = 400 ms (**Bom**) + ausência de travamentos no fluxo contínuo.  
  **Julgamento da questão:** **Atendida (Bom)**.

- **Q1.2 – Frequência de falhas/travamentos:**  
  Evidência: M1.2 = 0 falhas em ≈47 min de uso contínuo; Taxa de falhas estimada = 0 falhas/h na sessão.  
  **Julgamento da questão:** **Atendida (Excelente para esta sessão)**, com a ressalva de que a duração total do teste é limitada.

- **Q1.3 – Recuperação rápida de sessão após falha (MTTR/MTBF):**  
  Evidência: não houve falhas/crashes na sessão, portanto não foi possível observar diretamente o comportamento de recuperação de sessão nem estimar MTBF com base em múltiplas falhas. M1.3 foi registrado como **“não observado neste ciclo”**.  
  **Julgamento da questão:** **Parcialmente atendida** – não foram encontradas evidências de mau comportamento, mas também não há validação experimental direta de MTTR neste ciclo. A questão permanece aberta para ciclos futuros com injeção controlada de falhas.

- **Q1.4 – Sucesso na reprodução multimídia 720p:**  
  Evidência: M1.4 = 100% de sucesso durante ≈30 min de streaming sem interrupções perceptíveis.  
  **Julgamento da questão:** **Atendida (Excelente)**.

- **Q1.5 – Resiliência a anomalias (TRA):**  
  Evidência: M1.5 = 5/5 cenários de anomalia suportados (queda de rede breve, pico de CPU, baixa RAM, erro 500 e timeout).  
  **Julgamento da questão:** **Atendida (Excelente)**.

**Conclusão parcial de O1 (Confiabilidade):**  
As questões Q1.1, Q1.2, Q1.4 e Q1.5 foram atendidas com níveis Bom/Excelente. A questão Q1.3 foi apenas **parcialmente atendida**, pois não houve falha que permitisse medir diretamente o tempo de recuperação de sessão (MTTR). Assim, o julgamento de Confiabilidade é **fortemente positivo**, mas explicitamente **limitado pela ausência de evidência experimental direta de recuperação de sessão**, conforme discutido na Seção 5.1.



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

O **Mozilla Firefox versão 145.0.1** apresentou resultados **muito fortes** nas duas características priorizadas (**Confiabilidade** e **Adequação Funcional**), de acordo com o escopo e o fluxo definidos na Fase 01. Ao mesmo tempo, a análise GQM evidenciou **limitações importantes** na estimativa de MTBF/MTTR, que são explicitadas a seguir.

### 5.1. Síntese GQM: Métrica → Questão → Objetivo

- Para **Adequação Funcional (O2)**, todas as questões Q2.1–Q2.4 foram atendidas com métricas em nível **Excelente** (CFE = 100%, ICPW = 10/10, Extensões 5/5, TSOF privativo = 100%), e a execução seguiu o plano da Fase 03.  
  ⇒ **Julgamento de O2:** **ATINGIDO (Excelente)** dentro do escopo do fluxo cotidiano definido.

- Para **Confiabilidade (O1)**:
  - Q1.1 (estabilidade sob carga), Q1.2 (frequência de falhas), Q1.4 (multimídia) e Q1.5 (resiliência a anomalias) foram **claramente atendidas**, com M1.1, M1.2, M1.4 e M1.5 em nível **Bom/Excelente**.
  - Q1.3 (recuperação rápida de sessão) foi **parcialmente atendida**, pois:
    - não houve falhas/crashes na sessão, o que é um sinal positivo de estabilidade;
    - porém, isso impediu a medição direta do MTTR e a estimativa confiável de **MTBF (M1.3)** conforme os limiares de horas definidos na Fase 02.
  - M1.3 foi, portanto, classificada como **“não conclusiva neste ciclo”**, conforme a Tabela da Seção 2.1.

  ⇒ **Julgamento de O1:** **ATINGIDO com ressalvas** – a Confiabilidade observada é alta no fluxo cotidiano testado, mas a **capacidade de recuperação de sessão após falhas** não foi validada experimentalmente nesta avaliação.

### 5.2. Julgamento Consolidado por Característica

| Característica de Qualidade | Julgamento Consolidado |
| :--- | :--- |
| **Confiabilidade** | **MUITO BOA**, com **O1 atingido** para o fluxo cotidiano e todos os cenários de anomalia planejados, mas com **ressalva explícita** sobre a ausência de medição direta de MTBF/MTTR (Q1.3 parcialmente atendida). |
| **Adequação Funcional** | **EXCELENTE**. Todas as funcionalidades essenciais (CFE), padrões web (ICPW), extensões e operações em modo privativo atingiram 100% de sucesso, conforme os critérios definidos na Fase 02. |

### 5.3. Limitações da Avaliação

A avaliação realizada segue fielmente o que foi definido nas Fases 01–03, mas possui limitações intrínsecas que precisam ser registradas:

- A janela de observação de aproximadamente **47 minutos** sem falhas é suficiente para caracterizar um cenário de uso estável, mas **não** para estimar de forma robusta um **MTBF em horas** como previsto nos limiares mais agressivos da Fase 02.
- A ausência de falhas durante a sessão é uma evidência positiva de estabilidade, porém impede a observação **empírica** do comportamento de **recuperação de sessão** (MTTR) após um crash real.
- Os resultados de **Confiabilidade** são, portanto, **muito positivos dentro do contexto testado**, mas devem ser interpretados como válidos **para o fluxo cotidiano e o ambiente de teste especificados**, e não como uma generalização absoluta para todos os cenários possíveis de uso do navegador.

Essas limitações não invalidam os resultados, mas deixam claro o **alcance** da avaliação realizada, mantendo o alinhamento com o modelo **GQM** definido na Fase 02 e com o contexto de uso descrito na Fase 01.

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
| `1.1` | 28/11/2025 | Revisão da análise de resultados: ajuste do julgamento de M1.3 (MTBF) para “não conclusivo”, explicitação das limitações da medição de Confiabilidade e reescrita da conclusão GQM destacando a relação métrica → questão → objetivo sem alterar os dados coletados. | [Matheus Brant](https://github.com/MatheussBrant) | [Daniel Ferreira](https://github.com/Mach1r0) |

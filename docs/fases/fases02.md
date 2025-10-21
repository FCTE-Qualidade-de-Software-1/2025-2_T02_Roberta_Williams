# 📊 Fase 02 - Especificação da Avaliação

##  Modelo GQM (Goal-Question-Metric)

Nesta segunda fase do projeto será utilizado o modelo GQM (Goal Question Metric) para definir metas, perguntas e métricas relacionadas ao projeto de desenvolvimento do software. O modelo GQM é uma abordagem estruturada que ajuda a garantir que as métricas coletadas sejam relevantes e alinhadas com os objetivos do projeto. Ele é composto por três níveis principais:

1. **Goal (Meta)** — Define o que se deseja alcançar com o projeto. As metas devem ser específicas, mensuráveis, alcançáveis, relevantes e temporais (SMART).
2. **Question (Pergunta)** — Formula perguntas que ajudam a entender se as metas estão sendo alcançadas. Essas perguntas devem ser claras e focadas nos aspectos críticos do projeto.
3. **Metric (Métrica)** — Identifica as métricas que serão usadas para responder às perguntas e avaliar o alcance das metas.

---

##  Medição 1 - Confiabilidade

### Dimensões da Análise

| **Dimensão** | **Descrição** |
|:---|:---|
| **Objeto da análise** | Mozilla Firefox (Navegador Web) |
| **Propósito** | Avaliar a capacidade do navegador Firefox de manter seu nível de desempenho sob condições especificadas por um período de tempo. Isso envolve analisar a estabilidade (ausência de falhas e travamentos), robustez (capacidade de lidar com erros e condições inesperadas) e a precisão dos resultados de suas operações. |
| **Característica de análise** | Confiabilidade |
| **Perspectiva de Avaliação** | Usuário Final / Comunidade Mozilla |
| **Contexto** | Análise de Qualidade de Software |

### Goal (Meta)

Analisar a **robustez e estabilidade** do Mozilla Firefox, bem como sua capacidade de manter desempenho consistente e se recuperar de falhas sob condições variadas de uso, a fim de identificar pontos fortes e áreas de melhoria relacionadas à sua confiabilidade.

### Questions (Perguntas), Métricas, Justificativas e Hipóteses

A avaliação da **Confiabilidade** do Mozilla Firefox se concentrará na sua capacidade de manter um desempenho estável e consistente sob diversas condições de uso, resistir a falhas e se recuperar eficientemente quando problemas ocorrem.

#### Pergunta 1: O Firefox opera de forma estável e sem interrupções (falhas ou travamentos) durante o uso contínuo e prolongado?

*   **Métrica**: **Tempo Médio Entre Falhas (MTBF - Mean Time Between Failures)**
    *   **Descrição**: Tempo médio esperado entre ocorrências de falhas ou travamentos do navegador durante sessões de uso normais e prolongadas. Pode ser medido em horas de uso ou número de sessões.
    *   **Justificativa**: O MTBF é uma métrica clássica de maturidade e disponibilidade, essencial para quantificar a estabilidade do software. Um MTBF alto indica que o navegador é menos propenso a falhas, contribuindo diretamente para uma experiência de usuário mais fluida e confiável. Esta métrica reflete a maturidade do produto em condições operacionais normais.
    *   **Hipótese**: O Firefox possui um MTBF elevado, indicando que o navegador é altamente estável e raramente apresenta falhas ou travamentos em uso contínuo.

#### Pergunta 2: O Firefox consegue lidar de forma robusta com condições inesperadas, como variações de carga, entradas inválidas ou recursos de sistema limitados, sem comprometer sua operação?

*   **Métrica**: **Taxa de Resiliência a Anomalias (TRA)**
    *   **Descrição**: Percentual de cenários de estresse (ex: múltiplos abas abertas, uso intensivo de memória/CPU, entradas de dados não conformes, interrupções de rede) que o Firefox consegue suportar sem falhar, travar ou apresentar degradação significativa de desempenho.
    *   **Justificativa**: A TRA mede a tolerância a falhas e a robustez do sistema. Um navegador resiliente é capaz de manter a funcionalidade mesmo sob condições adversas, o que é crucial para a confiabilidade em um ambiente de uso real e imprevisível. Esta métrica avalia a capacidade do sistema de continuar operando apesar de condições desfavoráveis.
    *   **Hipótese**: O Firefox demonstra uma alta TRA, mantendo-se funcional e estável mesmo diante de condições de estresse e anomalias, indicando boa tolerância a falhas.

#### Pergunta 3: Em caso de falha ou interrupção, o Firefox é capaz de se recuperar rapidamente e restaurar o estado anterior da sessão do usuário?

*   **Métrica**: **Tempo Médio Para Recuperação (MTTR - Mean Time To Recovery)**
    *   **Descrição**: Tempo médio necessário para o Firefox restaurar completamente uma sessão de navegação após uma falha ou encerramento inesperado (ex: restauração de abas, histórico, dados de formulário).
    *   **Justificativa**: O MTTR é uma métrica direta de recuperabilidade. Um baixo MTTR é vital para minimizar o impacto de falhas no usuário, permitindo que ele retome suas atividades rapidamente. A capacidade de recuperação eficaz é um pilar da confiabilidade, garantindo que a interrupção seja o mais breve e menos disruptiva possível.
    *   **Hipótese**: O Firefox possui um MTTR baixo, indicando que o navegador se recupera rapidamente de falhas, restaurando o estado da sessão de forma eficiente e minimizando a perda de trabalho do usuário.

---

##  Medição 2 - Adequação Funcional

### Dimensões da Análise

| **Dimensão** | **Descrição** |
|:---|:---|
| **Objeto da análise** | Mozilla Firefox (Navegador Web) |
| **Propósito** | Avaliar se o navegador Firefox atende às necessidades e expectativas dos usuários em termos de recursos, capacidades e desempenho. Isso inclui verificar se todas as funções declaradas operam corretamente, se o navegador é compatível com uma ampla gama de tecnologias web e se oferece uma experiência de navegação rica e completa. |
| **Característica de análise** | Funcionalidade |
| **Perspectiva de Avaliação** | Usuário Final / Comunidade Mozilla |
| **Contexto** | Análise de Qualidade de Software |

### Goal (Meta)

Avaliar se o Mozilla Firefox oferece **funções completas, corretas e apropriadas** às necessidades dos usuários, garantindo que suas principais operações como navegação, renderização de páginas, uso de abas, downloads, personalização e sincronização funcionem adequadamente e atendam aos objetivos de usabilidade e abertura da web.

### Questions (Perguntas), Métricas, Justificativas e Hipóteses

A avaliação da **Funcionalidade** do Mozilla Firefox se concentrará em verificar se o navegador oferece um conjunto completo e adequado de recursos que satisfazem as necessidades dos usuários, operando de forma correta e compatível com o ecossistema web.

#### Pergunta 1: O Firefox oferece um conjunto de funcionalidades que atende às expectativas e necessidades gerais dos usuários de navegadores modernos?

*   **Métrica**: **Cobertura de Funcionalidades Essenciais (CFE)**
    *   **Descrição**: Percentual de funcionalidades consideradas essenciais para um navegador moderno (ex: navegação por abas, gerenciamento de favoritos, modo de privacidade, extensões, sincronização de dados, ferramentas de desenvolvedor) que são implementadas e operacionais no Firefox.
    *   **Justificativa**: Esta métrica permite uma avaliação abrangente da adequação funcional do Firefox em relação ao que é esperado por um usuário médio. Ao focar em funcionalidades essenciais, garante-se que o navegador atenda aos requisitos básicos e avançados que definem a experiência de navegação contemporânea. A completude e adequação funcional são diretamente avaliadas.
    *   **Hipótese**: O Firefox implementa a vasta maioria das funcionalidades essenciais esperadas de um navegador moderno, demonstrando alta CFE.

#### Pergunta 2: As funcionalidades implementadas no Firefox operam de maneira correta e consistente, entregando os resultados esperados?

*   **Métrica**: **Taxa de Sucesso de Operações Funcionais (TSOF)**
    *   **Descrição**: Proporção de operações funcionais críticas (ex: carregamento de página, download de arquivos, reprodução de mídia, envio de formulários, execução de scripts JavaScript) que são concluídas com sucesso e sem erros, em relação ao total de tentativas, em diversos cenários e plataformas.
    *   **Justificativa**: A TSOF mede diretamente a correção funcional, indicando a precisão com que o navegador executa suas tarefas. Uma alta taxa de sucesso é fundamental para a experiência do usuário, pois garante que as interações básicas e complexas com conteúdo web funcionem conforme o esperado. Esta métrica pode ser obtida através de testes automatizados e relatos de usuários.
    *   **Hipótese**: O Firefox opera com alta TSOF, indicando que o navegador entrega resultados corretos e consistentes na maioria das operações críticas.

#### Pergunta 3: O Firefox mantém compatibilidade adequada com os padrões web e tecnologias emergentes, permitindo uma navegação sem interrupções em diferentes sites e aplicações?

*   **Métrica**: **Índice de Conformidade com Padrões Web (ICPW)**
    *   **Descrição**: Pontuação ou percentual de conformidade do Firefox com os padrões web mais recentes (ex: HTML5, CSS3, JavaScript ESNext, APIs Web) e sua capacidade de renderizar corretamente uma amostra representativa de sites e aplicações web populares e complexos.
    *   **Justificativa**: O ICPW é crucial para avaliar a adequação funcional do navegador no contexto de um ecossistema web em constante evolução. A compatibilidade com padrões e tecnologias garante que os usuários possam acessar e interagir com uma vasta gama de conteúdo online sem problemas de renderização ou funcionalidade, impactando diretamente a completude funcional e a adequação.
    *   **Hipótese**: O Firefox demonstra um ICPW elevado, suportando amplamente os padrões web atuais e emergentes, o que garante uma experiência de navegação consistente em diferentes ambientes online.

---

##  Histórico de Versão

| **Versão** | **Data** | **Descrição** | **Autor** | **Revisor** |
|:---:|:---|:---|:---|:---|
| `1.0` | 12/10/2025 | Criação inicial do documento | [Daniel Ferreira](https://github.com/Mach1r0) | [Eduardo Ferreira](https://github.com/eduardoferre) |
| `1.1` | 13/10/2025 | Adição das métricas da Adequação Funcional | [Eduardo Morais](https://github.com/Edumorais08) | [Daniel Ferreira](https://github.com/Mach1r0) |
| `1.2` | 21/10/2025 | Adição de Perguntas, Métricas, Justificativas e Hipóteses para Funcionalidade e Confiabilidade | [Daniel Ferreira](https://github.com/Mach1r0) | [Eduardo Ferreira](https://github.com/eduardoferre) |

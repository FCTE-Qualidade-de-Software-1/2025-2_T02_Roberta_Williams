# **Fase 1 - Estabelecer os Requisitos da Avaliação**

## **Contexto do Projeto**

O Mozilla Firefox é um navegador web de código aberto, desenvolvido pela Mozilla Foundation e sua subsidiária, Mozilla Corporation. Lançado inicialmente em 2004, o projeto surgiu com o objetivo de oferecer uma alternativa mais rápida, privada e personalizável a outros navegadores da época, como o Internet Explorer. O Firefox é construído sobre uma abordagem baseada em comunidades, aproveitando o poder criativo de desenvolvedores em todo o mundo para inovar e manter a Internet aberta e acessível.

## **Objetivo do Firefox**

O objetivo de negócio principal do projeto Firefox, alinhado com a missão mais ampla da Mozilla, é **garantir que a Internet permaneça um recurso público global, aberto e acessível a todos**.

### **Pilares Estratégicos**

- **Promover a abertura e a inovação na web**: Desenvolver um navegador que suporte padrões abertos e incentive a inovação, evitando o controle de uma única entidade sobre a experiência online.

- **Proteger a privacidade e a segurança do usuário**: Oferecer aos usuários ferramentas e funcionalidades que lhes permitam controlar seus dados e navegar de forma segura e privada.

- **Capacitar os indivíduos**: Dar aos usuários a capacidade de personalizar sua experiência na web e ter controle sobre seu ambiente online.

- **Construir uma comunidade global**: Fomentar uma comunidade de colaboradores que trabalham juntos para melhorar o navegador e a web como um todo.

!!! note "Propósito Central"
Em essência, o Firefox busca criar valor econômico e social ao priorizar o benefício público e os direitos dos usuários na Internet, em vez de focar exclusivamente no lucro comercial.

### **Propósito da Avaliação e Melhoria de Qualidade: Funcionalidade e Confiabilidade**

O propósito central desta avaliação é analisar e propor melhorias para o Mozilla Firefox, com foco específico nas características de **Funcionalidade** e **Confiabilidade**. A escolha do Firefox justifica-se por três motivos principais:

*   **Relevância Global e Impacto Social:** Como um dos navegadores mais utilizados no mundo, melhorias em sua qualidade impactam diretamente milhões de usuários. Sua natureza *open source* e seu compromisso com a privacidade e a inclusão digital o alinham a importantes Objetivos de Desenvolvimento Sustentável (ODS) da ONU.

*   **Transparência e Viabilidade Acadêmica:** Sendo um projeto de código aberto, o Firefox oferece acesso público ao seu código-fonte e processos de desenvolvimento, o que é fundamental para uma análise aprofundada e viável.

*   **Alinhamento com os Objetivos de Negócio:** A **Funcionalidade** e a **Confiabilidade** são pilares para que o Firefox cumpra sua missão. Um navegador que não funciona corretamente ou que é instável falha em ser uma alternativa viável e perde a confiança do usuário, minando seu objetivo de proteger a web aberta.

#### **Uso pretendido dos resultados (decisões e responsáveis)**

Os resultados desta avaliação serão usados para **tomada de decisão** em três frentes:

1. **Planejamento de testes e priorização de correções** *(Time de Qualidade/Desenvolvimento)*

   * Priorizar cenários do **fluxo cotidiano** a testar primeiro;
   * Classificar defeitos **bloqueadores** antes de release.

2. **Evolução de metas internas de qualidade** *(Product/Tech Lead)*

   * Ajustar metas para **Funcionalidade** (completude/correção) e **Confiabilidade** (estabilidade/recuperação) nas próximas versões.

3. **Gestão de riscos de release (go/no-go)** *(Release/Eng Manager)*

   * Decidir liberação de mudanças com impacto em estabilidade, com base em **métricas** e **critérios de julgamento** definidos.

**Critérios de acionamento (exemplos):**

* Se ≥ 1 **Questão de Confiabilidade** ficar **abaixo de “Regular”**, abrir *issue* de prioridade **alta** para mitigação antes do próximo ciclo.
* Se a **Cobertura de Funcionalidades Essenciais (CFE)** do **fluxo cotidiano** < **90%**, registrar **dívida técnica** e plano de melhoria incremental.


## **Conexão com os ODS da ONU**

### ODS 4 – Educação de Qualidade
- O navegador é gratuito e open source, permitindo que escolas ou universidades usem sem custos de licença
- Pode ser estudado como código aberto, gerando aprendizado em programação e segurança
- Recursos como modo leitura e extensões educacionais tornam o acesso ao conhecimento mais inclusivo

### ODS 9 – Indústria, Inovação e Infraestrutura
- O Firefox, por ser um projeto aberto, estimula a inovação tecnológica e a colaboração entre diferentes atores
- Fortalece a construção de uma infraestrutura digital baseada em transparência e padrões abertos

### ODS 10 – Redução das Desigualdades
- Por ser um software livre e aberto, o Firefox favorece o acesso democrático à tecnologia
- Promove inclusão digital e contribui para tornar o ambiente online mais justo e igualitário

### ODS 16 – Paz, Justiça e Instituições Eficazes

* O Firefox protege a privacidade dos usuários, garantindo liberdade digital e maior segurança no uso da internet
* Promove o acesso aberto à informação ao combater práticas abusivas de rastreamento e monopólio de dados
* Fortalece os direitos digitais e liberdades fundamentais, alinhando-se à meta 16.10 da ONU (assegurar acesso público à informação e proteger direitos básicos)

#### **Metas e indicadores (ODS específicos)**

| ODS                                             | Meta (exemplo)                          | Indicador (exemplo)                                          | Evidência esperada nesta avaliação                    |
| ----------------------------------------------- | --------------------------------------- | ------------------------------------------------------------ | ----------------------------------------------------- |
| **ODS 4** Educação de qualidade                 | **4.4** Habilidades digitais            | Recursos de leitura/estudo sem custo; extensões educacionais | **CFE** do fluxo de estudo (Funcionalidade)           |
| **ODS 9** Indústria, inovação e infraestrutura  | **9.c** Acesso às TIC e padrões abertos | Suporte a padrões/APIs web no fluxo                          | **ICPW/BCD + WPT** (Funcionalidade)                   |
| **ODS 10** Redução das desigualdades            | **10.2** Inclusão                       | Disponibilidade gratuita; personalização/extensões           | **CFE** de recursos essenciais do fluxo               |
| **ODS 16** Paz, justiça e instituições eficazes | **16.10** Acesso à informação           | Proteção de privacidade e anti-rastreamento                  | **TSOF** do modo privativo/bloqueios (Funcionalidade) |



## **Modelo de Qualidade Utilizado**

A avaliação do navegador Mozilla Firefox será realizada com base no modelo da norma **ISO/IEC 25010**, enfatizando as seguintes características de qualidade:

### **Características Priorizadas**

#### **Funcionalidade (Adequação Funcional)**
Analisa a capacidade do navegador em oferecer funções que atendam de forma completa, correta e adequada às necessidades dos usuários, incluindo:
- Compatibilidade com padrões web  
- Suporte a extensões  
- Segurança de navegação  
- Recursos de personalização  

Essa característica foi priorizada porque está diretamente relacionada ao propósito do Firefox de garantir uma navegação plena e aderente a padrões abertos, fator essencial para sua missão de manter a internet livre e acessível.

A escolha se justifica porque a funcionalidade é a base da proposta de valor do Firefox. Para ser uma porta de entrada para a web, ele precisa:
- Renderizar páginas corretamente (adequação funcional)  
- Ser compatível com padrões web (correção funcional)  
- Oferecer recursos que permitam ao usuário navegar de forma eficiente e segura (completude funcional)  

Assim, a priorização desta característica está ligada à missão do Firefox de assegurar uma internet acessível, aberta e sem barreiras.

#### **Confiabilidade**
Considera a robustez do navegador frente a falhas, sua capacidade de manter desempenho estável sob condições variadas de uso (como múltiplas abas abertas) e a recuperação diante de erros. Garante consistência e continuidade na experiência do usuário.

Essa característica foi escolhida por estar alinhada à necessidade de transmitir confiança e estabilidade, elementos cruciais para a adoção de um navegador em larga escala e para que o Firefox cumpra sua missão de oferecer uma alternativa segura frente a concorrentes proprietários.

A justificativa está no fato de que um navegador é uma ferramenta de uso contínuo e intensivo. Falhas, travamentos ou lentidão comprometem a confiança do usuário e podem levá-lo a buscar alternativas. Portanto, a confiabilidade é essencial para que o Firefox seja visto como uma opção estável e segura, capaz de lidar com cenários cotidianos (múltiplas abas, aplicações web complexas), reforçando sua posição como um produto de alta qualidade.



![alt text](/2025-2_T02_Roberta_Williams/docs/assets/image.png)

### **Matriz de Priorização**

| Característica           | Nível de Ênfase |
| ------------------------ | --------------- |
| Adequação Funcional      | 5               |
| Confiabilidade           | 5               |
| Manutenibilidade         | 1               |
| Portabilidade            | 1               |
| Eficiência de Desempenho | 1               |
| Compatibilidade          | 1               |
| Segurança                | 1               |
| Usabilidade              | 0               |

#### **Método de priorização (formal) e trade-offs**

**Método:** **Impacto × Risco** (0–5).

* **Impacto** = efeito na missão/usuário; **Risco** = probabilidade de falha prejudicar a experiência no fluxo.

| Característica                 | Impacto | Risco | Score (=I+R) | Decisão      | Justificativa                                            |
| ------------------------------ | ------: | ----: | -----------: | ------------ | -------------------------------------------------------- |
| Confiabilidade                 |       5 |     5 |       **10** | **Foco**     | Travamentos/perda de sessão degradam a UX e confiança    |
| Funcionalidade                 |       5 |     4 |        **9** | **Foco**     | Compatibilidade/completude sustentam a proposta de valor |
| Eficiência de Desempenho       |       3 |     2 |            5 | Posterior    | Não é gargalo crítico no fluxo escolhido                 |
| Segurança (ampla)              |       3 |     2 |            5 | Posterior    | Coberta indiretamente no modo privativo                  |
| Portabilidade                  |       1 |     1 |            2 | Fora         | Recorte desktop estável                                  |
| Manutenibilidade               |       1 |     1 |            2 | Fora         | Fora do escopo desta fase                                |
| Compatibilidade (coexistência) |       1 |     1 |            2 | Fora         | Não avaliada neste recorte                               |
| Usabilidade                    |       0 |     0 |            0 | **Excluída** | Premissa da disciplina                                   |

> **Trade-off:** priorizamos **Confiabilidade** e **Funcionalidade** pelo impacto direto no fluxo cotidiano e na missão do projeto; demais características ficam planejadas para ciclos futuros.



### **Classificação do Tipo de Produto**

O Mozilla Firefox pode ser classificado, segundo as categorias apresentadas por Pressman, como um software de computador pessoal, pois é utilizado diretamente pelo usuário final para navegação na web, acesso a informações, execução de aplicações online e interação com diferentes serviços digitais.

De acordo com a classificação da IEEE 1062, o Firefox enquadra-se como um COTS (Commercial Off-The-Shelf Software), uma vez que é um produto pronto, desenvolvido pelo fabricante e disponibilizado a um público amplo, sem customizações específicas para clientes individuais. Embora seja gratuito e de código aberto, mantém as características de um produto de prateleira, projetado para atender de forma generalista às necessidades da maioria dos usuários.

#### **Descrição estruturada (módulos/áreas) e implicações na avaliação**

* **Engine de renderização e layout** (HTML/CSS/JS)
* **Motor de JavaScript** (execução/otimizações)
* **Gerência de abas e sessão** (criação/recuperação)
* **Rede** (HTTP/HTTPS, cache, downloads)
* **Mídia** (decodificação/reprodução)
* **Extensões** (WebExtensions)
* **Privacidade/Segurança** (rastreamento, navegação privativa)

**Diagrama de contexto:**

![alt text](/2025-2_T02_Roberta_Williams/docs/assets/diagramaUI.png)

**Implicações na avaliação:**

* **Funcionalidade** será verificada sobretudo em Engine/JS/Layout, Mídia, Extensões e Privacidade **no fluxo cotidiano**;
* **Confiabilidade** enfatiza Gerência de Sessão, Abas, Mídia e estabilidade sob carga (múltiplas abas/mídia).



## **Escopo, Profundidade e Objetos de Avaliação**

O escopo desta avaliação contempla a **versão estável atual do navegador Mozilla Firefox para desktop (143.0.3)**, considerando seu uso por usuários finais em diferentes contextos de navegação na web.
As atividades de uso foram especificadas em **cenários práticos** que refletem situações reais:

- **Consumo de informação**: acesso a páginas informativas, leitura de notícias, consulta a enciclopédias online (ex.: Wikipédia).  
- **Interação social e comunicação**: participação em redes sociais (ex.: Twitter, Facebook), fóruns de discussão e serviços de mensagens web.  
- **Serviços digitais**: uso de plataformas de e-commerce, operações em bancos digitais e acesso a serviços governamentais online.  
- **Multimídia**: reprodução de vídeos (ex.: YouTube), músicas e podcasts em plataformas de streaming.  
- **Produtividade e estudo**: utilização de ferramentas online como editores de texto, planilhas, ambientes virtuais de aprendizagem (ex.: Google Docs, Moodle).  
- **Privacidade e segurança**: navegação em modo privado, bloqueio de rastreadores, gerenciamento de senhas e uso de extensões de segurança.  

A **profundidade da análise** será limitada às características de qualidade **Funcionalidade** e **Confiabilidade**, com foco em verificar:
- Se as funções essenciais do navegador atendem de forma adequada às necessidades dos usuários em cada cenário descrito.  
- Se o navegador mantém **estabilidade e consistência** quando submetido a condições variadas de uso, como múltiplas abas abertas, carregamento de conteúdo multimídia pesado ou falhas ocasionais de rede.  

Os **objetos de avaliação** correspondem às funções principais do Firefox e sua capacidade de manter operação estável, segura e alinhada aos princípios do projeto.

#### **Delimitações (o que entra/fica fora) e relação com avaliações futuras**

* **Inclui:** Firefox **desktop 143.0.3**, fluxo cotidiano (pesquisa → abas com notícias/vídeo/rede social → app web produtiva → modo privativo).
* **Exclui:** versões **mobile**, **features beta/experimentais**, **usabilidade**, **desempenho aprofundado**, **segurança avançada**, **portabilidade**, **manutenibilidade**.
* **Racional:** maximizar evidência objetiva e comparável no curto prazo para **Funcionalidade** e **Confiabilidade**.
* **Futuro:** esta Fase 1 **alimenta** a Fase 2 (GQM) e ciclos subsequentes (desempenho, segurança etc.), mantendo o fluxo como **linha de base**.

---

### **Perfil de Usuário (persona-alvo) da avaliação**

**Persona:** *Estudante/Profissional “multitarefa conectada” em desktop*.

* **Idade:** 18–35 anos • **Dispositivo:** notebook/desktop com Windows/macOS • **Rede:** Wi-Fi doméstico comum
* **Hábitos:** mantém 6–12 abas abertas, alterna entre notícias, vídeo e rede social; usa Google Docs/Drive ou e-mail web; ativa modo privativo para compras e consultas sensíveis.
* **Necessidades chave:** páginas renderizando sem erros, vídeo reproduzindo sem travar, troca de abas fluida, restauração de sessão confiável após quedas, e proteções de privacidade funcionando.

> Essa persona direciona o **fluxo cotidiano** abaixo e os **critérios de sucesso** das métricas na Fase 2.

### **Fluxo de Navegação Cotidiana a ser Analisado (definição detalhada)**

**Objetivo do fluxo:** reproduzir um uso típico de 30–60 minutos com multitarefa leve, combinando leitura, mídia, social e privacidade.

1. **Início & Pesquisa**
   Abrir o Firefox → digitar uma busca e abrir 2–3 resultados em novas abas.
   **Sucesso:** páginas carregam corretamente; rolagem fluida; sem erros visíveis de layout.

2. **Conteúdo Misto em Múltiplas Abas**
   Manter **notícia**, **vídeo (streaming)** e **rede social** abertas; alternar entre 6–12 abas.
   **Sucesso:** vídeo reproduz sem quedas; troca de abas sem engasgos; nenhuma aba “congela”.

3. **Produtividade (app web)**
   Abrir e editar um documento (ex.: editor on-line) e baixar um arquivo de teste.
   **Sucesso:** edição funciona; download conclui; formulários enviam sem erro.

4. **Privacidade (navegação privativa)**
   Abrir **janela privativa**, visitar um e-commerce, verificar proteções contra rastreamento.
   **Sucesso:** bloqueios reportados; sem histórico persistente; login e checkout funcionam.

> **Condições de teste padrão:** sessão contínua, rede estável doméstica, sem extensões não essenciais ativadas (apenas as necessárias ao fluxo).



### **Requisitantes e Partes Interessadas**

Embora este trabalho acadêmico não tenha um requisitante direto, no contexto real do desenvolvimento do Mozilla Firefox os principais requisitantes são a própria Mozilla Foundation/Mozilla Corporation, a comunidade de desenvolvedores voluntários, usuários avançados que sugerem melhorias e empresas/parceiros de tecnologia que integram seus serviços ao navegador.
As principais partes interessadas abrangem os usuários finais que utilizam o Firefox diariamente, os desenvolvedores web que dependem de compatibilidade com padrões abertos, a comunidade open source que participa de sua evolução, além da sociedade civil e organizações de defesa digital, que se beneficiam da proteção de privacidade e do acesso aberto à informação promovidos pelo navegador.

#### **Stakeholders → critérios de sucesso → impacto na avaliação**

| Stakeholder           | Necessidades/Interesses           | Critérios de sucesso (como medimos)                                       | Impacto na seleção/escopo                                    |
| --------------------- | --------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Usuário final         | Navegação estável e contínua      | **MTBF** alto; **MTTR** baixo; baixa taxa de crash/sessão                 | Ênfase em **Confiabilidade** sob múltiplas abas e mídia      |
| Desenvolvedor web     | Compatibilidade com padrões       | **ICPW/Compatibilidade** no fluxo (renderização correta; APIs suportadas) | Ênfase em **Funcionalidade** e conformidade                  |
| Comunidade Mozilla    | Transparência e melhoria contínua | Evidências **auditáveis** e rastreáveis                                   | Exigir **GitPage + dados** e rastreabilidade doc→métrica     |
| Equipe de produto     | Previsibilidade de release        | Critérios **go/no-go** objetivos por objetivo GQM                         | Definir limiares e **regras de consolidação**                |
| Segurança/Privacidade | Proteções consistentes            | Funcionalidades de privacidade operantes                                  | Testes de **navegação privativa** e bloqueio de rastreadores |

> Essas expectativas **orientam** a priorização, o **escopo** e a **seleção de métricas** na Fase 2 (GQM).

---


## **Glossário**

* **Fluxo cotidiano**: sequência de ações comuns de um usuário típico (buscar, ler notícias, assistir vídeo, usar um app on-line e navegar no modo privativo) por 30–60 minutos, com 6–12 abas abertas.
* **MTBF (Mean Time Between Failures)**: tempo médio entre falhas. Quanto **maior**, **mais estável**.
* **MTTR (Mean Time To Recovery)**: tempo médio para o navegador **se recuperar** e **restaurar a sessão** após uma falha/queda. Quanto **menor**, melhor.
* **CFE (Cobertura de Funcionalidades Essenciais)**: porcentagem de recursos “básicos” do navegador que **funcionam de fato** no fluxo (abas, downloads, mídia, formulários, extensões, privacidade).
* **ICPW (Índice de Conformidade com Padrões Web)**: quão bem o navegador segue os **padrões da web** (HTML, CSS, APIs).
* **BCD (Browser-Compat-Data, do MDN)**: base pública que mostra **se uma API/tecnologia é suportada** pelos navegadores.
* **WPT (Web Platform Tests)**: suíte pública de testes de **interoperabilidade** entre navegadores; usamos o **% de testes passantes** relevantes ao fluxo.
* **TSOF (Taxa de Sucesso de Operações Funcionais)**: proporção de **ações críticas** do usuário que funcionam (abrir página, reproduzir vídeo, enviar formulário, baixar arquivo, etc.).
* **WebExtensions**: modelo de **extensões** do Firefox (e outros browsers) para adicionar funções ao navegador.
* **Engine/JS/Layout**: o “motor” que **carrega páginas**, **executa JavaScript** e **desenha** a página na tela.
* **Restauração de sessão**: ao reabrir o navegador após fechar/crash, **recuperar abas e janelas** do usuário.
* **Go/No-Go**: decisão de **liberar** (go) ou **segurar** (no-go) uma versão ou mudança.
* **Issue**: registro formal de um problema/tarefa no sistema de acompanhamento (ex.: GitHub, Bugzilla).
* **Trade-off**: **troca** necessária quando priorizamos algo (ex.: confiabilidade) e **adiamos** outra coisa (ex.: desempenho).
* **COTS (Commercial Off-The-Shelf)**: software “de prateleira”, pronto para uso geral, sem personalização para um cliente específico.
* **Compatibilidade (coexistência – ISO 25010)**: capacidade de um software **funcionar bem ao lado** de outros em um mesmo ambiente (não é o mesmo que “compatível com padrões web”).



## Uso de IA no Desenvolvimento do Trabalho

Este trabalho utilizou **ferramentas de IA generativas**  para **apoiar pesquisas** (sugestão de fontes públicas e organização de tópicos), **formatação do texto** (padronização de seções, tabelas e títulos) e **correção gramatical/ortográfica**. As saídas de IA foram **revisadas pela equipe**.



## **Equipe e Contribuições**

| Matrícula | Nome completo                                        | Contribuição (%) |
| --------- | ---------------------------------------------------- | ---------------- |
| 211061565 | [Daniel Ferreira Nunes ](https://github.com/Mach1r0) | 20               |
| 221008632 | [Eduardo Ferreira](https://github.com/eduardoferre)  | 20               |
| 231011275 | [Eduardo Morais](https://github.com/Edumorais08)     | 20               |
| 221029249 | [Júlia Takaki](https://github.com/juliatakaki)       | 20               |
| 222037737 | [Matheus Brant](https://github.com/MatheussBrant)    | 20               |

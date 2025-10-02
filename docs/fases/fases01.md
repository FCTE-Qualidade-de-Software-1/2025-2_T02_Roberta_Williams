# **Fase 1: Estabelecer os Requisitos da Avaliação**

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
- O Firefox protege a privacidade dos usuários, garantindo liberdade digital e maior segurança no uso da internet
- Promove o acesso aberto à informação ao combater práticas abusivas de rastreamento e monopólio de dados
- Fortalece os direitos digitais e liberdades fundamentais, alinhando-se à meta 16.10 da ONU (assegurar acesso público à informação e proteger direitos básicos)

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



![alt text](image.png)

### **Matriz de Priorização**

| Característica           | Nível de Ênfase | 
|--------------------------|-----------------|
| Adequação Funcional      | 5 |
| Confiabilidade           | 5 | 
| Manutenibilidade         | 1 | 
| Portabilidade            | 1  |
| Eficiência de Desempenho | 1  | 
| Compatibilidade          | 1 |
| Segurança                | 1 | 
| Usabilidade              | 0 |

### **Classificação do Tipo de Produto**

O Mozilla Firefox pode ser classificado, segundo as categorias apresentadas por Pressman, como um software de computador pessoal, pois é utilizado diretamente pelo usuário final para navegação na web, acesso a informações, execução de aplicações online e interação com diferentes serviços digitais.

De acordo com a classificação da IEEE 1062, o Firefox enquadra-se como um COTS (Commercial Off-The-Shelf Software), uma vez que é um produto pronto, desenvolvido pelo fabricante e disponibilizado a um público amplo, sem customizações específicas para clientes individuais. Embora seja gratuito e de código aberto, mantém as características de um produto de prateleira, projetado para atender de forma generalista às necessidades da maioria dos usuários.

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

---

### **Fluxo de Navegação Cotidiana a ser Analisado**

Para garantir que a avaliação seja representativa do uso real, será analisado o seguinte fluxo de navegação:

1. **Início da Sessão e Pesquisa**: Abrir o navegador e realizar uma pesquisa sobre um tema de interesse.  
2. **Consumo de Conteúdo Misto**: Navegar entre diferentes abas, incluindo um portal de notícias, uma plataforma de vídeo e uma rede social.  
3. **Interação com Ferramentas de Produtividade**: Acessar e utilizar uma ferramenta online, como um editor de documentos em nuvem ou um serviço de e-mail.  
4. **Uso de Recursos de Privacidade**: Ativar o modo de navegação privativa e verificar as proteções contra rastreamento em um site de e-commerce.  

#### **Justificativa da Escolha do Fluxo**
Este fluxo foi escolhido por simular um cenário de uso realista e multifacetado, que testa simultaneamente a **Funcionalidade** (renderização de diferentes tipos de mídia, compatibilidade com aplicações web) e a **Confiabilidade** (gerenciamento de múltiplas abas, estabilidade durante a reprodução de vídeo). Ele permite observar como o navegador se comporta sob uma carga de trabalho típica, fornecendo dados valiosos sobre sua robustez e adequação funcional no dia a dia.


### **Requisitantes e Partes Interessadas**

Embora este trabalho acadêmico não tenha um requisitante direto, no contexto real do desenvolvimento do Mozilla Firefox os principais requisitantes são a própria Mozilla Foundation/Mozilla Corporation, a comunidade de desenvolvedores voluntários, usuários avançados que sugerem melhorias e empresas/parceiros de tecnologia que integram seus serviços ao navegador.
As principais partes interessadas abrangem os usuários finais que utilizam o Firefox diariamente, os desenvolvedores web que dependem de compatibilidade com padrões abertos, a comunidade open source que participa de sua evolução, além da sociedade civil e organizações de defesa digital, que se beneficiam da proteção de privacidade e do acesso aberto à informação promovidos pelo navegador.

| Matrícula | Nome completo | Contribuição (%) |
|-----------|----------------|-------------------|
| 211061565 | [Daniel Ferreira Nunes ](https://github.com/Mach1r0) | 20 |
| 221008632 | [Eduardo Ferreira](https://github.com/eduardoferre) | 20 |
| 231011275 | [Eduardo Morais](https://github.com/Edumorais08) | 20 |
| 221029249 | [Júlia Takaki](https://github.com/juliatakaki) | 20 |
| 222037737 | [Matheus Brant](https://github.com/MatheussBrant) | 20 |

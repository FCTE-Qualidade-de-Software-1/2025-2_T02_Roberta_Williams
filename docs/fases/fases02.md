# MODELO GQM 

Nesta segunda fase do projeto será utilizado o modelo GQM (Goal Question Metric) para definir metas, perguntas e métricas relacionadas ao projeto de desenvolvimento do software. O modelo GQM é uma abordagem estruturada que ajuda a garantir que as métricas coletadas sejam relevantes e alinhadas com os objetivos do projeto. ele é composto por três níveis principais:

1. **Goal (Meta)**: Define o que se deseja alcançar com o projeto. As metas devem ser específicas, mensuráveis, alcançáveis, relevantes e temporais (SMART).
2. **Question (Pergunta)**: Formula perguntas que ajudam a entender se as metas estão sendo alcançadas. Essas perguntas devem ser claras e focadas nos aspectos críticos do projeto.
3. **Metric (Métrica)**: Identifica as métricas que serão usadas para responder

# **Medição 1 - Confiabilidade**

## Goal (Meta)

Analisar a robustez e estabilidade do Mozilla Firefox, bem como sua capacidade de manter desempenho consistente e se recuperar de falhas sob condições variadas de uso, a fim de identificar pontos fortes e áreas de melhoria relacionadas à sua confiabilidade.

## Question (Pergunta)

### Perguntas

- **Q2.1:** O navegador mantém desempenho estável e consistente sob condições variadas de uso, como múltiplas abas abertas, carregamento de conteúdo multimídia pesado ou falhas ocasionais de rede?
- **Q2.2:** Qual a frequência de falhas, travamentos ou lentidão durante o uso contínuo e intensivo do navegador?
- **Q2.3:** O navegador se recupera adequadamente de erros e falhas, minimizando a perda de dados ou interrupção da experiência do usuário?
- **Q2.4:** A reprodução de vídeos e áudios em plataformas de streaming ocorre sem interrupções ou problemas de sincronização?
- **Q2.5:** O navegador restaura a sessão anterior após um travamento inesperado?

## Metric (Métricas)

| Código    | Métrica                                         | Descrição                                                                                                         | Meta                      |
|-----------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------|
| **M2.1.1** | Taxa de Falhas/Travamentos                     | Número de travamentos ou falhas inesperadas por hora de uso ou por sessão de navegação.                           | < 0,1 falha/hora          |
| **M2.1.2** | Tempo Médio Entre Falhas (MTBF)                 | Tempo médio de operação contínua do navegador antes da ocorrência de uma falha.                                   | > 24 horas                |
| **M2.1.3** | Tempo de Resposta da Interface                  | Tempo médio para a interface responder a interações (ex: clique em links, abertura de abas) sob diferentes cargas.| < 500 ms (interações básicas) |
| **M2.1.4** | Taxa de Sucesso na Reprodução Multimídia        | Percentual de vídeos e áudios reproduzidos sem interrupções ou problemas de sincronização em plataformas de streaming.| > 98%                     |
| **M2.1.5** | Taxa de Recuperação de Sessão                   | Percentual de vezes que o navegador restaura a sessão anterior após um travamento inesperado.                     | > 95%                     |

# **Medição 2 – Adequação Funcional**

## Goal (Meta)

Avaliar se o Mozilla Firefox oferece funções completas, corretas e apropriadas às necessidades dos usuários, garantindo que suas principais operações como navegação, renderização de páginas, uso de abas, downloads, personalização e sincronização funcionem adequadamente e atendam aos objetivos de usabilidade e abertura da web.

---

## Question (Perguntaa)
### Perguntas:

- **Q2.5:** As funções principais do Firefox (abrir abas, carregar páginas, salvar favoritos, histórico, downloads, sincronização) funcionam corretamente?  
- **Q2.6:** O navegador exibe corretamente páginas baseadas em diferentes padrões web (HTML5, CSS3, JavaScript, etc.)?  
- **Q2.7:** As extensões e temas funcionam corretamente e sem conflitos com o navegador?  
- **Q2.8:** O Firefox permite personalizar a interface e as preferências de forma eficaz e funcional?  
- **Q2.9:** As funções integradas (modo leitura, busca na barra de endereços, sugestões) apresentam comportamento adequado e esperado pelo usuário?

---

## Metric (Métricas)

| **Código** | **Métrica** | **Descrição** | **Meta** |
|-------------|-------------|----------------|-----------|
| **M2.2.1** | Taxa de Sucesso das Funções Principais | Percentual de funções testadas que executam corretamente sem erros (abrir abas, histórico, downloads, favoritos). | ≥ 95% |
| **M2.2.2** | Conformidade com Padrões Web | Pontuação em testes de suporte a padrões abertos (HTML5Test, ACID3, etc.). | ≥ 90% |
| **M2.2.3** | Taxa de Compatibilidade de Extensões | Percentual de extensões testadas que funcionam sem falhas (ex: tradutor, bloqueador de anúncios, leitor de PDF). | ≥ 90% |
| **M2.2.4** | Taxa de Personalização Aplicada com Sucesso | Percentual de alterações de tema, idioma ou layout aplicadas corretamente. | ≥ 95% |
| **M2.2.5** | Taxa de Sucesso de Sincronização de Dados | Percentual de sincronizações bem-sucedidas entre dispositivos (favoritos, histórico, senhas). | ≥ 95% |
| **M2.2.6** | Taxa de Renderização Correta | Percentual de páginas renderizadas corretamente (sem erros de exibição ou elementos quebrados). | ≥ 98% |

---

### **Histórico de Versão**

| Versão | Data       | Descrição                                         | Autor          | Revisor          |
| :----- | :--------- | :------------------------------------------------ | :------------- | :--------------- |
| 1.0    | 12/10/2025 | Criação inicial do documento                      | [Daniel Ferreira](https://github.com/Mach1r0)   | [Eduardo Ferreira](https://github.com/eduardoferre) |
| 1.1    | 13/10/2025 | Adição das métricas da Adequação Funcional        | [Eduardo Morais](https://github.com/Edumorais08)| [Daniel Ferreira](https://github.com/Mach1r0) |
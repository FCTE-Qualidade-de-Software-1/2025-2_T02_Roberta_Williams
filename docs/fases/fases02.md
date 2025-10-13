# MODELO GQM 

Nesta segunda fase do projeto será utilizado o modelo GQM (Goal Question Metric) para definir metas, perguntas e métricas relacionadas ao projeto de desenvolvimento do software. O modelo GQM é uma abordagem estruturada que ajuda a garantir que as métricas coletadas sejam relevantes e alinhadas com os objetivos do projeto. ele é composto por três níveis principais:

1. **Goal (Meta)**: Define o que se deseja alcançar com o projeto. As metas devem ser específicas, mensuráveis, alcançáveis, relevantes e temporais (SMART).
2. **Question (Pergunta)**: Formula perguntas que ajudam a entender se as metas estão sendo alcançadas. Essas perguntas devem ser claras e focadas nos aspectos críticos do projeto.
3. **Metric (Métrica)**: Identifica as métricas que serão usadas para responder

# Medição 1 - Confiabilidade

## Goal (Meta)

Analisar a robustez e estabilidade do Mozilla Firefox, bem como sua capacidade de manter desempenho consistente e se recuperar de falhas sob condições variadas de uso, a fim de identificar pontos fortes e áreas de melhoria relacionadas à sua confiabilidade.

## Question (Pergunta)

### Perguntas

- **Q2.1:** O navegador mantém desempenho estável e consistente sob condições variadas de uso, como múltiplas abas abertas, carregamento de conteúdo multimídia pesado ou falhas ocasionais de rede?
- **Q2.2:** Qual a frequência de falhas, travamentos ou lentidão durante o uso contínuo e intensivo do navegador?
- **Q2.3:** O navegador se recupera adequadamente de erros e falhas, minimizando a perda de dados ou interrupção da experiência do usuário?
- **Q2.4:** A reprodução de vídeos e áudios em plataformas de streaming ocorre sem interrupções ou problemas de sincronização?


### Métricas

| Código    | Métrica                                         | Descrição                                                                                                         | Meta                      |
|-----------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------|
| **M2.1.1** | Taxa de Falhas/Travamentos                     | Número de travamentos ou falhas inesperadas por hora de uso ou por sessão de navegação.                           | < 0,1 falha/hora          |
| **M2.1.2** | Tempo Médio Entre Falhas (MTBF)                 | Tempo médio de operação contínua do navegador antes da ocorrência de uma falha.                                   | > 24 horas                |
| **M2.1.3** | Tempo de Resposta da Interface                  | Tempo médio para a interface responder a interações (ex: clique em links, abertura de abas) sob diferentes cargas.| < 500 ms (interações básicas) |
| **M2.1.4** | Taxa de Sucesso na Reprodução Multimídia        | Percentual de vídeos e áudios reproduzidos sem interrupções ou problemas de sincronização em plataformas de streaming.| > 98%                     |
| **M2.1.5** | Taxa de Recuperação de Sessão                   | Percentual de vezes que o navegador restaura a sessão anterior após um travamento inesperado.                     | > 95%                     |

### **Histórico de Versão**

| Versão | Data       | Descrição                                         | Autor          | Revisor          |
| :----- | :--------- | :------------------------------------------------ | :------------- | :--------------- |
| 1.0    | 12/10/2025 | Criação inicial do documento | [Daniel Ferreira](https://github.com/Mach1r0) | [Eduardo Ferreira](https://github.com/eduardoferre) |

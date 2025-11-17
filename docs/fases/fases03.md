# 🏛️ Fase 03: Projetar a Avaliação

## 1. Objetivo deste Plano


O objetivo deste documento é "produzir o plano de avaliação"[cite: 41, 276]. Ele serve como a ponte entre a **Fase 02** (onde *especificamos* as métricas) e a **Fase 04** (onde *executamos* a coleta)[cite: 18].


Este plano detalha o **método de avaliação**, os **recursos necessários** e o **cronograma de ações** [cite: 279, 280], com instruções claras para que um avaliador possa executar a avaliação de forma completa e reprodutível[cite: 281].

* **Produto Alvo:** Mozilla Firefox (desktop) Versão 143.0.3.
* **Persona Alvo:** "Estudante/Profissional multitarefa conectada".

## 2. Recursos Necessários


Conforme especificado pelo processo de avaliação[cite: 279], os seguintes recursos são necessários:

### Recursos de Hardware
* **Dispositivo:** Notebook ou desktop (Ex: Intel i5 ou equivalente, 8GB de RAM).
* **Rede:** Conexão Wi-Fi doméstica/banda larga padrão.

### Recursos de Software
* **Sistema Operacional:** Windows 11 ou macOS.
* **Produto:** Navegador Mozilla Firefox, versão 143.0.3 (instalação limpa).
* **Ferramentas de Coleta:**
    * Planilha de coleta (Google Sheets) para a "Ficha de Registro".
    * Software de gravação de tela (Ex: OBS Studio, QuickTime) para capturar as evidências em vídeo.
    * Cronômetro (físico ou de software).
* **Extensões de Teste (conforme M2.3):**
    1.  Bloqueador de anúncios (Ex: uBlock Origin)
    2.  Tradutor (Ex: Google Tradutor)
    3.  Gerenciador de Senhas (Ex: Bitwarden)
    4.  Leitor de PDF (Ex: Leitor de PDF nativo ou extensão)
    5.  Utilitário (Ex: Dark Reader)

### Recursos Humanos
* **Avaliador:** 1 membro da equipe por sessão, com conhecimento do fluxo de navegação e das métricas a serem coletadas.

## 3. Método de Avaliação e Coleta de Dados


Este é o **método de avaliação** [cite: 279] que detalha o fluxo de testes e as instruções exatas para a coleta de dados de cada métrica definida na Fase 02.

### 3.1. Preparação da Sessão de Teste (Setup)

Para garantir a consistência, cada sessão de avaliação deve começar com os seguintes passos:

1.  **Instalação Limpa:** Iniciar com o Firefox 143.0.3.
2.  **Limpeza de Dados:** Limpar todo o cache, cookies e histórico de navegação.
3.  **Extensões:** Desativar todas as extensões, exceto as 5 listadas para o teste da M2.3 (que só devem ser ativadas no Passo 3 do fluxo).
4.  **Início da Coleta:**
    * Abrir a "Ficha de Registro" (Google Sheet).
    * **Iniciar a gravação de tela** (evidência principal).
    * Iniciar o cronômetro principal da sessão (para M1.2 e M1.3).

### 3.2. Fluxo de Execução e Instruções de Coleta

O avaliador deve seguir o "Fluxo de Navegação Cotidiana" e coletar os dados das métricas nos momentos especificados abaixo:

#### Passo 1: Início & Pesquisa (Duração: 5-10 min)

* **Ação:** Abrir o Firefox. Realizar 3 buscas no Google. Abrir 6 abas de notícias/blogs a partir dos resultados.
* **Coleta (M2.1 - CFE):**
    * Na Ficha de Registro, marcar "Sucesso" ou "Falha" para as tarefas:
        1.  Abrir nova aba.
        2.  Fechar aba.
        3.  Alternar entre abas.
        4.  Adicionar uma página aos favoritos.
        5.  Verificar se a busca aparece no histórico.

#### Passo 2: Conteúdo Misto (Duração: 30-40 min)

* **Ação:** Manter as 6-12 abas abertas. Uma aba deve conter um streaming de vídeo (YouTube) em 720p, contínuo. Alternar ativamente entre as abas (notícia, rede social, vídeo).
* **Coleta (M1.4 - Sucesso Multimídia):**
    * Observar a aba de vídeo 720p. Registrar o número de interrupções (engasgos, buffer, falhas de áudio).
* **Coleta (M1.1 - Resposta da UI):**
    * Realizar 10 testes de "troca de aba" (clicar em uma aba e medir o tempo até ela estar 100% visível/interativa).
    * Usar o cronômetro ou o painel "Performance" do DevTools. Registrar a média em (ms).
* **Coleta (M1.2 - Taxa de Falhas / M1.3 - MTBF):**
    * Manter o cronômetro da sessão (60 min) rodando.
    * Se ocorrer um *crash* (travamento ou fechamento inesperado):
        1.  Parar o cronômetro da sessão. Registrar o tempo como "MTBF" (M1.3).
        2.  Registrar '1' na contagem de falhas (M1.2).
        3.  Fazer print da tela de erro/log de crash.

#### Passo 3: Produtividade (App Web) (Duração: 10 min)

* **Ação:** Abrir um app web (ex: Google Docs). Editar um documento. Iniciar um download de 100MB. Ativar as 5 extensões de teste.
* **Coleta (M2.1 - CFE):**
    * Na Ficha de Registro, marcar "Sucesso" ou "Falha" para as tarefas:
        1.  Editar texto no Google Docs.
        2.  Download do arquivo de 100MB (concluiu? corrompeu?).
* **Coleta (M2.3 - Compatibilidade de Extensões):**
    * Tentar usar a função principal de cada uma das 5 extensões (Ex: traduzir a página, bloquear um anúncio).
    * Registrar o número de extensões que funcionaram corretamente.

#### Passo 4: Privacidade (Navegação Privativa) (Duração: 10 min)

* **Ação:** Abrir uma nova janela privativa. Visitar 3 sites de e-commerce. Simular login e checkout.
* **Coleta (M2.4 - TSOF Modo Privativo):**
    * Na Ficha de Registro, marcar "Sucesso" ou "Falha" para as tarefas (login, checkout simulado).
    * Clicar no ícone de escudo na barra de endereço e fazer um print do relatório de bloqueios.

#### Passo 5: Teste de Anomalias (Duração: 5 min)

* **Ação:** Com o navegador ainda em uso, executar os 5 cenários de anomalia.
* **Coleta (M1.5 - TRA):**
    1.  **Queda de Rede:** Desconectar o Wi-Fi por 15 segundos e reconectar.
    2.  **Pico de CPU:** Rodar um script/software que use 100% da CPU por 20 segundos.
    3.  **Baixa RAM:** Abrir outros apps pesados até o sistema alertar sobre memória.
    4.  **Erro 500:** Acessar uma página de teste de erro 500.
    5.  **Timeout:** Acessar um site que simule timeout.
    * Para cada cenário, registrar "Sucesso" (navegador se recuperou) ou "Falha" (travou/crashou).

#### Passo 6: Análise de Conformidade (Pós-Sessão)

* **Coleta (M2.2 - ICPW):**
    * Esta métrica é coletada fora do fluxo de usuário.
    * Acessar o **MDN Browser-Compat-Data (BCD)**.
    * Listar 10 APIs/recursos web essenciais usados no fluxo (Ex: "HTML5 Video", "Fetch API", "CSS Flexbox").
    * Verificar o status de compatibilidade ("support") para o Firefox 143.
    * Calcular a porcentagem de conformidade.

### 3.3. Armazenamento e Estrutura dos Dados

* **Ficha de Registro (Google Sheet):** Todos os dados quantitativos (ms, %, h, contagens) serão registrados em uma planilha centralizada. A estrutura da ficha já está definida na Fase 02.
* **Evidências (Vídeo e Prints):** Toda sessão de teste (Passos 1-5) deve ser **gravada em vídeo**. Prints de tela são obrigatórios para comprovar falhas, resultados de M2.4 (Privacidade) e M2.2 (ICPW).
* **Nomenclatura:** Os arquivos de evidência devem ser nomeados com o ID da sessão (Ex: `Sessao_01_Video.mp4`, `Sessao_01_M2.4_Print.png`).

## 4. Cronograma das Ações


O cronograma a seguir detalha a execução das Fases 03 e 04[cite: 280]:

| Data (Exemplo) | Fase | Atividade | Responsáveis | Entregável |
| :--- | :--- | :--- | :--- | :--- |
| 16/11/25 | Fase 03 | Finalização e revisão deste Plano de Avaliação. | Equipe | `fases03.md` (Este documento) |
| 17/11/25 | Fase 04 | Execução da Sessão de Teste 01 (Coleta M1.1-M2.4) | Membro 1 | Ficha de Registro (Linha 1), Vídeo 1 |
| 18/11/25 | Fase 04 | Execução da Sessão de Teste 02 (Coleta M1.1-M2.4) | Membro 2 | Ficha de Registro (Linha 2), Vídeo 2 |
| 19/11/25 | Fase 04 | Execução da Sessão de Teste 03 (Coleta M1.1-M2.4) | Membro 3 | Ficha de Registro (Linha 3), Vídeo 3 |
| 20/11/25 | Fase 04 | Execução das Sessões 04 e 05 (Coleta M1.1-M2.4) | Membros 4, 5 | Ficha de Registro (Linhas 4, 5), Vídeos 4, 5 |
| 21/11/25 | Fase 04 | Coleta da M2.2 (ICPW) e consolidação dos dados. | Equipe | Planilha final com médias calculadas. |
| 22/11/25 | Fase 04 | Análise, Comparação e Julgamento dos resultados. | Equipe | Tabelas de Julgamento (O1, O2) preenchidas. |
| 23/11/25 | Fase 04 | Produção do Relatório Final e vídeo de apresentação. | Equipe | `fases04.md` e Vídeo Final. |



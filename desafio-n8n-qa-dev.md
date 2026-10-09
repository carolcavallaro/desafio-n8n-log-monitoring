# 🎯 Desafio Criativo: Planejando Automações com N8N

## 🧱 Passo 1: Definição da Automação

Quero criar uma automação no N8N para capturar, tratar e notificar automaticamente erros e exceções disparados por uma aplicação Web.

* **Público ou responsável:**  
  Equipes de Desenvolvimento (Full-Stack), Garantia da Qualidade (QA) e Sustentação.

* **Resultado esperado:**  
  Filtrar os logs recebidos por severidade, salvar os detalhes da falha em uma base de dados para auditoria de QA e enviar um alerta em tempo real com a *stack trace* no Discord/Slack para rápida atuação do time de dev.

---

## 🧱 Passo 2: Contexto e Regras

* **Ferramentas envolvidas:**  
  Webhook (N8N), PostgreSQL (ou Google Sheets) e Discord (ou Slack).

* **Fluxo desejado:**  
  1. Receber o *payload* JSON com o log de erro vindo da aplicação via Webhook.  
  2. Filtrar o evento com base no nível de severidade (mantendo apenas erros do tipo `CRITICAL` ou `FATAL`).  
  3. Salvar os detalhes do incidente (*Timestamp*, *Endpoint*, *Status Code*, Mensagem de Erro e *Stack Trace*) na base de dados para controle de QA.  
  4. Formatar uma mensagem visualmente clara e enviá-la para o canal de alertas dos desenvolvedores.

* **Regras importantes:**  
  * Ignorar erros de baixa severidade (como `INFO` ou `WARNING`).  
  * Se o *payload* recebido não mantiver a estrutura válida de JSON ou faltar o campo de erro principal, registrar no banco como "Erro Malformado" para investigação do time de QA.

---

## 🤖 Passo 3: Prompt Final para IA

Atue como um especialista em N8N e arquitetura de software.

Crie uma automação para monitoramento, triagem e notificação em tempo real de erros de aplicação Web (Incident Management para QA/Dev).

Público:
Equipes de Desenvolvimento Full-Stack e Engenharia de QA.

Ferramentas envolvidas:
Webhook (N8N), PostgreSQL (ou Google Sheets) e Discord (ou Slack).

Fluxo:
1. Receber o log de erro em formato JSON via Webhook HTTP.
2. Validar e filtrar os dados, mantendo apenas falhas de severidade CRITICAL ou FATAL.
3. Persistir os detalhes do bug (Timestamp, Endpoint, Status Code e Stack Trace) em um banco relacional para métricas de QA.
4. Enviar uma notificação formatada em rich-text/embed para o canal de suporte no Discord/Slack.

Regras:
- Descartar logs informativos ou avisos simples (INFO/WARNING).
- Garantir o tratamento de payloads malformados ou incompletos.

Explique quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow.

---

## 🛠️ Nós do N8N Recomendados
* **Webhook Node:** Ponto de entrada HTTP REST para capturar requisições JSON da aplicação.
* **Filter / If Node:** Para filtrar a severidade (`CRITICAL`/`FATAL`) e validar a estrutura do JSON.
* **PostgreSQL / Google Sheets Node:** Para persistir o histórico de bugs e métricas de QA.
* **Discord / Slack Node:** Para disparar o alerta imediato ao time.

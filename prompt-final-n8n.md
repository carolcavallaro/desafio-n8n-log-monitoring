# 🤖 Prompt Final: Automação de Monitoramento no N8N

## Prompt Estruturado

Atue como um especialista em N8N e arquitetura de software.

Crie uma automação para monitoramento, triagem e notificação em tempo real de erros de aplicação Web (Incident Management para QA/Dev).

**Público:**
Equipes de Desenvolvimento Full-Stack e Engenharia de QA.

**Ferramentas envolvidas:**
Webhook (N8N), PostgreSQL (ou Google Sheets) e Discord (ou Slack).

**Fluxo:**
1. Receber o log de erro em formato JSON via Webhook HTTP.
2. Validar e filtrar os dados, mantendo apenas falhas de severidade CRITICAL ou FATAL.
3. Persistir os detalhes do bug (Timestamp, Endpoint, Status Code e Stack Trace) em um banco relacional para métricas de QA.
4. Enviar uma notificação formatada em rich-text/embed para o canal de suporte no Discord/Slack.

**Regras:**
- Descartar logs informativos ou avisos simples (INFO/WARNING).
- Garantir o tratamento de payloads malformados ou incompletos.

---

## 🛠️ Nós do N8N Recomendados

* **Webhook Node:** Ponto de entrada HTTP REST para capturar requisições JSON da aplicação.
* **Filter / If Node:** Para filtrar a severidade (`CRITICAL`/`FATAL`) e validar a estrutura do JSON.
* **PostgreSQL / Google Sheets Node:** Para persistir o histórico de bugs e métricas de QA.
* **Discord / Slack Node:** Para disparar o alerta imediato ao time.

# 🛠️ N8N Incident Management & Log Monitoring Automation

> **Projeto de Automação e QA/Full-Stack**  
> **Status:** Concluído 🎯  
> **Área:** Engenharia de Software / Testes de Software (QA) / Automação de Processos  

---

## 📌 Sobre o Repositório
Este repositório contém o planejamento e a arquitetura de uma automação construída no **N8N** para monitoramento, triagem e notificação em tempo real de erros e exceções de aplicações Web. 

O projeto foi desenvolvido como parte de um desafio prático de automação, conectando conceitos de **desenvolvimento Full-Stack** (consumo de webhooks, tratamento de dados JSON, persistência em banco) com **Garantia da Qualidade / QA** (gerenciamento de incidentes, triagem de bugs e facilitação da análise de causa raiz).

---

## 🎯 Objetivos do Sistema
- **Centralizar a recepção de logs:** Capturar exceções de runtime via requisições HTTP REST.
- **Filtragem Inteligente:** Processar apenas falhas de alta severidade (`CRITICAL` ou `FATAL`), reduzindo o ruído (*alert fatigue*) na comunicação da equipe.
- **Registro para Métricas de QA:** Armazenar dados estruturados (Timestamp, Status Code, Stack Trace, Endpoint) para acompanhamento da saúde da aplicação.
- **Alertas Imediatos:** Notificar os times de desenvolvimento e sustentação em tempo real no Discord/Slack.

---

## 🏗️ Estrutura do Repositório
- `README.md`: Apresentação geral do projeto no portfólio.
- `desafio-n8n-qa-dev.md`: Documentação técnica do planejamento e prompt estruturado gerado para o Desafio DIO.

---

## 👩‍💻 Autora

Desenvolvido por **Carolina Cavallaro** 🎯

Estudante de **Análise e Desenvolvimento de Sistemas (ADS)** em transição para a área de TI. Unindo mais de 15 anos de bagagem corporativa e visão analítica ao aprendizado contínuo em **QA/Testes**, **Desenvolvimento Full-Stack** e automação com **N8N**.

- 🛠️ **Foco Atual:** QA / Software Testing & Full-Stack Development
- 📬 **Contato:** [LinkedIn](https://linkedin.com/in/seu-perfil)

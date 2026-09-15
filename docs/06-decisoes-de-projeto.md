# Documento 06 • Organização do Trabalho, Metodologia e Registro de Decisões

## 1. Metodologia de Trabalho da Equipe

O grupo estruturou suas atividades utilizando princípios ágeis baseados no framework **Scrum/Kanban**:
* **Comunicação Contínua:** Reuniões rápidas diárias de alinhamento (*Daily Standup*) de 10 minutos para tirar dúvidas entre áreas.
* **Sprints Temáticas:** Divisão em ciclos focados em Diagnóstico, Definição de Requisitos, Prototipação UX, Arquitetura Técnica e Documentação.
* **Ambiente Centralizado:** Uso do GitHub como repositório único de documentação técnica, controle de versões e registro das decisões de projeto.

---

## 2. Ferramentas Utilizadas pelo Grupo

| Ferramenta | Finalidade no Projeto |
|---|---|
| **GitHub** | Repositório de documentação, versionamento e publicação dos arquivos markdown. |
| **Figma** | Criação de wireframes, protótipo de alta fidelidade e validação de acessibilidade visual. |
| **DBDiagram / Draw.io** | Modelagem conceitual do banco de dados relacional e diagramas de fluxo operacional. |
| **Trello / Notion** | Quadro Kanban para controle de tarefas em andamento, impedimentos e revisões. |

---

## 3. Registro de Decisões Técnicas de Projeto (ADR - Architecture Decision Records)

### Decisão 01: Plataforma Web em Nuvem vs. Aplicativo Nativo
* **Contexto:** Havia a dúvida se deveríamos criar um app nativo para Android/iOS ou uma plataforma web responsiva.
* **Decisão:** Plataforma Web Responsiva.
* **Justificativa:** Menor barreira de entrada para pacientes de baixa renda (não exige espaço de memória do celular) e compatibilidade imediata com os computadores antigos das clínicas.

### Decisão 02: Modelo de Banco de Dados Relacional (SQL)
* **Contexto:** Avaliação entre banco NoSQL (documentos) ou SQL relacional (PostgreSQL).
* **Decisão:** Banco Relacional com suporte a transações estritas (ACID).
* **Justificativa:** A principal dor da clínica é a concorrência de agendamentos (*overbooking*). Bancos relacionais oferecem travas (*locks*) de consistência atômica superiores para impedir reservas simultâneas do mesmo horário.

### Decisão 03: Separação Estrita de Perfis de Acesso (RBAC)
* **Contexto:** Discutiu-se se recepcionistas poderiam visualizar notas de atendimento para ajudar a orientar o paciente no balcão.
* **Decisão:** Bloqueio total do prontuário para a recepção.
* **Justificativa:** Conformidade estrita com o Artigo 11 da LGPD (dados sensíveis de saúde). Somente profissionais de saúde habilitados podem acessar diagnósticos clínicos.

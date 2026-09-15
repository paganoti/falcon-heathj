# Documento 04 • Papéis Profissionais da Equipe Técnica

Para desenvolver a solução da Falcon Health, 5 papéis técnicos essenciais e complementares foram definidos:

---

## 1. Product Owner (PO) / Analista de Requisitos
* **O que faz:** Atua como a ponte de comunicação entre a rotina real das clínicas populares e a equipe de desenvolvimento de software, assegurando que o produto resolva as dores reais da operação.
* **Principais responsabilidades:** Levantar processos com as unidades, construir o backlog de histórias de usuário, definir critérios de aceitação e gerenciar a priorização do MVP.
* **Conhecimentos e competências:** Metodologias ágeis (Scrum/Kanban), escuta ativa, mapeamento de fluxos operacionais, visão de negócio em saúde e gestão de valor.
* **Principais entregas:** Backlog do produto no repositório, matriz MoSCoW de priorização e diagramas de fluxo de agendamento.
* **Trabalho conjunto:** Alinha com o UX/UI Designer sobre as regras de negócio de cada tela e com o Engenheiro Back-end sobre a viabilidade técnica de cada entrega.
* **Impacto se a função fosse ignorada:** O grupo construiria ferramentas confusas ou desnecessárias, perderia o foco do MVP e não resolveria a dor central de concorrência das clínicas.

---

## 2. Designer de Experiência e Interface (UX/UI Designer)
* **O que faz:** Projeta a estrutura navegável, o design de interação e a identidade visual das telas com foco absoluto em facilidade de uso, simplicidade e inclusão digital.
* **Principais responsabilidades:** Realizar pesquisas com usuários, criar personas, estruturar wireframes de baixa fidelidade, prototipar telas em alta fidelidade e zelar pela acessibilidade.
* **Conhecimentos e competências:** Figma, Design System, testes de usabilidade com usuários leigos, arquitetura de informação e diretrizes de acessibilidade (WCAG 2.1).
* **Principais entregas:** Mapa de personas da clínica, wireframes das jornadas, guia de estilos (*Design System*) e protótipo interativo navegável.
* **Trabalho conjunto:** Constrói as jornadas a partir dos critérios do Product Owner e entrega especificações visuais de componentes para o Front-end Engineer.
* **Impacto se a função fosse ignorada:** O sistema seria feio, hostil e difícil de manusear, causando abandono por parte dos pacientes e sobrecarga de erros manuais na recepção.

---

## 3. Engenheiro de Back-end e Banco de Dados (Software Engineer)
* **O que faz:** Modela as estruturas de persistência de dados em nuvem e escreve a lógica de negócios e APIs que impedem falhas de agendamento e sincronizam as filiais.
* **Principais responsabilidades:** Modelar o banco relacional, implementar rotas de API seguras, programar travas de concorrência para consultas e garantir integridade transacional.
* **Conhecimentos e competências:** Bancos de dados relacionais (PostgreSQL/MySQL), APIs RESTful, modelagem de dados, regras ACID e computação em nuvem.
* **Principais entregas:** Diagrama Entidade-Relacionamento (DER), coleção de rotas de API documentadas e implementação da lógica de agendamento em tempo real.
* **Trabalho conjunto:** Fornece as rotas de consumo para o Front-end Engineer e adota os requisitos de criptografia e auditoria ditados pelo Especialista de Segurança.
* **Impacto se a função fosse ignorada:** A interface seria apenas uma imagem sem vida; os agendamentos continuariam sofrendo duplicações e os dados ficariam corrompidos.

---

## 4. Engenheiro Front-end (Front-end Engineer)
* **O que faz:** Transforma as telas prototipadas em código de aplicação web leve, dinâmico e executável em navegadores desktop e móveis.
* **Principais responsabilidades:** Programar os componentes interativos, consumir os dados providos pelas APIs do back-end, validar dados digitados no navegador e otimizar velocidade de carregamento.
* **Conhecimentos e competências:** HTML5 semântico, CSS3 responsivo, JavaScript/TypeScript moderno, integração com APIs assíncronas e otimização de renderização.
* **Principais entregas:** Aplicação web responsiva codificada, validação em tempo real de formulários e integração total com as rotas de backend.
* **Trabalho conjunto:** Recebe os protótipos e especificações do UX/UI Designer e conecta as telas com os endpoints desenvolvidos pelo Back-end Engineer.
* **Impacto se a função fosse ignorada:** As ideias e designs ficariam restritos a arquivos estáticos do Figma, sem se tornarem uma ferramenta operável pelos funcionários e pacientes.

---

## 5. Analista de Segurança da Informação e LGPD (InfoSec & Compliance)
* **O que faz:** Protege a integridade, o sigilo e a disponibilidade de dados sensíveis de saúde dos pacientes, garantindo conformidade irrestrita com a Lei Geral de Proteção de Dados.
* **Principais responsabilidades:** Desenhar a arquitetura de permissões por perfil (RBAC), projetar registros de logs de auditoria e auditar a segurança no tráfego de prontuários médicos.
* **Conhecimentos e competências:** Lei Geral de Proteção de Dados (LGPD/ANPD), princípios de *Privacy by Design*, autenticação segura (JWT/OAuth), criptografia e análise de riscos cibernéticos.
* **Principais entregas:** Matriz RBAC de perfis de usuário, relatório de análise de riscos à privacidade de dados e política de segurança do sistema.
* **Trabalho conjunto:** Orienta a equipe de Back-end e Front-end no tratamento de dados e senhas e revisa termos de consentimento junto com o UX/UI.
* **Impacto se a função fosse ignorada:** Vazamento de diagnósticos médicos de pacientes, multas pesadas da ANPD, escândalos de reputação e perda da licença operacional da rede.

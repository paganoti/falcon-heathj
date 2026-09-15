# Documento 03 • Requisitos do Sistema e Escopo do MVP

Para balancear a urgência das clínicas com a viabilidade técnica da equipe de desenvolvimento, utilizamos a metodologia de priorização **MoSCoW**:
* **Must Have (Alta prioridade):** Essencial para o MVP (Produto Mínimo Viável) entrar em operação.
* **Should Have (Média prioridade):** Importante, programado logo após o MVP funcional.
* **Could Have (Baixa prioridade):** Melhorias desejáveis para fases posteriores de evolução.

---

## 1. Requisitos Funcionais (RF)

| Código | Requisito Funcional | Descrição Detalhada | Prioridade MoSCoW |
|---|---|---|---|
| **RF01** | Gestão de Agendamentos em Tempo Real | Capacidade de marcar, remarcar e cancelar consultas com validação de disponibilidade e trava de concorrência entre filiais. | **Alta (Must)** |
| **RF02** | Cadastro de Unidades, Salas e Médicos | Estrutura hierárquica que mapeia filiais, especialidades disponíveis, salas de atendimento e agendas semanais dos médicos. | **Alta (Must)** |
| **RF03** | Fila Dinâmica e Painel de Recepção | Funcionalidade para recepcionistas registrarem check-in do paciente, monitorando status: *Aguardando*, *Em Atendimento*, *Concluído* e *Ausente*. | **Alta (Must)** |
| **RF04** | Prontuário Básico Unificado | Módulo compartilhado para médicos consultarem diagnósticos passados, alergias e anotações clínicas inseridas em qualquer unidade da rede. | **Alta (Must)** |
| **RF05** | Controle de Perfis de Acesso (RBAC) | Restrição rigorosa de funcionalidades de acordo com a credencial autenticada (Paciente, Recepcionista, Médico, Administrador). | **Alta (Must)** |
| **RF06** | Confirmação e Lembretes Automáticos | Gatilho automático de disparo prévio via WhatsApp/SMS com confirmação ativa e liberação imediata de horário desmarcado. | **Média (Should)** |
| **RF07** | Portal do Paciente Simplificado | Interface mobile leve para pacientes consultarem histórico de atendimentos e consultas futuras sem senhas complexas. | **Média (Should)** |
| **RF08** | Painel Analítico da Gestão | Relatórios consolidados com taxas de faltas (*no-show*), ocupação média de salas e especialidades com maior fila de espera. | **Baixa (Could)** |

---

## 2. Requisitos Não Funcionais (RNF)

| Código | Requisito Não Funcional | Especificação e Critério de Aceitação | Prioridade MoSCoW |
|---|---|---|---|
| **RNF01** | Segurança e Conformidade com a LGPD | Criptografia ponta a ponta (TLS 1.3 em trânsito e AES-256 em repouso), com registro inalterável de logs de auditoria para leitura de dados de saúde. | **Alta (Must)** |
| **RNF02** | Integridade Transacional e Bloqueio de Concorrência | O banco de dados deve utilizar isolamento transacional estrito para garantir que nenhum slot de horário seja marcado duplamente em acessos simultâneos. | **Alta (Must)** |
| **RNF03** | Responsividade e Usabilidade Mobile | Adaptação automática e funcional para telas de computadores desktop de recepção e telas verticais de smartphones populares. | **Alta (Must)** |
| **RNF04** | Desempenho e Carga Leve | Carregamento total da tela de atendimento e agendamento em menos de 3 segundos em conexões 3G e 4G comerciais. | **Média (Should)** |
| **RNF05** | Acessibilidade Digital (WCAG 2.1 AA) | Conformidade com contraste cromático, fontes sem serifa legíveis, botões com área de toque ampla e compatibilidade com leitores de tela. | **Média (Should)** |
| **RNF06** | Disponibilidade da Aplicação | Uptime de pelo menos 99,5% nos horários de funcionamento das clínicas (segunda a sábado, das 06:30 às 20:00). | **Média (Should)** |

# Documento 02 • Formato da Solução, Público-Alvo e Funcionamento

## 1. Formato Escolhido: Plataforma Web Integrada Responsiva

A Falcon Health optou por desenvolver uma **plataforma web baseada em nuvem com design responsivo**, acessível por qualquer navegador moderno.

### Por que não um aplicativo nativo para celular?
* Pacientes de clínicas populares com frequência utilizam smartphones com capacidade de armazenamento reduzida e planos de dados móveis limitados. Exigir o download obrigatório de um aplicativo de dezenas de megabytes cria uma barreira imediata de adesão.
* A plataforma web é acessada diretamente por links curtos enviados via mensagem, sem necessidade de download nas lojas de apps.

### Por que não um software instalado localmente (Desktop)?
* Softwares locais exigem atualização manual em cada máquina, geram custos contínuos de suporte e mantêm os dados presos fisicamente nas filiais.
* A plataforma web roda em nuvem com sincronização instantânea em qualquer computador já existente nas recepções e consultórios, mantendo custo zero de nova infraestrutura física.

---

## 2. Quem Utilizará a Solução (Mapeamento de Usuários)

| Perfil | Meio de Acesso | Necessidades Principais |
|---|---|---|
| **Pacientes** | Celular / Navegador móvel | Visualizar especialidades, escolher horários, receber lembretes e confirmar presenças com um clique. |
| **Recepcionistas** | Computador da clínica | Visualizar agenda do dia, registrar check-in presencial, gerenciar desistências e controlar a fila da recepção. |
| **Profissionais de Saúde** | Computador ou tablet no consultório | Acessar lista de pacientes do dia, visualizar prontuário básico de filiais parceiras e prescrever orientações clínicas. |
| **Gestores da Rede** | Computador administrativo | Monitorar taxa de ocupação, horários com maior ausência de pacientes e distribuição de especialidades por filial. |

---

## 3. Como a Solução Funciona na Prática

1. **Agendamento Central:** Seja pela internet pelo próprio paciente ou presencialmente via recepcionista, o sistema bloqueia o horário no banco de dados centralizado em milissegundos, impedindo duplicações.
2. **Confirmação Automatizada:** 24 horas antes do horário marcado, o paciente recebe uma mensagem automática (SMS/WhatsApp) com os botões "Confirmar" ou "Desmarcar". Em caso de desmarcação, o slot de horário volta imediatamente à disponibilidade pública.
3. **Recepção e Sala de Espera:** Ao chegar à clínica, a recepcionista clica em "Check-in". O médico visualiza no seu painel que o paciente está na sala de espera.
4. **Atendimento Clínico:** O médico abre o prontuário básico, analisa os atendimentos anteriores registrados em qualquer filial e insere notas e condutas do dia.

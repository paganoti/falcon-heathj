# Publicação no LinkedIn • Christian (Back-end & Banco de Dados)

### Texto da Publicação:

Evitar que dois pacientes reservem a mesma consulta médica no mesmo segundo é um dos maiores desafios de arquitetura quando integramos filiais em nuvem.

Na **Falcon Health**, assumi a responsabilidade da arquitetura back-end e da modelagem de dados para eliminar de vez os conflitos de agenda que atormentavam a rede de clínicas populares. Ao migrar agendas isoladas em planilhas para uma base centralizada, a integridade dos dados tornou-se uma prioridade inegociável.

Implementamos rotas de API com regras transacionais atômicas (ACID) no banco de dados relacional. Cada alteração de status — da reserva ao check-in presencial — reflete instantaneamente em todas as recepções da rede, impedindo reservas sobrepostas (*overbooking*) sob condições concorrentes de acesso.

Tecnologia confiável nos bastidores é o que garante tranquilidade aos médicos e respeito ao tempo do paciente.

#Backend #EngenhariaDeSoftware #FalconHealth #BancoDeDados #APIs #Cloud #PostgreSQL #ArquiteturaDeSistemas

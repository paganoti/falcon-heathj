# Falcon Health

Plataforma Web Integrada para Gestão de Clínicas Populares

---

## Equipe

| # | Papel | Integrante |
|---|---|---|
| 1 | Product Owner (PO) / Analista de Requisitos | João Pedro |
| 2 | Designer de Experiência e Interface (UX/UI) | Claudelisson |
| 3 | Engenheiro de Back-end e Banco de Dados | Christian |
| 4 | Engenheiro Front-end | Pedro Henrique |
| 5 | Analista de Segurança da Informação e Privacidade | Enzo Paganoti |


---

## Sobre o Projeto

A Falcon Health Soluções Digitais é uma empresa de HealthTech focada em desenvolver soluções web integradas em nuvem para modernizar clínicas populares. O objetivo é centralizar agendamentos, reduzir conflitos operacionais e garantir comunicação rápida entre pacientes e equipe clínica.

### O Problema

Processos manuais fragmentados — mensagens, ligações e planilhas desconexas — resultam em:

- Agendamentos duplicados (overbooking)
- Histórico do paciente inacessível entre filiais
- Altas taxas de faltas (no-show)
- Filas desorganizadas na recepção

### A Solução

Uma Plataforma Web Integrada Responsiva, acessível diretamente pelo navegador, sem exigir instalação de softwares nas clínicas nem aplicativos pesados para os pacientes.

**Público-alvo:**

| Perfil | Benefício Principal |
|---|---|
| Pacientes | Agendamento facilitado e lembretes automáticos |
| Recepcionistas | Gestão da fila e agenda unificada |
| Médicos | Prontuário básico unificado entre filiais |
| Gestão | Indicadores de faltas e ocupação |

---

## Requisitos do Sistema (Metodologia MoSCoW)

### Requisitos Funcionais (RF)

| Cód. | Requisito | Prioridade |
|---|---|---|
| RF01 | Gestão de Agendamentos (marcação, reagendamento, cancelamento com trava em tempo real) | Alta (Must) |
| RF02 | Unidades e Especialidades (cadastro de médicos, salas e horários por unidade) | Alta (Must) |
| RF03 | Painel de Recepção / Fila (check-in e status da sala de espera) | Alta (Must) |
| RF04 | Prontuário Básico Unificado entre filiais | Alta (Must) |
| RF05 | Controle de Perfis (RBAC) | Alta (Must) |
| RF06 | Lembretes Automáticos via WhatsApp/SMS | Média (Should) |
| RF07 | Portal do Paciente | Média (Should) |
| RF08 | Painel Analítico de Gestão | Baixa (Could) |

### Requisitos Não Funcionais (RNF)

| Cód. | Critério | Prioridade |
|---|---|---|
| RNF01 | Segurança e LGPD (TLS 1.3, dados cifrados, auditoria) | Alta (Must) |
| RNF02 | Integridade e Concorrência (bloqueio transacional) | Alta (Must) |
| RNF03 | Responsividade (desktop e mobile) | Alta (Must) |
| RNF04 | Desempenho de Carga (< 3s em redes 3G/4G) | Média (Should) |
| RNF05 | Acessibilidade (WCAG) | Média (Should) |
| RNF06 | Disponibilidade de Serviço (uptime ≥ 99,5%) | Média (Should) |


---

## Estrutura do Projeto Web

```
falcon-health/
├── frontend/
│   ├── public/                     # Arquivos estáticos (favicon, imagens, manifest)
│   ├── src/
│   │   ├── assets/                 # Imagens, ícones e fontes
│   │   ├── components/             # Componentes reutilizáveis (botões, cards, modais)
│   │   ├── pages/                  # Telas da aplicação (Login, Agenda, Fila, Prontuário)
│   │   ├── services/                # Consumo da API (chamadas HTTP)
│   │   ├── hooks/                  # Hooks customizados
│   │   ├── routes/                 # Definição de rotas da aplicação
│   │   ├── styles/                 # Estilos globais / configuração Tailwind
│   │   └── App.jsx
│   ├── package.json
│   └── vite.config.js
│
├── backend/
│   ├── src/
│   │   ├── controllers/            # Regras de entrada das requisições
│   │   ├── services/               # Regras de negócio (ex: validação de conflito de agenda)
│   │   ├── models/                 # Modelagem das entidades (Paciente, Médico, Consulta)
│   │   ├── routes/                 # Definição dos endpoints da API REST
│   │   ├── middlewares/            # Autenticação (JWT), RBAC e tratamento de erros
│   │   ├── config/                 # Configuração de banco de dados e variáveis de ambiente
│   │   └── server.js
│   ├── database/
│   │   ├── migrations/             # Scripts de criação/alteração de tabelas
│   │   └── seeds/                  # Dados iniciais para testes
│   ├── package.json
│   └── .env.example
│
├── docs/
│   ├── 01-problema-e-solucao.md
│   ├── 02-requisitos-e-prioridades.md
│   ├── 03-papeis-profissionais.md
│   ├── 04-seguranca-privacidade.md
│   └── 05-organizacao-e-decisoes.md
│
├── .gitignore
└── README.md
```

---

## Segurança e Privacidade (LGPD)

O projeto adota Privacy by Design desde a concepção:

- Criptografia TLS 1.3 em trânsito e dados sensíveis cifrados em repouso
- Trilha de auditoria completa de acessos
- Controle de acesso granular por papel (RBAC)
- Conformidade com a LGPD/ANPD e políticas de retenção de dados


---

## Licença

Projeto acadêmico interdisciplinar — uso educacional.

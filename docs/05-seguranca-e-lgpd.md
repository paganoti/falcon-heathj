# Documento 05 • Segurança da Informação, LGPD, Riscos e Acessibilidade

## 1. Tratamento de Dados Sensíveis de Saúde (LGPD)

O sistema da **Falcon Health** lida diretamente com dados pessoais sensíveis (Art. 5º da Lei 13.709/2018 - LGPD). Foram adotadas as seguintes salvaguardas:

### 1.1 Controle de Acesso Baseado em Papéis (RBAC - Role-Based Access Control)
As informações são compartimentadas de acordo com a real necessidade da função desempenhada:
* **Recepcionistas:** Acessam dados cadastrais básicos (nome, telefone, documento, data e horário da consulta). **Não têm acesso a diagnósticos, receitas ou prontuários**.
* **Médicos:** Acessam dados cadastrais e o histórico clínico de atendimentos anteriores dos pacientes que estão na sua fila de espera do dia.
* **Pacientes:** Acessam unicamente as informações referentes ao seu próprio perfil e histórico.
* **Administradores:** Acessam indicadores agregados (gráficos e taxas de ausência), sem visualização de dados nominais de diagnósticos.

### 1.2 Trilha de Auditoria (Logs Imutáveis)
Cada visualização, inclusão ou alteração em um prontuário médico gera um registro automático contendo:
* Identificador do usuário que acessou;
* Carimbo de data e hora (*timestamp*);
* Endereço IP e ação realizada (ex: *visualizou prontuário*, *anexou prescrição*).

### 1.3 Criptografia
* **Em Trânsito:** Todo o tráfego de dados entre navegadores e o servidor é criptografado obrigatoriamente via HTTPS com protocolo TLS 1.3.
* **Em Repouso:** Os campos de histórico clínico e documentos sensíveis no banco de dados são cifrados utilizando o padrão AES-256.

---

## 2. Acessibilidade e Inclusão Digital (WCAG 2.1 AA)

Como a rede atende públicos populares, incluindo idosos e pessoas com baixo domínio digital:
* **Contraste de Cores:** Índices de contraste superiores a 4.5:1 para permitir leitura nítida mesmo sob a luz do sol em telas simples.
* **Tipografia e Botões:** Textos sem serifa com tamanho mínimo de 16px e botões de toque de pelo menos 48x48px para facilitar o clique em telas de celulares menores.
* **Compatibilidade com Leitores de Tela:** Estrutura em HTML5 semântico com marcações ARIA para suporte a pessoas com deficiência visual.

---

## 3. Matriz de Riscos e Planos de Contingência

| Risco Identificado | Nível de Severidade | Medida Preventiva da Falcon Health |
|---|---|---|
| **Oscilação ou queda de internet na clínica** | Alta | Cache local do navegador para manter a lista do dia acessível offline temporariamente até a reconexão. |
| **Tentativa de invasão / vazamento de dados** | Crítica | Bloqueio de IP após tentativas consecutivas de login, firewall de aplicação e auditoria contínua de vulnerabilidades. |
| **Resistência inicial dos funcionários à nova ferramenta** | Média | Interface simplificada com fluxos de no máximo 3 cliques e roteiro de treinamento direto na recepção. |

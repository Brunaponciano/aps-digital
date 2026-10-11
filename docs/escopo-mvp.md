# Escopo do MVP — App do Paciente

> **Fase 1 do APS Digital**  
> **Status:** Em detalhamento  

---

## 1. O que é o MVP do APS Digital?

O **Mínimo Produto Viável (MVP)** foca exclusivamente na **Fase 1: Aplicativo do Paciente**. O objetivo é entregar uma aplicação funcional, compreensível, segura e pronta para demonstração no portfólio acadêmico, cobrindo os fluxos prioritários de cuidado na Atenção Primária à Saúde.

---

## 2. Funcionalidades Incluídas no MVP

### A. Cadastro, Acesso e Gestão de Perfil
- **Identificação do Paciente:**
  - Informar CPF ou CNS e Data de Nascimento (identificação fictícia no protótipo acadêmico).
  - E-mail e confirmação de e-mail.
  - Celular e senha segura (com confirmação).
- **Vínculo Territorial e Endereço:**
  - Informar CEP, rua, número e bairro.
  - Indicação obrigatória da Agente Comunitária de Saúde (ACS).
  - Caso o paciente informe que não sabe quem é sua ACS, o sistema orienta o comparecimento à UBS para verificação de território e não conclui o cadastro sem vínculo.
- **Validação:** Envio e confirmação de código fictício via SMS para ativação da conta.
- **Múltiplos Perfis no Mesmo Aparelho:**
  - Suporte para famílias que compartilham o smartphone.
  - Lista de contas previamente utilizadas no aparelho, exigindo autenticação individual para acesso aos dados de saúde.
- **Atualização de Endereço:**
  - Permite alterar o endereço sem perder a conta nem o histórico.
  - Atualização do vínculo com nova UBS/Equipe conforme regras territoriais.

---

### B. Gestão de Consultas
- **Agendamento:**
  - Escolha do tipo de atendimento: **Médico** ou **Enfermeiro**.
  - Restrição de profissionais: O sistema exibe exclusivamente profissionais da **equipe de saúde da família à qual o paciente está vinculado**.
  - Seleção de data e horário disponíveis.
  - Confirmação do agendamento com gravação na área "Meus agendamentos".
- **Visualização e Acompanhamento:**
  - Lista de consultas futuras e histórico de atendimentos passados.
- **Reagendamento:**
  - Alteração de data/horário respeitando a disponibilidade da equipe, atualizando automaticamente os lembretes para evitar duplicidade.
- **Cancelamento:**
  - Opção de cancelamento prévio para liberação do horário para outros usuários da comunidade.

---

### C. Vacinação ("Minhas vacinas")
- **Histórico Vacinal:** Visualização das vacinas já registradas.
- **Próximas Doses:** Previsão de datas para próximas doses conforme o calendário básico.
- **Alertas de Atraso:** Identificação de vacinas em atraso, com orientação para comparecimento à UBS com a caderneta física.
- **Critério de Segurança da Informação:** O sistema nunca afirma que uma vacina "não foi tomada" apenas pela ausência de registro eletrônico (respeito a possíveis desatualizações no cadastro).

---

### D. Medicamentos e Receitas ("Minhas retiradas")
- **Histórico de Dispensação:** Consulta ao histórico de retiradas realizadas na farmácia da UBS.
- **Controle de Receitas de Uso Contínuo:** Visualização da validade das receitas registradas.
- **Alerta de Vencimento:** Notificação com 14 dias de antecedência antes do término da validade da receita.
- **Sem Renovação Automática:** O aplicativo deixa explícito que a renovação depende de avaliação e rotina da UBS, orientando o usuário a procurar o serviço em tempo hábil.

---

### E. Sistema de Notificações
- **Canais:** Notificações locais no dispositivo (push) e Central de Notificações com histórico dentro do próprio app.
- **Prazos Definidos:**
  - **Consultas:** 24 horas antes do horário marcado.
  - **Vacinas:** 2 dias antes da data prevista.
  - **Receitas:** 14 dias antes do vencimento.
- **Consistência:** Cancelamento ou reagendamento de consultas cancela ou atualiza imediatamente os alertas correspondentes.

---

## 3. O que NÃO faz parte do MVP (Fora de Escopo)

Para manter o foco, o aprendizado estruturado e a viabilidade do projeto, os seguintes itens **não serão incluídos no MVP**:

| Item Fora do Escopo | Justificativa |
|---|---|
| **Resultados de Exames** | Funcionalidade removida expressamente do escopo inicial para evitar complexidade desnecessária de integrações laboratoriais. |
| **Renovação Automática de Receita** | Depende de ato médico/prescrição e protocolos clínicos locais que não cabem ao app decidir. |
| **Dispensação Automática de Remédios** | A entrega depende de estoque físico e conferência na farmácia da UBS. |
| **Sistema Web da UBS (Fase 2)** | Será desenvolvido após o fechamento e validação do App do Paciente. |
| **App do ACS (Fase 3)** | Previsto para expansão futura do projeto. |
| **Integração Real com Sistemas Nacionais (e-SUS / ConecteSUS)** | Sistemas oficiais não oferecem APIs públicas abertas; utilizaremos uma base de dados local simulada/fictícia com rigor acadêmico. |

---

## 4. Regras de Negócio Preliminares (RN)

1. **RN01 - Vínculo Territorial Obrigatório:** Não é permitido concluir o cadastro de paciente sem vinculação a um endereço coberto por uma equipe/ACS da UBS.
2. **RN02 - Agendamento Restrito à Equipe:** O paciente só pode marcar consultas com profissionais vinculados à sua equipe de saúde da família.
3. **RN03 - Isolamento de Contas Compartilhadas:** Um dispositivo com múltiplas contas nunca deve exibir informações médicas de outro usuário sem senha válida.
4. **RN04 - Sincronização de Lembretes:** Reagendamento ou cancelamento de consulta deve obrigatoriamente anular o lembrete anterior e reprogramar o novo.
5. **RN05 - Integridade do Registro Vacinal:** A ausência de registro de dose deve ser tratada como "Sem registro no sistema", orientando a conferência presencial da caderneta física.
6. **RN06 - Preservação de Identidade em Mudança de Endereço:** A alteração de endereço atualiza o território e equipe, mas preserva o histórico de saúde do usuário.

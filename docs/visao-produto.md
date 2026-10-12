# Visão do Produto — APS Digital

> **Referência:** Issue #1 — Definir visão e objetivos do APS Digital  
> **Conceito:** "Comunicação, gestão e cuidado a um clique."  
> **Status:** Aprovado  

---

## 1. O Problema e a Oportunidade

Na rotina da Atenção Primária à Saúde (APS) e das Unidades Básicas de Saúde (UBS), observam-se dificuldades frequentes que impactam diretamente a continuidade do cuidado:

- **Faltas em consultas agendadas** (absenteísmo), deixando horários ociosos e gerando filas.
- **Dificuldade de agendamento:** Pacientes deixam de marcar consultas preventivas ou de rotina devido à necessidade de deslocamento físico até a UBS apenas para o agendamento.
- **Atraso e esquecimento vacinal:** Dificuldade em acompanhar o calendário de imunização de adultos e crianças da família.
- **Interrupção de tratamentos contínuos:** Pacientes esquecem o prazo de validade das receitas de medicamentos contínuos e só percebem que a receita venceu quando já estão na farmácia da UBS.

O **APS Digital** surge para aproximar o cidadão da sua equipe de saúde através de uma solução digital simples, acessível e segura.

---

## 2. Visão e Proposta de Valor

O **APS Digital** é uma plataforma focada em organizar a comunicação entre a comunidade e a Atenção Primária à Saúde, fortalecendo o vínculo territorial entre o paciente e a sua equipe de referência (médico, enfermeiro e Agente Comunitário de Saúde - ACS).

**Objetivos principais:**
- Facilitar o agendamento e o gerenciamento de consultas básicas.
- Reduzir o absenteísmo por meio de lembretes automáticos pontuais.
- Apoiar o cumprimento do calendário vacinal.
- Prevenir a interrupção de medicamentos contínuos avisando antecipadamente sobre o vencimento de receitas.
- Valorizar o vínculo territorial com a UBS e a ACS de referência.

---

## 3. Público-Alvo e Realidade de Uso

O projeto foi desenhado para **qualquer usuário atendido pelo SUS na APS**, considerando características socioeconômicas reais:

- **Aparelhos celulares compartilhados:** É comum em uma mesma família que vários membros (pais, filhos, idosos) utilizem o mesmo smartphone. O sistema permite alternar entre contas individuais no mesmo aparelho com segurança.
- **Acesso a dependentes:** Responsáveis precisam acompanhar as consultas, vacinas e receitas de crianças ou pessoas dependentes sob sua tutela.
- **Simplicidade de uso:** Interface intuitiva, acessível e com vocabulário claro, evitando barreiras para pessoas com menor letramento digital.

---

## 4. Estrutura e Fases de Desenvolvimento

O ecossistema do APS Digital foi planejado para ser construído em 4 etapas complementares:

```
APS Digital
│
├── Fase 1: App do Paciente (MVP Atual)
│     └── Acompanhamento de consultas, vacinas, receitas e lembretes
│
├── Fase 2: Sistema Web da UBS
│     └── Gestão de agendas, equipes, acolhimento e equipe eMulti
│
├── Fase 3: App do ACS
│     └── Acompanhamento territorial, visitas domiciliares e cadastro de famílias
│
└── Fase 4: Dados e Indicadores
      └── Painéis gerenciais para tomada de decisão em saúde pública
```

---

## 5. Princípios de Segurança e Privacidade

- **Proteção de Dados (LGPD):** O projeto trata dados sensíveis de saúde, exigindo sigilo e controles rígidos de acesso.
- **Nenhum dado real em desenvolvimento:** Durante a fase acadêmica de desenvolvimento e demonstração de portfólio, todos os dados de pacientes (nomes, CPFs, receitas) serão estritamente fictícios.
- **Armazenamento Seguro:** Senhas nunca são armazenadas em texto simples.
- **Privacidade entre usuários:** Em dispositivos com múltiplas contas salvas, os dados de saúde de uma pessoa nunca são acessíveis a outra sem a devida autenticação.

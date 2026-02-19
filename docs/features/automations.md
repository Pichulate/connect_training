# Automações

## Visão Geral

O módulo de automações do Endeavor Connect elimina trabalho manual e padroniza a comunicação com mentores antes das mentorias. O sistema envia automaticamente **briefings** e **convites** para os mentores, garantindo que eles cheguem bem preparados para a sessão.

---

## Automações Disponíveis

### 1. Envio de Briefing para Mentores

**Quando é disparado:** Quando um meeting muda de status **Potential → Scheduled**

**O que é enviado:** Um e-mail personalizado para o(s) mentor(es) do meeting contendo:

| Seção do Briefing | Conteúdo |
|---|---|
| **Sobre a empresa** | Nome, setor, estágio e descrição da empresa |
| **Sobre os empreendedores** | Perfil dos fundadores que participarão |
| **Contexto do desafio** | Extraído do campo **Context** da Priority vinculada |
| **Desafios específicos** | Extraído do campo **Challenges** da Priority vinculada |
| **Perguntas-chave** | Extraído do campo **Key Questions** da Priority vinculada |
| **O que já foi tentado** | Extraído do campo **Test Alternatives** da Priority (se preenchido) |
| **Logística** | Data, horário, formato (presencial/online) e informações de acesso |

> **Importante:** A qualidade do briefing depende diretamente da qualidade da Priority vinculada ao meeting. Se a Priority estiver incompleta, o briefing chegará incompleto ao mentor.

---

### 2. Envio de Convite / Calendário

**Quando é disparado:** Junto com o briefing, ao mover para **Scheduled**

**O que é enviado:** Um convite de calendário (`.ics` / Google Calendar) com:
- Título da reunião
- Data e horário
- Link de videoconferência (quando aplicável)
- Nomes dos participantes
- Breve descrição da pauta

---

### 3. [Adicionar outras automações existentes]

> **Nota para o mantenedor:** Liste aqui todas as outras automações do sistema (ex: lembretes, follow-ups pós-mentoria, notificações de rating, etc.) com o mesmo padrão de documentação.

---

## Pré-requisitos para as Automações Funcionarem

Para garantir que as automações sejam disparadas corretamente e gerem comunicações de qualidade, verifique:

| Pré-requisito | Por quê é necessário |
|---|---|
| Meeting vinculado a uma Priority | O briefing usa os campos da Priority como fonte de conteúdo |
| Priority com Context, Challenges e Key Questions preenchidos | São as seções principais do briefing enviado ao mentor |
| E-mail do mentor cadastrado e atualizado | O sistema envia para o e-mail registrado no perfil |
| Data e hora definidas no meeting | Necessário para o convite de calendário |
| Formato do meeting definido | Determina se haverá link de videoconferência ou endereço presencial |

---

## O que acontece se a automação não for disparada?

Se as automações não forem disparadas (ex: meeting criado já como Completed, ou dados faltando), o envio manual é necessário. Nestes casos:

1. Verifique o log de automações do meeting (se disponível)
2. Se o briefing não foi enviado, você pode reenviar manualmente via o painel do meeting
3. Para convites de calendário, envie manualmente pelo Google Calendar

---

## Personalização das Automações

> **Nota para o mantenedor:** Descreva aqui se/como as automações podem ser personalizadas por programa, tipo de mentoria ou outros critérios. Inclua também quem tem permissão para alterar as configurações de automação.

---

## Boas Práticas

- **Nunca mova um meeting para Scheduled sem a Priority vinculada** — o briefing será enviado sem conteúdo relevante, o que é pior do que não enviar
- **Revise o preview do briefing antes de confirmar** (se o sistema oferecer essa opção) para garantir que o conteúdo está correto
- **Atualize o e-mail do mentor** no perfil se você souber que está desatualizado — antes de agendar, não depois
- **Meeting cancelado após envio do briefing?** Envie um e-mail manual de cancelamento ao mentor — o sistema pode não fazer isso automaticamente

---

## Rastreabilidade

O sistema registra o histórico de comunicações de cada meeting:
- Data e hora do envio do briefing
- Status do convite (enviado, aceito, recusado)
- Histórico de reenvios manuais

> **Nota:** Adicione aqui detalhes de como visualizar o log de automações de um meeting específico.

# Endeavor Connect — Visão Geral do Sistema

## O que é o Endeavor Connect

O **Endeavor Connect** é o sistema interno de gestão de mentoring da Endeavor Brasil. Ele é a plataforma central onde os colaboradores registram, organizam e acompanham todas as interações entre empreendedores e mentores dentro dos programas da Endeavor.

O sistema é **mandatório para todos os colaboradores** que trabalham com programas de aceleração e mentoring.

---

## Para que serve

O Endeavor Connect centraliza três grandes eixos de trabalho:

1. **Gestão de meetings** — registro e acompanhamento de mentorias entre empreendedores e mentores, organizado em um pipeline Kanban
2. **Gestão de priorities** — registro dos principais desafios dos empreendedores, que alimenta um fluxo de recomendação automática de mentores
3. **Automações** — envio automatizado de briefings e convites para mentores antes das mentorias

---

## Principais módulos

| Módulo | Função principal |
|---|---|
| **Busca** | Localizar empresas do portfólio e mentores cadastrados |
| **Meetings** | Pipeline Kanban de mentorias (Potential → Scheduled → Completed) |
| **Priorities** | Registro de desafios estratégicos dos empreendedores |
| **Automações** | Envio de briefings e convites pré-mentoria |

---

## Quem usa o sistema

- **Analistas e Gerentes de Programas** — uso diário para registrar meetings e priorities
- **Time de Operações** — garantia de qualidade dos dados e fluxos automáticos
- **Liderança** — acompanhamento de métricas e pipeline de mentoring

---

## Conceitos fundamentais

### Empresa (Portfolio Company)
Empresas do portfólio da Endeavor que participam dos programas. Cada empresa tem um perfil com informações como setor, estágio, empreendedores e histórico de mentorias.

### Mentor
Profissionais voluntários cadastrados na rede Endeavor que oferecem mentoring às empresas do portfólio. Cada mentor tem áreas de expertise, disponibilidade e histórico de meetings.

### Meeting
Registro de uma sessão de mentoring entre um ou mais mentores e empreendedores. Cada meeting passa por estágios no pipeline (Potential → Scheduled → Completed) e carrega dados estruturados sobre a sessão.

### Priority
Registro de um desafio estratégico de uma empresa. É o ponto de partida para o fluxo de recomendação de mentores — o sistema analisa os campos da priority para sugerir mentores com expertise relevante.

---

## Fluxo típico de trabalho

```
1. Analista identifica um desafio de uma empresa
       ↓
2. Cria uma Priority com contexto, desafios e key questions
       ↓
3. Sistema recomenda mentores automaticamente com base na Priority
       ↓
4. Analista cria um Meeting (status: Potential) com o mentor recomendado
       ↓
5. Meeting agendado → status muda para Scheduled
       ↓
6. Sistema envia briefing ao mentor e convite automático
       ↓
7. Mentoria acontece → Meeting marcado como Completed
       ↓
8. Analista preenche campos pós-mentoria (rating, notas, próximos passos)
```

---

## Navegação básica

> **Nota:** Adicione aqui capturas de tela e detalhes de navegação quando disponíveis.

O sistema é acessado via browser e tem as seguintes seções principais no menu:

- **Dashboard** — visão geral de atividade recente
- **Empresas** — diretório de empresas do portfólio
- **Mentores** — diretório de mentores
- **Meetings** — pipeline de mentorias
- **Priorities** — log de desafios dos empreendedores

---

*Para detalhes sobre cada módulo, consulte os documentos em `docs/features/`.*

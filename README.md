# Endeavor Connect — Knowledge Base de Onboarding

Repositório de conhecimento para onboarding técnico de novos colaboradores da **Endeavor Brasil** no sistema interno **Endeavor Connect**.

---

## O que é este repositório

Este é um knowledge base estruturado em Markdown, mantido pelo time de Produto, que centraliza toda a documentação sobre funcionalidades, fluxos e boas práticas do Endeavor Connect. Ele foi criado para ser usado junto ao **Claude.ai Projects**, funcionando como uma base de conhecimento consultável por IA.

**Casos de uso principais:**

- Fazer onboardings de 1h com novos colaboradores de forma estruturada
- Tirar dúvidas específicas sobre funcionalidades durante ou após o onboarding
- Gerar roteiros e agendas personalizadas de treinamento
- Documentar decisões de produto e fluxos complexos para referência futura

---

## Como usar com Claude.ai Projects

### Passo 1 — Criar um Projeto no Claude.ai

1. Acesse [claude.ai](https://claude.ai) e clique em **Projects** no menu lateral
2. Crie um novo projeto chamado `Endeavor Connect - Onboarding`
3. Clique em **Project instructions** e cole o conteúdo do arquivo [`CLAUDE_PROJECT_INSTRUCTIONS.md`](./CLAUDE_PROJECT_INSTRUCTIONS.md)

### Passo 2 — Adicionar os documentos como Knowledge

No painel do projeto, clique em **Add content** e faça upload dos seguintes arquivos (em ordem de prioridade):

| Arquivo | Descrição |
|---|---|
| `docs/overview.md` | Visão geral do sistema |
| `docs/features/meetings.md` | Log de meetings e Kanban |
| `docs/features/priorities.md` | Log de priorities e recomendação de mentores |
| `docs/features/search.md` | Busca de empresas e mentores |
| `docs/features/automations.md` | Automações de briefings e convites |
| `docs/onboarding/session-guide.md` | Roteiro da sessão de onboarding de 1h |
| `docs/onboarding/faq.md` | Perguntas frequentes |

> **Dica:** Sempre que atualizar um arquivo markdown aqui, substitua o arquivo correspondente no projeto Claude.ai.

### Passo 3 — Usar

Exemplos de perguntas que você pode fazer ao Claude dentro do projeto:

- *"Crie um roteiro de onboarding de 1h para uma nova pessoa do time de programas"*
- *"Como funciona o fluxo de recomendação automática de mentores?"*
- *"Quais campos são obrigatórios no log de um meeting?"*
- *"Explique o kanban de meetings para alguém que nunca usou o sistema"*

---

## Estrutura do Repositório

```
connect_training/
├── README.md                          ← Este arquivo
├── CLAUDE_PROJECT_INSTRUCTIONS.md     ← System prompt para o Claude.ai Project
│
├── docs/
│   ├── overview.md                    ← Visão geral do Endeavor Connect
│   ├── features/
│   │   ├── search.md                  ← Busca de empresas e mentores
│   │   ├── meetings.md                ← Log de meetings (Kanban + campos)
│   │   ├── priorities.md              ← Log de priorities + recomendação de mentores
│   │   └── automations.md             ← Automações pré-mentoria
│   └── onboarding/
│       ├── session-guide.md           ← Roteiro da sessão de 1h
│       └── faq.md                     ← Perguntas frequentes
│
└── sources/
    ├── README.md                      ← Como importar conteúdo de outras fontes
    ├── notion/                        ← Exports do Notion (cole aqui)
    ├── slack/                         ← Conversas relevantes do Slack (cole aqui)
    └── gdocs/                         ← Conteúdo do Google Docs/Slides (cole aqui)
```

---

## Como contribuir com novos conteúdos

### Adicionando conteúdo do Notion

1. Exporte a página do Notion como **Markdown & CSV**
2. Salve o arquivo em `sources/notion/nome-da-pagina.md`
3. Extraia as partes relevantes e incorpore nos documentos em `docs/`

### Adicionando conteúdo do Google Docs / Slides

1. No Google Docs: **File → Download → Plain text (.txt)**
2. Salve em `sources/gdocs/nome-do-documento.md` e formate como Markdown
3. Incorpore o conteúdo nos arquivos `docs/` correspondentes

### Adicionando mensagens do Slack

1. Copie e cole as conversas relevantes em `sources/slack/topico.md`
2. Adicione contexto no topo do arquivo (data, canal, participantes)
3. Use como referência ao atualizar a documentação principal

Veja o guia completo em [`sources/README.md`](./sources/README.md).

---

## Manutenção

| Situação | Ação recomendada |
|---|---|
| Nova feature lançada | Adicionar/atualizar o arquivo de feature correspondente em `docs/features/` |
| Mudança de fluxo | Atualizar o arquivo de feature E o `session-guide.md` se for relevante pro onboarding |
| Nova dúvida recorrente no onboarding | Adicionar ao `docs/onboarding/faq.md` |
| Conversa importante no Slack | Salvar em `sources/slack/` e extrair para docs se relevante |

---

*Mantido pelo time de Produto da Endeavor Brasil.*

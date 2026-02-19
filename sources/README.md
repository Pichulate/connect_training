# Como Importar Conteúdo de Outras Fontes

Esta pasta é o repositório de **conteúdo bruto** importado de outras ferramentas (Notion, Google Docs, Slides, Slack). Ela serve como staging area — você coloca o conteúdo aqui e depois incorpora as partes relevantes nos documentos principais em `docs/`.

---

## Estrutura de Pastas

```
sources/
├── README.md          ← Este arquivo
├── notion/            ← Exports do Notion
├── slack/             ← Conversas relevantes do Slack
└── gdocs/             ← Conteúdo do Google Docs, Google Slides, etc.
```

---

## Como Importar do Notion

### Método 1: Export direto (recomendado para documentos longos)
1. Abra a página no Notion
2. Clique nos `...` no canto superior direito da página
3. Selecione **Export** → **Markdown & CSV**
4. Descompacte o arquivo e renomeie para algo descritivo: `nome-da-pagina-YYYY-MM.md`
5. Cole o arquivo em `sources/notion/`

### Método 2: Copiar e colar (para trechos específicos)
1. Selecione o conteúdo relevante no Notion
2. Crie um arquivo `.md` em `sources/notion/` com um nome descritivo
3. Cole o conteúdo e adicione no topo:
   ```
   # [Título da página/seção]
   Fonte: Notion — [nome do workspace/página]
   Data de importação: YYYY-MM-DD
   ```

### Depois de importar
- Identifique quais trechos são relevantes para a documentação principal
- Copie e adapte para os arquivos correspondentes em `docs/features/` ou `docs/onboarding/`
- Mantenha o arquivo fonte em `sources/notion/` mesmo após incorporar — serve como auditoria

---

## Como Importar do Google Docs

### Para Google Docs (texto)
1. Abra o documento
2. **File → Download → Plain Text (.txt)**
3. Renomeie o arquivo para `.md` e mova para `sources/gdocs/`
4. Adicione cabeçalho no topo:
   ```
   # [Título do documento]
   Fonte: Google Docs — [link do documento]
   Data de importação: YYYY-MM-DD
   ```
5. Formate o conteúdo como Markdown onde necessário (títulos, listas, tabelas)

### Para Google Slides (apresentações)
1. Abra a apresentação
2. **File → Download → Plain Text (.txt)** ou copie o conteúdo slide por slide
3. Crie um arquivo em `sources/gdocs/` com nome descritivo
4. Organize o conteúdo por slide, indicando qual slide corresponde a qual bloco de texto
5. Útil para onboarding: apresentações podem se tornar o `session-guide.md` ou complementá-lo

---

## Como Importar Mensagens do Slack

### Para conversas relevantes
1. Localize a conversa no Slack (DM com desenvolvedor, canal de produto, etc.)
2. Copie as mensagens relevantes
3. Crie um arquivo em `sources/slack/` com nome descritivo: `topico-da-conversa-YYYY-MM.md`
4. Use o seguinte formato:

```markdown
# [Tópico da Conversa]
Canal/DM: #nome-do-canal ou DM com [Nome]
Data: YYYY-MM-DD
Participantes: [Lista de participantes]

---

## Contexto
[Breve descrição do que motivou a conversa]

---

## Conversa

**[Nome] (HH:MM):**
[Mensagem]

**[Nome] (HH:MM):**
[Mensagem]

---

## Decisões/Insights Principais
- [Decisão ou insight 1]
- [Decisão ou insight 2]
```

### O que vale a pena importar do Slack
- Explicações sobre como uma feature funciona (especialmente do desenvolvedor)
- Decisões de produto importantes com justificativa
- Edge cases e comportamentos especiais do sistema
- Bugs conhecidos e workarounds
- Contexto histórico sobre por que algo foi construído de determinada forma

---

## Convenções de Nomenclatura de Arquivos

Use sempre nomes descritivos em kebab-case com data:

| Formato | Exemplo |
|---|---|
| `[topico]-[YYYY-MM].md` | `kanban-meetings-2024-03.md` |
| `[nome-doc]-export-[YYYY-MM].md` | `apresentacao-onboarding-export-2024-11.md` |
| `slack-[topico]-[YYYY-MM].md` | `slack-fluxo-recomendacao-mentores-2024-08.md` |

---

## Ciclo de vida do conteúdo em `sources/`

```
Conteúdo bruto → sources/       Revisão manual       docs/ (documentação principal)
(Notion/Docs/Slack)       ──→   pelo PM         ──→  (incorporado e estruturado)
```

- **NÃO delete** arquivos de `sources/` mesmo após incorporá-los em `docs/` — eles são histórico
- **ATUALIZE** os arquivos em `docs/` quando o conteúdo fonte mudar
- **MARQUE** no arquivo de sources quando o conteúdo foi incorporado (ex: adicione um comentário no topo: `> Incorporado em docs/features/meetings.md em YYYY-MM-DD`)

---

## Prioridades de Importação Sugeridas

Se você tem muito conteúdo para importar, comece por:

1. **Apresentações de onboarding existentes** — já estruturadas para treinamento
2. **Docs de especificação de features** — especialmente Priorities e Meetings (features mais complexas)
3. **Conversas do Slack sobre fluxos de recomendação** — informação raramente documentada
4. **FAQs ou dúvidas já respondidas** em qualquer lugar — vão direto para `docs/onboarding/faq.md`
5. **Decisões de produto** — contexto valioso para explicar "por que as coisas são assim"

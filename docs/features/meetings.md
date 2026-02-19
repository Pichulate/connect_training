# Log de Meetings

## Visão Geral

O módulo de **Meetings** é o coração operacional do Endeavor Connect. Ele registra todas as mentorias entre empreendedores e mentores, organizadas em um pipeline **Kanban** com três estágios principais.

---

## O Kanban de Meetings

O pipeline funciona como um quadro Kanban com os seguintes estágios:

```
[ POTENTIAL ] ──→ [ SCHEDULED ] ──→ [ COMPLETED ]
```

| Estágio | Significado |
|---|---|
| **Potential** | Meeting identificado como possível/desejado, ainda não confirmado |
| **Scheduled** | Meeting confirmado com data, hora e mentor definidos |
| **Completed** | Mentoria realizada — aguarda ou já tem preenchimento pós-mentoria |

### Regras de transição
- Um meeting começa em **Potential** ao ser criado
- Move para **Scheduled** quando data e mentor são confirmados → neste momento as automações são disparadas (ver `automations.md`)
- Move para **Completed** após a realização da mentoria

---

## Campos do Meeting

### Campos de identificação

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Empresa** | Sim | Empresa do portfólio que receberá a mentoria |
| **Estágio da empresa** | Sim | Fase atual da empresa no momento do meeting (ex: Seed, Series A) |
| **Programa** | Sim | Programa Endeavor ao qual o meeting está vinculado |

### Participantes

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Mentor(es)** | Sim | Um ou mais mentores que participarão da sessão |
| **Empreendedor(es)** | Sim | Fundadores/líderes da empresa que participarão |
| **Attendings** | Não | Colaboradores da Endeavor presentes na mentoria |

### Dados da sessão

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Data** | Quando Scheduled | Data e hora da mentoria |
| **Formato** | Não | Presencial, online ou híbrido |
| **Duração** | Não | Duração prevista ou realizada da sessão |
| **Tema / Pauta** | Recomendado | Assunto principal ou desafio abordado |

### Vínculo com Priorities

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Priority relacionada** | Recomendado | Priority que originou ou está sendo abordada neste meeting |

### Campos pós-mentoria (preencher após Completed)

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Rating** | Sim | Avaliação da qualidade da mentoria (escala definida pelo sistema) |
| **Notas pós-mentoria** | Recomendado | Resumo dos principais pontos discutidos |
| **Próximos passos** | Recomendado | Ações acordadas durante a mentoria |
| **Follow-up necessário** | Não | Flag para indicar se há necessidade de acompanhamento |

---

## Como criar um Meeting

1. Localize a empresa usando a busca (ver `search.md`)
2. No perfil da empresa ou no painel de Meetings, clique em **"+ Novo Meeting"**
3. Preencha os campos obrigatórios: empresa, estágio, programa, mentor(es), empreendedor(es)
4. Salve como **Potential** para registrar a intenção
5. Quando confirmado: adicione data/hora e mova para **Scheduled**
6. Após a mentoria: mova para **Completed** e preencha os campos pós-mentoria

---

## Boas práticas

### Preenchimento de dados
- Sempre vincule o meeting a uma **Priority** quando aplicável — isso cria rastreabilidade entre desafio → mentoria
- O campo **Estágio da empresa** deve refletir o estágio no **momento do meeting**, não o atual — é dado histórico importante
- Preencha os campos pós-mentoria o quanto antes após a realização — memória fica mais fraca com o tempo

### Qualidade dos dados
- **Rating** é fundamental para o sistema aprender quais mentores têm melhor performance
- Meetings sem campos pós-mentoria preenchidos distorcem as métricas de programa
- Um meeting por empreendedor/mentor + tema específico — evite meetings genéricos

### Fluxo ideal
- Crie o meeting a partir de uma **Priority** sempre que possível, não de forma isolada
- Revise os meetings em **Potential** semanalmente — meetings esquecidos neste estágio são desperdício de oportunidade

---

## Visão em lista vs. Kanban

O módulo de meetings oferece duas visualizações:

- **Kanban** — visão de pipeline, ideal para gestão do fluxo operacional
- **Lista** — visão tabular, ideal para análise, filtros e exportação

> **Nota:** Adicione aqui detalhes específicos de interface, filtros disponíveis e capturas de tela quando disponíveis. Inclua também regras específicas de negócio de cada programa se houver.

# Log de Priorities

## Visão Geral

O módulo de **Priorities** registra os principais desafios estratégicos dos empreendedores. É mais do que um simples log — cada Priority bem preenchida alimenta o **fluxo de recomendação automática de mentores**, conectando os desafios certos com os especialistas certos.

Uma Priority representa um **desafio real e prioritário** de uma empresa em um determinado momento. Ela funciona como o ponto de partida para toda a jornada de mentoring.

---

## Campos da Priority

### Campos de identificação

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Empresa** | Sim | Empresa do portfólio dona do desafio |
| **Empreendedor responsável** | Sim | Quem está liderando ou vivendo este desafio |
| **Programa** | Sim | Programa Endeavor ao qual está vinculada |
| **Data de criação** | Automático | Gerada automaticamente pelo sistema |
| **Status** | Sim | Ativa, Em progresso, Concluída, Arquivada |

### Campos de conteúdo do desafio

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Título** | Sim | Nome curto e descritivo do desafio |
| **Context** | Sim | Contexto da empresa e da situação que gerou o desafio. Deve explicar o cenário atual, o histórico relevante e por que isso é um desafio agora |
| **Challenges** | Sim | Descrição detalhada do(s) desafio(s) específico(s). O que exatamente a empresa está enfrentando? |
| **Key Questions** | Sim | As perguntas mais importantes que precisam ser respondidas para avançar. São as "dúvidas críticas" do empreendedor |
| **Test Alternatives** | Não | Hipóteses ou alternativas que o empreendedor já cogitou ou testou. O que já foi tentado? O que está sendo considerado? |

### Campos de aprendizado e encerramento

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Learnings** | Quando concluída | O que foi aprendido ao longo do processo de mentoring desta priority |
| **Outcome** | Quando concluída | Qual foi o resultado final? O desafio foi superado? Como? |

---

## O Fluxo de Recomendação Automática de Mentores

Este é o diferencial mais poderoso do módulo de Priorities. Quando uma Priority é criada (ou atualizada) com os campos de conteúdo bem preenchidos, o sistema automaticamente:

### Como funciona

```
Priority criada/atualizada
       ↓
Sistema analisa: Context + Challenges + Key Questions
       ↓
Algoritmo de matching identifica áreas de expertise relevantes
       ↓
Sistema cruza com base de mentores cadastrados
       ↓
Lista de mentores recomendados é gerada (ordenada por relevância)
       ↓
Analista revisa e seleciona mentores para criar Meetings
```

### O que o algoritmo considera
- **Expertise dos mentores** — tags e áreas de especialização
- **Setor/vertical** — alinhamento com o setor da empresa
- **Histórico de meetings** — mentores que já atenderam a empresa (evita repetição desnecessária)
- **Qualidade do histórico** — ratings de mentorias anteriores do mentor
- **Disponibilidade** — status ativo do mentor na plataforma

### Boas práticas para maximizar a qualidade das recomendações

**A qualidade do output é diretamente proporcional à qualidade do input.** Uma Priority bem preenchida gera recomendações muito mais precisas.

| Boa prática | Por quê importa |
|---|---|
| Preencha **Context** com riqueza de detalhes | O algoritmo usa este campo para entender o cenário e o estágio da empresa |
| Use linguagem específica em **Challenges** | Termos técnicos do setor melhoram o matching de expertise |
| Formule **Key Questions** de forma direta e clara | Perguntas bem formuladas mapeiam melhor as lacunas de conhecimento |
| Inclua o que já foi tentado em **Test Alternatives** | Evita recomendar mentores que abordariam algo já descartado |
| Mantenha o **Status** atualizado | Priorities "ativas" concluídas continuam consumindo atenção do sistema |

---

## Como criar uma Priority

1. Localize a empresa usando a busca (ver `search.md`)
2. No perfil da empresa ou no painel de Priorities, clique em **"+ Nova Priority"**
3. Preencha todos os campos obrigatórios — quanto mais detalhe, melhor a recomendação
4. Salve → o sistema processa e gera as recomendações automaticamente
5. Revise a lista de mentores recomendados
6. Crie um **Meeting** a partir do mentor escolhido (o meeting já nasce vinculado à Priority)

---

## Relação entre Priorities e Meetings

Uma Priority pode ter **múltiplos meetings** vinculados — é comum que um desafio exija conversas com diferentes mentores ao longo do tempo.

```
Priority: "Como escalar vendas enterprise?"
    ├── Meeting 1: Mentor especialista em Sales Enterprise (Potential)
    ├── Meeting 2: Mentor com experiência em SaaS B2B (Completed, Rating: 5)
    └── Meeting 3: Mentor em Pricing (Scheduled)
```

- Sempre vincule o meeting à priority de origem ao criar
- O histórico de meetings de uma priority conta a história da evolução daquele desafio
- Ao encerrar uma priority, preencha **Learnings** e **Outcome** para enriquecer o histórico da empresa

---

## Boas práticas gerais

- Uma empresa deve ter no máximo **3-5 Priorities ativas** simultaneamente — mais do que isso dilui o foco
- Priorize **qualidade sobre quantidade** — uma Priority bem preenchida é mais valiosa do que dez preenchidas pela metade
- Revise Priorities ativas em ciclos regulares (ex: mensalmente) para atualizar status e aprendizados
- Ao encerrar um ciclo do programa, garanta que todas as Priorities têm **Learnings** e **Outcome** preenchidos

---

> **Nota:** Adicione aqui detalhes do algoritmo de recomendação, exemplos reais de Priorities bem preenchidas e screenshots da interface quando disponíveis.

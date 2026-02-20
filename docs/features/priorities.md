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

### Aba Match (Recomendação de Mentores)

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Matching Rationale** | Recomendado | Instruções adicionais para ajustar os pesos do algoritmo de recomendação. Quanto mais específico, mais precisa a lista gerada. Pode ser editado para regenerar a lista. Ex: *"O mentor precisa ter experiência em expansão para mercados latino-americanos e já ter passado pela fase de Series B."* |

---

## Recomendação Automática de Mentores

A Priority é o ponto de partida para a **Mentor Recommendation List** — a funcionalidade que sugere automaticamente os Top 10 mentores mais adequados para o desafio do founder. A lista é gerada na aba **"Match"** da Priority e usa um algoritmo de 4 etapas.

### Como o algoritmo funciona (resumo)

1. **Quebra em blocos:** os campos da Priority (Context, Key Questions, Tested Alternatives, Matching Rationale) são analisados e convertidos em 9 blocos de perguntas — Expertise, Cargos, Indústria, Geografia, Estágio, Business Model, Target Market, entre outros
2. **Pesos:** cada bloco recebe um peso proporcional à sua importância para aquele desafio específico
3. **Comparação:** cada bloco ponderado é comparado com os perfis de mentores em 9 categorias
4. **Top 10:** a lista é refinada com o Matching Rationale e gera os 10 nomes mais relevantes, com justificativas de match

> Para o passo a passo completo de como gerar, regenerar e interpretar a lista, veja [`mentor-recommendation.md`](./mentor-recommendation.md).

### Boas práticas para maximizar a qualidade das recomendações

**A qualidade do output é diretamente proporcional à qualidade do input.** Uma Priority bem preenchida gera recomendações muito mais precisas.

| Boa prática | Por quê importa |
|---|---|
| Preencha **Context** com riqueza de detalhes | O algoritmo usa este campo para entender o cenário e o estágio da empresa |
| Use linguagem específica em **Challenges** | Termos técnicos do setor melhoram o matching de expertise |
| Formule **Key Questions** de forma direta e clara | Perguntas bem formuladas mapeiam melhor as lacunas de conhecimento |
| Inclua o que já foi tentado em **Test Alternatives** | Evita recomendar mentores que abordariam algo já descartado |
| Preencha o **Matching Rationale** na aba Match | Ajusta os pesos do algoritmo — quanto mais específico, mais precisa a lista |

---

## Como criar uma Priority

1. Localize a empresa usando a busca (ver `search.md`)
2. No perfil da empresa ou no painel de Priorities, clique em **"+ Nova Priority"**
3. Preencha todos os campos da aba **Details** — Context, Challenges, Key Questions e, se aplicável, Test Alternatives
4. Salve a Priority
5. Navegue até a aba **"Match"**, preencha o **Matching Rationale** e clique em **"Generate Recommended List"**
6. Aguarde o processamento e revise o **Top 10 de mentores recomendados** com as justificativas de match
7. Crie um **Meeting** a partir do mentor escolhido — o meeting já nasce vinculado à Priority

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

# Mentor Recommendation List

## O que é

A **Mentor Recommendation List** é a funcionalidade do Endeavor Connect que recomenda automaticamente os melhores nomes para resolver desafios específicos (Priorities) dos founders. A lista é gerada com base nas informações preenchidas na Priority e nos perfis enriquecidos da base de pessoas mentoras.

O objetivo é **facilitar o processo de matchmaking** na hora da seleção e priorização de nomes — entregando uma lista que já tem alto potencial de match, sem a necessidade de busca manual.

> Dúvidas não cobertas por este material? Procure **@Bruno Pichulate**.

---

## Como acessar

1. Entre no Connect e selecione uma **Priority** existente no kanban ou crie uma nova
2. Dentro da Priority, navegue até a aba **"Match"**
3. O botão **"Generate Recommended List"** estará disponível para gerar a lista

---

## O campo Matching Rationale

O **Matching Rationale** é o campo onde você pode fornecer **instruções adicionais** para refinar o algoritmo de recomendação. Ele ajusta os pesos das categorias usadas para identificar similaridades com a base de mentores e melhora a precisão das recomendações.

**Por que preencher:**
- Sem Matching Rationale, o algoritmo usa apenas os campos da Priority (Context, Key Questions, Tested Alternatives) com pesos iguais
- Com Matching Rationale, você pode indicar explicitamente o que mais importa — ex: *"o mentor precisa ter experiência em mercados latino-americanos e ter passado pela fase de Series B"*
- O campo é o principal mecanismo para **refinar e regenerar** a lista quando os resultados iniciais não forem satisfatórios

---

## Gerando a lista

1. Acesse a aba **"Match"** dentro da página da Priority
2. Preencha o campo **Matching Rationale** com instruções de refinamento (recomendado)
3. Clique no botão **"Generate Recommended List"**
4. Aguarde o processamento — quando a lista estiver pronta, um ícone aparecerá no card da Priority
5. Visualize os **Top 10 mentores sugeridos**, ranqueados por relevância, cada um com uma explicação de por que é um bom match para o desafio

---

## Regenerando a lista

Há duas formas de gerar uma nova versão da lista:

### 1. Editando o Matching Rationale
- Ajuste o conteúdo do campo **Matching Rationale** com novas instruções ou refinamentos
- O botão **"Generate Recommended List"** se transforma em **"Update Recommendations"**
- Clique no botão para gerar uma nova lista baseada nos novos inputs

### 2. Resalvando campos da aba Details
- Quando os campos principais da Priority (Context, Key Questions, Tested Alternatives) forem salvos novamente, uma nova lista pode ser gerada

> Se não gostar das recomendações iniciais, utilize o campo **"Want to modify the results?"** para refinar o Matching Rationale e regenerar.

---

## Como o algoritmo funciona

A lista é gerada em **4 etapas**:

### Etapa 1 — Quebra da Priority em blocos de perguntas

O sistema utiliza os campos preenchidos na Priority (**Context**, **Tested Alternatives**, **Key Questions** e **Matching Rationale**) para entender o desafio do founder e quebrar o problema em **9 blocos de perguntas** que precisam ser respondidas para encontrar o mentor ideal:

| Bloco | Pergunta que o algoritmo responde |
|---|---|
| **Expertise** | Qual expertise técnica o mentor precisa ter? |
| **Cargos (Roles)** | Quais cargos o mentor deve ter ocupado? |
| **Indústria (Industry)** | Em qual indústria/setor o mentor precisa ter experiência? |
| **Geografia (Geography)** | Quais geografias o mentor precisa conhecer? |
| **Estágio (Stage)** | Em qual estágio de empresa o mentor já atuou? |
| **Business Model** | Qual modelo de negócio o mentor conhece bem? |
| **Target Market** | Qual mercado-alvo o mentor tem experiência? |
| + 2 outros blocos | Definidos dinamicamente de acordo com o desafio |

### Etapa 2 — Atribuição de pesos

Cada um dos 9 blocos é classificado por **importância**, de acordo com o desafio específico, e recebe um peso proporcional.

**Exemplo:** se o founder está lidando com expansão para os EUA, o bloco **Geography** recebe mais peso do que o bloco **Industry**.

### Etapa 3 — Comparação com perfis de mentores

Cada bloco ponderado é comparado com os perfis das pessoas mentoras, analisando as mesmas 9 categorias (Expertise, Industry, Stage, Business Model, Target Market, Geography, etc.) para identificar similaridades e gerar uma lista inicial de candidatos.

### Etapa 4 — Classificação final

A lista inicial é refinada levando em conta o **Matching Rationale** e as informações mais relevantes dos mentores, gerando os **Top 10 nomes mais recomendados** — cada um acompanhado de uma explicação que destaca por que aquele mentor é um bom match para o desafio.

---

## FAQ

**Quantos mentores serão sugeridos?**

A lista final conterá os **Top 10 mentores**, ranqueados com base nos critérios mais relevantes para a Priority.

**O que fazer se não gostar das recomendações?**

Utilize o campo **"Want to modify the results?"** para refinar as instruções do Matching Rationale e regenere a lista. Quanto mais específico o Matching Rationale, mais precisa tende a ser a nova lista.

**Por que devo preencher o Matching Rationale?**

O Matching Rationale ajusta os pesos das categorias usadas para identificar as principais similaridades com a base de mentores, melhorando a precisão das recomendações. Ele também é usado para refinar a lista final, garantindo nomes mais alinhados ao desafio da Priority.

**A lista é gerada automaticamente ao salvar a Priority?**

Não. A geração é sempre iniciada manualmente pelo botão **"Generate Recommended List"** (ou **"Update Recommendations"**, no caso de regeneração). O sistema não gera a lista de forma passiva sem ação do usuário.

---

## Relação com outros módulos

- **Priorities** — a Mentor Recommendation List é acionada a partir de uma Priority. Veja os campos relevantes em [`priorities.md`](./priorities.md)
- **Meetings** — após escolher um mentor da lista, o próximo passo é criar um Meeting vinculado à Priority. Veja [`meetings.md`](./meetings.md)

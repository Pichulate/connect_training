# Log de Meetings

## O que é uma Meeting?

Meeting é um **registro de uma conexão entre pessoas mentoras e empreendedoras** que ocorreu por intermediação da Endeavor. Inclui o registro de mentorias, mentorias avaliativas, eventos, mentorias coletivas e outras interações.

> Todas as meetings devem ser criadas e gerenciadas pelo **Endeavor Connect**. O sistema está integrado ao SalesForce — qualquer alteração feita no Connect é refletida no SF praticamente em tempo real (e vice-versa, com possível delay de algumas horas).

---

## O Kanban de Meetings

O pipeline funciona como um quadro Kanban com os seguintes estágios:

```
[ POTENTIAL ] ──→ [ SCHEDULED ] ──→ [ COMPLETED ]
                        ↓
               [ CANCELLED / NO RESPONSE / REFUSED ]
```

| Status | Quando usar |
|---|---|
| **Potential** | Toda potencial conexão que esteja no radar. Use no momento em que souber que quer realizar uma conexão com aquele mentor. |
| **Scheduled** | Depois de confirmar data e horário e disparar invites para ambas as partes. A data deve ser **maior** que a data atual. |
| **Completed** | Ao final da meeting. A data deve ser **igual ou menor** que a data atual. |
| **Cancelled** | Quando uma mentoria já agendada (Scheduled) for cancelada por qualquer uma das partes. |
| **No Response** | Quando o mentor/a não respondeu ao pedido de mentoria enviado. |
| **Refused** | Quando o mentor/a respondeu recusando o pedido de mentoria. |

> **Importante:** Registrar Cancelled, No Response e Refused é fundamental — esses dados geram visibilidade sobre o comportamento da rede mediante os convites enviados.

---

## Campos da Meeting

### Aba General Info

| Campo | Obrigatório | Como preencher |
|---|---|---|
| **Company** | Sim | Empresa para qual a meeting será realizada. Para aparecer na lista, precisa ter uma Account criada no SalesForce. |
| **Stage** | Sim | Etapa do funil: Scale-Up, EE, EE Selection, etc. Determina quais Types ficam disponíveis. |
| **Type** | Sim | Tipo da meeting. As opções dependem do Stage selecionado. Ver seção "Meeting Types" abaixo. |
| **Subject** | Sim | One liner sobre o que é aquela conexão — idealmente com contexto adicional do desafio, o grande tema da mentoria. **Máximo 80 caracteres.** O resto do time deve olhar para isso e rapidamente saber do que se tratou. Filtros de Keywords buscam aqui também. |
| **Date / Time** | Quando Scheduled | Dia e horário em que a meeting acontecerá. Pré-preenchido automaticamente ao criar, mas pode ser editado. |
| **Duration (minutos)** | Não | Estimativa de duração da meeting. |
| **Status** | Sim | Ver tabela de status acima. Pré-preenchido automaticamente. |

> **Title gerado automaticamente:** O título da meeting é criado automaticamente pela junção de **Stage + Type + Subject**. Não é necessário colocar o nome do mentor ou da conta.

### Aba Attendees

| Campo | Obrigatório | Descrição |
|---|---|---|
| **Attendee (person)** | Obrigatório em Completed | Nome da pessoa (empreendedora, mentora ou staff). Precisa ter um Contact criado no SF. Para mentores, o campo "Relationship to Endeavor" do SF deve estar atualizado. |
| **Role** | Sim | **Received** = empreendedor(a) que recebe a mentoria; **Donated** = mentor(a) que doa horas; **Neutral** = staff da Endeavor que acompanha. |

> Você pode criar uma meeting em **Potential ou Scheduled sem os Attendees** — o campo só é obrigatório em **Completed**.

> **Application não precisa mais ser preenchida** — funciona de forma automática baseada nos registros dos Contacts no SalesForce. É importante manter os Contacts sempre atualizados.

### Aba Review (preencher após Completed)

| Campo | Obrigatório | Como preencher |
|---|---|---|
| **Challenge** | Recomendado | Os **dois principais desafios** (Functional Skills) abordados na meeting. Ao adicionar um challenge, presume-se que a pessoa Donated tem entendimento sobre aquele tema — isso enriquece o histórico de giveback e a busca por critérios. |
| **Topics** | Recomendado | Subconjunto de tags que quebram o challenge em micro-temas. Usar o formato `#palavra`. Ex: `#ICP`, `#GTM`, `#go-to-market`. Objetivo: construir um mapa mental detalhado sobre os domínios de habilidade do mentor. |
| **Transcript Link (Meeting Notes)** | Recomendado | Link para as notas da meeting. **Só aceita links** — não é permitido adicionar texto diretamente. |
| **1-5 satisfied with connection** | Recomendado | Nível de satisfação do gestor de contas em relação à conexão. Com o tempo, alimenta os UPVOTES nas características do perfil do mentor. |
| **Mentor's highlights** | Recomendado | Pontos positivos da pessoa mentora (no processo e durante a mentoria): Appointment agility, Previous preparation, Active listening, Contextual adaptation, Actionable feedback. |
| **Mentor's lowlights** | Recomendado | Pontos negativos: Challenging scheduling, Unprepared mentor, Difficulty listening, Generic advice, Contextual gap. |
| **Mentor's key characteristics** | Recomendado | Características de personalidade: Curious, Pragmatic, Suggestive, Detail-oriented, Succint, Charismatic, Endevorised. |

### Aba Staff Feedbacks

| Campo | Obrigatório | Como preencher |
|---|---|---|
| **Send Rating** | Recomendado | Botão para enviar avaliação para Donated e Received após a meeting. Só aparece para types específicos e após Completed. Meta da Endeavor: 50% de resposta — para isso o envio deve ser próximo de 100%. |

> **Regras do Send Rating:**
> - Formato do número: `55 + DDD + número`
> - Após enviar, o botão fica bloqueado por 24h
> - Fluxo: *Rating sent* → *Waiting for response* → *Partial Response Received* → *Response Received*
> - Se não tiver número de um C-level, criar uma Affiliation no SF e adicionar o telefone no campo Mobile

---

## Meeting Types

As opções de Type dependem do **Stage** selecionado. Abaixo os principais types e quando usar:

| Type | Stage | Quando usar | Regras de Subject |
|---|---|---|---|
| **Checkpoint / Onboarding** | EE, EE Selection, Scale-Up | Quando precisa coletar informações ou atualizar o plano de trabalho com o founder — sem doação de horas de nenhuma parte. | — |
| **Diagnostics** | Scale-Up | Quando o founder não tem claro seus principais desafios e quer orientação de um mentor para definir melhor o plano de aceleração. | One liner + contexto adicional do desafio. |
| **Godparent Mentoring** | Scale-Up | Sessões **consecutivas** com a mesma pessoa mentora, com evolução e acompanhamento periódico do desafio. | One liner. Ex: *Geração de demanda B2B SMB por canais* |
| **Spot Mentoring** | Scale-Up | **Única sessão** para sanar um desafio pontual, sem necessidade de acompanhamento perene com o mesmo mentor. | One liner. |
| **Mentoring** | EE, EE Selection | Mentoria para sanar um desafio do empreendedor. Diferenciar entre [Spot] e [Contínua] no Subject. | Usar prefixos: `[Coaching]`, `[Benchmark]`, `[Acesso a mercados]`, `[Fundraising]`, `[Intro a Advisor]` quando aplicável. |
| **Founder to Founder** | EE Selection, Scale-Up | Conexão entre founders para troca de experiências entre pares ou com referências de mercado. | One liner. |
| **Meetup / Gathering** | EE, EE Selection, Scale-Up | Quando há uma pessoa doando horas para um grupo / Gathering: encontro só entre empreendedores sem donated específico. | — |
| **P2P (Group)** | EE, EE Selection, Scale-Up | Somente reuniões do programa P2P — grupo com alta sinergia e encontros periódicos. | — |
| **Investor Intro** | EE, EE Selection, Scale-Up | Apoio em captação com introdução a fundos. | `[SUP Ventures]`, `[Catalyst]`, `[Fundo Global]` quando aplicável. |
| **Commercial Intro** | EE, EE Selection, Scale-Up | Introdução com potenciais parcerias comerciais com Corporates da rede. | — |
| **Partnership Intro** | EE, EE Selection, Scale-Up | Demandas que podem criar sinergias de parceria entre empresas da rede. | — |
| **Talent Intro** | EE, EE Selection, Scale-Up | Introdução com potenciais talentos para a empresa apoiada. | `[Checagem de referência]` quando aplicável. |
| **Connection to EE's Team** | EE | Conexão focada em resolver desafio de alguém do time (não o EE/C-level). | One liner. |
| **EE Advisory Board Meeting** | EE | — | `[Comitê Estratégico]` quando aplicável. |
| **2nd Opinion Review** | EE Selection | Etapa do processo seletivo de EE — verificar se a empresa está apta para o Painel Local. | — |
| **Financial Review** | EE Selection | Etapa seletiva com foco em métricas financeiras. | — |

### Features habilitadas por Type

Nem todos os types têm as mesmas funcionalidades disponíveis. As principais:

- **AI Generated Meeting Summary** — disponível em: Godparent Mentoring, Spot Mentoring, Mentoring, Meetup / Gathering
- **AI Suggested Priorities** — disponível em: Checkpoint
- **Entrepreneur's Priorities — Related Meeting** — disponível na maioria dos types
- **Keywords Criteria Filters Search** — disponível em todos
- **Mentor's Profile Modal (Last Meetings)** — disponível em todos
- **Send Rating** — disponível em: Diagnostics, Godparent Mentoring, Spot Mentoring, Mentoring, 2nd Opinion Review, Financial Review

---

## Stages e Relação com SalesForce

| Produto | Meeting Stage (Connect) | Stage no SF |
|---|---|---|
| SUP | Scale-Up | ScaleUp/Local Program |
| SUP | Scale-Up Alumni | ScaleUp/Local Program Alumni |
| SUP-O | Scale-Up Outliers / Selection | Pre-Selection |
| EE | EE | Post-Selection |
| GR/Embaixadores/Times Endeavor | Others | Non-Selection |

---

## Como criar uma Meeting

### Pela tela de Meetings
1. Clique em **+ Nova Meeting**
2. Preencha Company, Stage e Type — isso determina os campos disponíveis
3. Preencha o Subject (máx. 80 caracteres)
4. Adicione os Attendees (pode deixar para depois se ainda não confirmado)
5. Salve como **Potential**
6. Quando confirmada: adicione data/hora e mova para **Scheduled**
7. Após a mentoria: mova para **Completed** e preencha a aba Review

### Pelo perfil da pessoa mentora
Na tela de **Find Mentors and Entrepreneurs**, ao abrir o perfil de um mentor, clique em **+ Meeting** (canto superior direito). Company, Attendees Donated e Neutral virão pré-preenchidos automaticamente.

---

## Integração com SalesForce

- Alterações feitas no **Connect** refletem no SF **praticamente em tempo real** (delay de poucos minutos no máximo)
- Alterações feitas no **SF** podem demorar **algumas horas** para refletir no Connect — aguarde antes de acionar suporte
- O **histórico dos últimos 6 meses** do SF já aparece no Connect mesmo que você nunca tenha usado a feature de Meetings no Connect

---

## Analisando o histórico de meetings de um mentor

No perfil do mentor, a visualização mostra por padrão as **10 meetings mais recentes**. Você pode:
- Buscar por palavras no título da meeting
- Filtrar por ordenação (mais antigas ou mais recentes primeiro)

---

## Solução de Problemas

**Não consigo adicionar um attendee:**
As regras de aparecer um attendee são baseadas nas regras de GC existentes. Se todos os campos da entidade Contact estiverem corretos no SF e o attendee ainda não aparece, verifique o dash [Gestão do Conhecimento — Apuração](https://lookerstudio.google.com/reporting/705b54b8-ee86-4f61-a799-d323c2f9a61e/page/p_96jl7xku4c) ou entre em contato com @Nayara Fontes.

**Não consigo adicionar a empresa:**
Mesma lógica — verifique se todos os campos da entidade Account estão corretos no SF. Use o mesmo dashboard de GC.

**Sinto falta de um type que usava com frequência:**
Entre em contato com @Nayara Fontes para explorar o cenário e ajustar o sistema.

**Bug ou comportamento inesperado:**
Envie uma notificação pelo bot do Slack **"Suporte bugs e dúvidas"** no canal **#Inovação**, incluindo o link da meeting ou o SalesForce ID.

---

## Acompanhamento de Indicadores

Para acompanhar indicadores de gestão de dados (nível de preenchimento, erros, atualizações):

- **Dashboard de Gestão de Dados:** [Looker Studio](https://lookerstudio.google.com/u/0/reporting/0885be92-e583-44f1-bbd9-cbbab9cb1850/page/p_4a25ygvmjd)

---

## Vídeo Demonstrativo

O vídeo a seguir cobre: visão geral do kanban, pesquisa por empresa, mudança de visualização, criar/editar/deletar/clonar uma meeting e fazer a review.

[Assistir no Loom](https://www.loom.com/share/3474ee73c68e43a3a723a4667b2bd0bb?sid=9067db16-f9c7-447b-b2fd-33bd23209774)

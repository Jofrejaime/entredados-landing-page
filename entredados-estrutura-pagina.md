# Entredados — Estrutura Completa da Landing Page
> Versão 1.0 · Junho 2025
> Documento de arquitectura visual e editorial da página.
> Inclui: propósito de cada secção, layout, copy, uso de imagens e lógica de design.

---

## Por que as Imagens São Inegociáveis

O questionário de identidade visual da Entredados define claramente:

> *"A marca deve ser percebida como inovadora, confiável e acessível."*
> *"Uma ponte entre conhecimento técnico e aplicação prática."*
> *"Promovendo a democratização do uso de dados em Angola."*

Uma página puramente tipográfica — por mais bem construída que seja — comunica **tecnologia**. Mas não comunica **pessoas**. E o público-alvo da Entredados (gestores, directores, pesquisadores angolanos) precisa de se **ver** na página. Precisa de sentir que aquela solução foi feita para alguém como eles.

O banner existente da Entredados já valida esta decisão: a marca já usa uma pessoa real, angolana, num contexto de apresentação da plataforma. Isso não foi acidente — foi posicionamento.

### O papel técnico das imagens com blur

O blur (desfoque) não é um efeito decorativo. Tem três funções específicas:

**1. Criar profundidade sem distrair**
A imagem desfocada vive no fundo. O conteúdo (headline, copy, CTA) vive à frente. O visitante processa a emoção da imagem e a informação do texto ao mesmo tempo, em camadas separadas.

**2. Garantir contraste de leitura**
O blur + overlay escuro (`#030F0F` com 60–75% de opacidade) cria um fundo neutro e profundo sobre o qual o texto branco tem contraste máximo — sem perder a humanidade da fotografia por baixo.

**3. Dar contexto angolano sem peso cultural**
Uma imagem nítida de um escritório específico pode alienar. Uma imagem desfocada de pessoas a trabalhar, em contexto angolano, cria pertença sem impor um ambiente concreto. O visitante projecta a sua própria realidade.

---

## Filosofia de Imagens — Regras Editoriais

### O que fotografar / seleccionar
- Pessoas reais, angolanas, em contextos profissionais
- Ambientes de trabalho: reuniões, ecrãs com dashboards, análise de dados
- Momentos de decisão e colaboração — não poses estáticas
- Diversidade de género e geração (reflecte o mercado angolano real)

### O que evitar absolutamente
- Stock photos genéricas de pessoas brancas em escritórios americanos
- Imagens de servidores, cabos de rede ou hardware — clichés tecnológicos
- Poses de marketing forçadas (pessoas a apontar para ecrãs com sorriso exagerado)
- Qualquer imagem que não passe no teste: *"Esta pessoa poderia ser cliente da Entredados em Luanda?"*

### Tratamento técnico das imagens
```
Blur:           filter: blur(3px) a blur(8px) conforme a secção
Overlay:        background: #030F0F com opacity 0.55 a 0.75
Escala:         object-fit: cover em container com aspect-ratio definido
Posição:        object-position: center (ajustar por imagem)
Transição:      as imagens de hero fazem unblur suave ao carregar (500ms)
```

---

## ESTRUTURA COMPLETA DA PÁGINA

---

## SECÇÃO 00 — NAVBAR
**Tipo:** Componente fixo · Fundo `#030F0F` · Altura 72px

### Layout
```
[Logo + Nome]    [Sobre] [Serviços] [Como Funciona] [Contacto]    [Falar com a Equipa →]
←————————————————————————————————————————————————————————————————————————————————————————→
```

### Elementos
| Elemento | Especificação |
|---|---|
| Logo | Ícone SVG + wordmark "Entredados" em verde `#00DF82` |
| Links | Poppins Medium 15px · cor `#8AADA8` · hover `#F1F7F7` |
| CTA | Botão outline verde · Poppins SemiBold 15px |
| Comportamento scroll | Navbar ganha `border-bottom: 1px solid #1C2E2E` após 80px de scroll |

### Imagem
Nenhuma. A navbar é estrutura pura.

---

## SECÇÃO 01 — HERO
**Tipo:** Full-width · Fundo escuro + imagem blur · Altura mínima 100vh

### Propósito
Responder em 3 segundos à pergunta que todo visitante faz ao chegar:
*"O que é isto e serve para mim?"*

A headline afirma. O subtítulo explica. O visual (imagem + dashboard) prova.

### Layout
```
┌─────────────────────────────────────────────────────────────┐
│  [IMAGEM DE FUNDO · BLUR · PESSOAS EM CONTEXTO PROFISSIONAL]│
│  [OVERLAY #030F0F · 65% OPACIDADE]                          │
│                                                             │
│  ┌────────────────────────────┐   ┌─────────────────────┐  │
│  │ EYEBROW                    │   │  DASHBOARD MOCKUP   │  │
│  │ HEADLINE H1                │   │  (card elevado,     │  │
│  │ — palavra "dados" sublinhada│  │   fundo #0A1A1A,    │  │
│  │                            │   │   métricas reais)   │  │
│  │ SUBTÍTULO                  │   │                     │  │
│  │                            │   │  AOA 4.2M ↑18%      │  │
│  │ [CTA PRIMÁRIO →]           │   │  347 clientes ↑12%  │  │
│  │ [Ver como funciona]        │   │  ▃▅▄▇▆█▇            │  │
│  │                            │   │                     │  │
│  │ Sem compromisso. 24h.      │   └─────────────────────┘  │
│  └────────────────────────────┘                             │
└─────────────────────────────────────────────────────────────┘
```

### Copy
```
Eyebrow:     ANÁLISE DE DADOS · ANGOLA

H1:          Decisões certas
             começam com dados reais.

Subtítulo:   A Entredados transforma os dados da sua empresa
             em dashboards automatizados, análises de mercado
             e estratégias concretas de crescimento.

CTA 1:       Solicitar uma Análise Gratuita →
CTA 2:       Ver como funciona

Nota:        Sem compromisso. Resposta em menos de 24 horas.
```

### Imagem
```
Tipo:        Fotografia de fundo full-width
Conteúdo:    Pessoa(s) angolana(s) em ambiente profissional —
             reunião, análise de ecrã, contexto de liderança
Blur:        filter: blur(4px)
Overlay:     #030F0F · opacity 0.65
Animação:    Ao carregar a página, a imagem faz unblur suave
             de blur(8px) → blur(4px) em 600ms ease-out
             Efeito: a página "acorda" com o visitante
```

### Lógica de design
O dashboard mockup à direita tem função dupla: ancora visualmente o lado direito (evita o hero parecer vazio) e mostra o produto em uso, com números reais angolanos (AOA). O visitante vê imediatamente o que vai receber.

---

## SECÇÃO 02 — SOCIAL PROOF
**Tipo:** Barra horizontal · Fundo `#0A1A1A` · Sem título

### Propósito
Credibilidade imediata, sem discurso. Os números falam sem que ninguém os apresente.

### Layout
```
┌─────────────────────────────────────────────────────┐
│                                                     │
│   +50                    +200               3 Anos  │
│   Empresas           Dashboards           No Mercado│
│   Acompanhadas          Criados            Angolano │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### Animação
Os números fazem count-up (de 0 ao valor final) quando entram no viewport pela primeira vez. Duração: 1200ms ease-out. Triggado por IntersectionObserver.

### Imagem
Nenhuma. A força desta secção vem da contenção — só números.

---

## SECÇÃO 03 — O PROBLEMA
**Tipo:** Fundo `#030F0F` · Conteúdo centrado · Imagem lateral

### Propósito
Antes de apresentar a solução, o visitante tem de se rever no problema. Esta secção fala sobre a dor — não sobre a Entredados. Quem se reconhecer nos três blocos já está meio convencido.

### Layout
```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  EYEBROW                                                    │
│  HEADLINE H2                                                │
│  Parágrafo de introdução                                    │
│                                                             │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────────┐  │
│  │ 01           │  │ 02           │  │ 03               │  │
│  │ Título       │  │ Título       │  │ Título           │  │
│  │ Descrição    │  │ Descrição    │  │ Descrição        │  │
│  └──────────────┘  └──────────────┘  └──────────────────┘  │
│                                                             │
│              "Existe uma forma melhor de operar. →"         │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Copy
```
Eyebrow:     O CUSTO DA INCERTEZA

H2:          A maioria das empresas angolanas toma decisões
             sem saber o que os seus dados dizem.

Parágrafo:   Sem análise estruturada, os recursos da sua empresa
             vão para estratégias que não funcionam. O mercado
             muda, a concorrência avança — e a resposta chega tarde.

Card 01:     Decisões baseadas em intuição
             Sem dados organizados, cada escolha estratégica
             é uma aposta. O risco aumenta. O crescimento estagna.

Card 02:     Concorrência sem visibilidade
             Não saber o que os seus concorrentes fazem — e como
             o consumidor responde — é uma desvantagem competitiva
             que se acumula todos os dias.

Card 03:     Relatórios que ninguém usa
             Os dados existem, mas estão dispersos e sem contexto.
             Relatórios manuais consomem tempo e raramente chegam
             à pessoa certa, na hora certa.

Frase ponte: Existe uma forma melhor de operar. →
```

### Imagem
```
Tipo:        Imagem de fundo subtil na secção inteira
Conteúdo:    Ambiente de escritório angolano, reunião,
             ou pessoa a olhar para ecrã com expressão
             de incerteza / concentração
Blur:        filter: blur(6px)
Overlay:     #030F0F · opacity 0.82
Nota:        O blur é mais forte aqui porque o texto é mais
             denso — a imagem é presença, não distracção
```

---

## SECÇÃO 04 — SERVIÇOS / A SOLUÇÃO
**Tipo:** Fundo `#030F0F` · Grid 2x2 · Imagem de destaque

### Propósito
Mostrar concretamente o que a Entredados faz. Não features — benefícios. Cada serviço termina com uma frase de impacto curta que resume o valor em 5 palavras.

### Layout
```
┌──────────────────────────────────────────────────────────────────┐
│                                                                  │
│  EYEBROW                                                         │
│  HEADLINE H2                         ┌────────────────────────┐  │
│  Subtítulo                           │  IMAGEM · BLUR         │  │
│                                      │  Pessoa a trabalhar    │  │
│  ┌──────────────┐  ┌──────────────┐  │  com dados / ecrã      │  │
│  │▌ Serviço 01  │  │▌ Serviço 02  │  │  Overlay 70%           │  │
│  │  Título      │  │  Título      │  └────────────────────────┘  │
│  │  Descrição   │  │  Descrição   │                              │
│  │  Benefício   │  │  Benefício   │                              │
│  └──────────────┘  └──────────────┘                              │
│  ┌──────────────┐  ┌──────────────┐                              │
│  │▌ Serviço 03  │  │▌ Serviço 04  │                              │
│  │  Título      │  │  Título      │                              │
│  │  Descrição   │  │  Descrição   │                              │
│  │  Benefício   │  │  Benefício   │                              │
│  └──────────────┘  └──────────────┘                              │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### Copy
```
Eyebrow:     O QUE FAZEMOS

H2:          Análise de dados que a sua
             equipa consegue usar amanhã.

Subtítulo:   A Entredados não é só uma consultora. Somos um
             parceiro de transformação digital — entregamos
             soluções, formamos a sua equipa e construímos
             uma cultura de decisão orientada por dados.

Serviço 01:  Análise de Dados e Desenvolvimento
             Recolhemos, organizamos e interpretamos os dados
             da sua empresa para revelar padrões ocultos e
             oportunidades reais de crescimento.
             → O que era opaco torna-se claro.

Serviço 02:  Dashboards Automatizados
             Painéis de controlo inteligentes, personalizados
             para o seu negócio e actualizados em tempo real —
             sem trabalho manual, sem atrasos.
             → Sem relatórios. Sem atrasos.

Serviço 03:  Inteligência Competitiva
             Analisamos o comportamento do consumidor e os
             movimentos da concorrência para que a sua empresa
             antecipe decisões estratégicas.
             → Menos surpresas. Mais antecipação.

Serviço 04:  Decisões em Tempo Real
             Estruturamos os seus dados para que qualquer
             decisão estratégica tenha base factual — rápida,
             documentada e acessível a toda a liderança.
             → Da dúvida à decisão, em minutos.
```

### Imagem
```
Tipo:        Imagem lateral (lado direito, altura total dos cards)
Conteúdo:    Pessoa angolana a trabalhar num ecrã com dados
             visíveis, ou equipa em reunião de análise
Blur:        filter: blur(3px)
Overlay:     #030F0F · opacity 0.70
Nota:        Esta imagem tem menos blur que o hero — o visitante
             já está mais dentro da página, a conexão pode
             ser mais directa
```

---

## SECÇÃO 05 — DIFERENCIAL
**Tipo:** Fundo `#0A1A1A` · Layout split · Imagem com presença forte

### Propósito
Responder à objecção silenciosa: *"Mas porque a Entredados e não outra?"*
O argumento central é o contexto angolano — algo que nenhuma consultora internacional pode copiar.

### Layout
```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│  ┌──────────────────────────┐  ┌──────────────────────┐  │
│  │  IMAGEM · BLUR           │  │  EYEBROW             │  │
│  │  Pessoa angolana,        │  │  H2                  │  │
│  │  contexto local,         │  │  Parágrafo           │  │
│  │  expressão de confiança  │  │                      │  │
│  │  Blur: 3px               │  │  ▌ Pilar 01          │  │
│  │  Overlay: 60%            │  │    Título            │  │
│  │                          │  │    Descrição         │  │
│  │                          │  │                      │  │
│  │                          │  │  ▌ Pilar 02          │  │
│  │                          │  │    Título            │  │
│  │                          │  │    Descrição         │  │
│  │                          │  │                      │  │
│  │                          │  │  ▌ Pilar 03          │  │
│  │                          │  │    Título            │  │
│  └──────────────────────────┘  └──────────────────────┘  │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### Copy
```
Eyebrow:     POR QUE A ENTREDADOS

H2:          Feito para Angola.
             Construído para durar.

Parágrafo:   Não entregamos relatórios genéricos. Trabalhamos
             com a realidade do mercado angolano — os seus
             desafios, os seus dados, o seu contexto.

Pilar 01:    Educação + Tecnologia
             Capacitamos as pessoas enquanto entregamos
             soluções. O conhecimento fica na sua organização —
             não apenas os relatórios.

Pilar 02:    Contexto Local
             Entendemos o mercado angolano. As nossas análises
             refletem a realidade onde a sua empresa opera.

Pilar 03:    Parceria Contínua
             Não desaparecemos após a entrega. Acompanhamos
             a sua evolução e estamos presentes quando
             os dados mudam.
```

### Imagem
```
Tipo:        Imagem de metade da secção (lado esquerdo)
Conteúdo:    Pessoa angolana com expressão de confiança
             e domínio — pode ser o próprio fundador/equipa
             da Entredados, se disponível
Blur:        filter: blur(3px)
Overlay:     #0A1A1A · opacity 0.60
Nota:        Esta é a imagem com menos blur da página inteira.
             O visitante está no meio da jornada — a conexão
             humana pode ser mais directa aqui.
             Se a Entredados tiver foto da equipa real,
             USAR AQUI. Nada cria mais confiança.
```

---

## SECÇÃO 06 — PROCESSO
**Tipo:** Fundo `#030F0F` · 4 etapas horizontais · Sem imagem

### Propósito
Eliminar o medo do "como funciona". Muitos visitantes chegam interessados mas receosos do processo. Esta secção torna o caminho previsível e tranquilizador.

### Layout
```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│  EYEBROW                                                 │
│  HEADLINE H2                                             │
│  Subtítulo                                               │
│                                                          │
│  01 ————————— 02 ————————— 03 ————————— 04              │
│  Diagnóstico  Estruturação  Análise e    Acompanha-      │
│               ·            Visualização  mento           │
│  Descrição    Descrição    Descrição    Descrição        │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### Copy
```
Eyebrow:     O PROCESSO

H2:          Da recolha ao insight,
             em quatro etapas.

Subtítulo:   Um processo claro, sem surpresas, adaptado à
             realidade da sua empresa. Sabe exactamente
             o que esperar em cada fase.

Etapa 01:    Diagnóstico
             Analisamos os dados que já existem na sua empresa,
             identificamos lacunas e mapeamos as oportunidades
             que podem ser trabalhadas imediatamente.

Etapa 02:    Estruturação
             Organizamos as fontes de dados, criamos pipelines
             e preparamos o ambiente técnico para análise
             contínua e segura.

Etapa 03:    Análise e Visualização
             Desenvolvemos dashboards e relatórios que tornam
             os dados compreensíveis para toda a equipa —
             da liderança à operação.

Etapa 04:    Acompanhamento
             Monitorizamos os resultados, ajustamos as métricas
             e formamos a equipa para usar os dados
             de forma cada vez mais autónoma.
```

### Imagem
Nenhuma. O processo beneficia de clareza máxima — qualquer imagem seria distracção. O espaço em branco é o design.

---

## SECÇÃO 07 — PARA QUEM
**Tipo:** Fundo `#0A1A1A` · Grid 2 cards · Imagens dentro dos cards

### Propósito
Confirmação final de identidade. O visitante lê e pensa: *"Sim, isto é para mim."*

### Layout
```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│  EYEBROW                                                 │
│  HEADLINE H2                                             │
│                                                          │
│  ┌────────────────────────────┐  ┌──────────────────┐   │
│  │ [IMAGEM BLUR · TOPO CARD]  │  │[IMAGEM BLUR TOPO]│   │
│  │                            │  │                  │   │
│  │  TAG: Empresas             │  │ TAG: Pesquisa    │   │
│  │  Título H3                 │  │ Título H3        │   │
│  │  Descrição                 │  │ Descrição        │   │
│  └────────────────────────────┘  └──────────────────┘   │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### Copy
```
Eyebrow:     PARA QUEM

H2:          Para quem quer crescer com
             informação, não com suposições.

Card 01:
  Tag:       EMPRESAS E ORGANIZAÇÕES
  Título:    Empresas e Organizações
  Descrição: Que precisam de visibilidade operacional,
             análise de mercado e dashboards que apoiem
             decisões de gestão no dia a dia — sem depender
             de relatórios manuais ou de equipa técnica interna.

Card 02:
  Tag:       PESQUISADORES E ANALISTAS
  Título:    Pesquisadores e Analistas
  Descrição: Que trabalham com dados em Angola e precisam
             de ferramentas, metodologia e parceria técnica
             para desenvolver projectos de maior impacto
             e rigor analítico.
```

### Imagem
```
Card 01:
  Tipo:      Imagem no topo do card (banner horizontal, 200px altura)
  Conteúdo:  Reunião de gestão, sala de conselho, decisão empresarial
  Blur:      filter: blur(3px)
  Overlay:   #0A1A1A · opacity 0.65

Card 02:
  Tipo:      Imagem no topo do card (banner horizontal, 200px altura)
  Conteúdo:  Pessoa a analisar dados, ecrã com gráficos,
             ambiente académico ou de pesquisa
  Blur:      filter: blur(3px)
  Overlay:   #0A1A1A · opacity 0.65
```

---

## SECÇÃO 08 — CTA FINAL
**Tipo:** Fundo `#00DF82` (verde total) · Split layout

### Propósito
A conversão. Tudo o que veio antes construiu confiança — esta secção pede a acção. O verde total é o único momento da página onde o fundo inverte completamente. É impossível não notar.

### Layout
```
┌──────────────────────────────────────────────────────────┐
│ [FUNDO VERDE #00DF82]                                    │
│                                                          │
│  ┌───────────────────────────┐  ┌──────────────────────┐ │
│  │  H2 (texto escuro)        │  │  Campo: Nome         │ │
│  │  Subtítulo                │  │  Campo: Email        │ │
│  │                           │  │  Campo: Empresa      │ │
│  │  [CTA Escuro →]           │  │  [Botão escuro →]    │ │
│  │                           │  │  Nota de privacidade │ │
│  └───────────────────────────┘  └──────────────────────┘ │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### Copy
```
H2:          Os seus dados já têm respostas.
             Falta interpretá-los.

Subtítulo:   Agende uma conversa com a nossa equipa.
             Sem compromisso, sem termos técnicos —
             só foco no seu negócio.

CTA lateral: Falar com a Entredados →

Formulário:
  Campo 1:   O seu nome  [placeholder: Ex: João Silva]
  Campo 2:   Email profissional  [placeholder: Ex: joao@empresa.ao]
  Campo 3:   Nome da empresa  [placeholder: Ex: Empresa Lda.]
  Botão:     Falar com a Entredados →
  Nota:      Os seus dados são confidenciais e nunca
             partilhados com terceiros.

Sucesso:     Recebemos o seu contacto.
             A nossa equipa vai entrar em contacto
             em menos de 24 horas.

Erro:        Algo correu mal. Tente novamente ou contacte-nos
             em info@entredados.ao
```

### Imagem
Nenhuma. O verde absoluto é o elemento de impacto. Qualquer imagem competiria com ele e diluiria o momento de conversão.

---

## SECÇÃO 09 — FOOTER
**Tipo:** Fundo `#030F0F` · Grid 4 colunas · Sem imagem

### Propósito
Encerramento institucional. Dá a informação que o visitante precisa para confiar: contacto, redes sociais, links legais. Simples e completo.

### Layout
```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│  [Logo]                  Serviços   Empresa   Contacto  │
│  "O mundo tem a          · Análise  · Sobre   · email   │
│   idade dos dados."      · Dashb.   · Missão  · Insta   │
│                          · Intelig. · Equipa  · LinkedIn │
│                          · Decisões · Parcei. · YouTube  │
│                                                          │
│  ────────────────────────────────────────────────────── │
│  © 2025 Entredados. Angola.   Privacidade · Termos      │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### Copy
```
Tagline:     "O mundo tem a idade dos dados."

Col. Serviços:
  Título:    Serviços
  Links:     Análise de Dados
             Dashboards Automatizados
             Inteligência Competitiva
             Decisões em Tempo Real

Col. Empresa:
  Título:    Empresa
  Links:     Sobre Nós · Missão · Equipa · Parceiros

Col. Contacto:
  Título:    Contacto
  Info:      info@entredados.ao
  Redes:     Instagram · LinkedIn · YouTube

Copyright:   © 2025 Entredados. Todos os direitos reservados. Angola.
Legais:      Política de Privacidade · Termos de Uso
```

---

## MAPA DE IMAGENS — RESUMO

| Secção | Imagem? | Tipo | Blur | Overlay |
|---|---|---|---|---|
| Navbar | Não | — | — | — |
| Hero | **Sim** | Fundo full-width | 4px | #030F0F · 65% |
| Social Proof | Não | — | — | — |
| Problema | **Sim** | Fundo subtil | 6px | #030F0F · 82% |
| Serviços | **Sim** | Lateral direita | 3px | #030F0F · 70% |
| Diferencial | **Sim** | Metade esquerda | 3px | #0A1A1A · 60% |
| Processo | Não | — | — | — |
| Para Quem | **Sim** | Topo dos 2 cards | 3px | #0A1A1A · 65% |
| CTA Final | Não | — | — | — |
| Footer | Não | — | — | — |

**Total: 5 imagens** em 4 secções distintas.
Cada uma com propósito específico. Nenhuma decorativa.

---

## RITMO DE LEITURA DA PÁGINA

```
ENTRADA         Hero → impacto emocional imediato (imagem + headline)
                ↓
CONFIANÇA       Social Proof → números que validam
                ↓
IDENTIFICAÇÃO   Problema → "isto sou eu"
                ↓
SOLUÇÃO         Serviços → "isto é o que preciso"
                ↓
DIFERENCIAÇÃO   Por que Entredados → "isto é para Angola, para mim"
                ↓
PROCESSO        Como funciona → "não é complicado"
                ↓
CONFIRMAÇÃO     Para Quem → "sim, sou eu"
                ↓
ACÇÃO           CTA Final → "vou experimentar"
                ↓
SAÍDA           Footer → informação institucional
```

Este ritmo segue a jornada psicológica de um decisor angolano que nunca ouviu falar de análise de dados estruturada: da curiosidade à confiança, da confiança à decisão.

---

## NOTAS TÉCNICAS PARA IMPLEMENTAÇÃO

### CSS das imagens blur
```css
.section-image {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  filter: blur(4px);
  transform: scale(1.05); /* evita bordas brancas do blur */
  z-index: 0;
}

.section-overlay {
  position: absolute;
  inset: 0;
  background: #030F0F;
  opacity: 0.65;
  z-index: 1;
}

.section-content {
  position: relative;
  z-index: 2;
}
```

### Animação de entrada do Hero
```css
@keyframes unblur {
  from { filter: blur(8px); opacity: 0.7; }
  to   { filter: blur(4px); opacity: 1;   }
}

.hero-image {
  animation: unblur 600ms ease-out forwards;
}
```

### Performance
- Todas as imagens em formato WebP
- Atributo `loading="lazy"` em todas excepto o hero
- Hero image com `fetchpriority="high"` e preload no `<head>`
- Tamanho máximo por imagem: 300KB após compressão

---

*Entredados · Estrutura da Landing Page · v1.0 · Junho 2025*
*Documento a usar como referência durante desenvolvimento e revisão.*

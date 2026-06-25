# Entredados — Design System
> Versão 1.0 · Junho 2025 · Coletivos Digital

---

## 1. Fundação da Marca

### Missão Visual
A Entredados deve ser percebida como **inovadora, confiável e técnica** — sem ser fria ou inacessível. O sistema visual é construído sobre três princípios:

- **Clareza** — Cada elemento tem um propósito. Nada é decoração.
- **Precisão** — Espaçamentos, tamanhos e pesos são sistemáticos e nunca arbitrários.
- **Autoridade** — A marca fala com líderes de negócio. O visual deve transmitir domínio técnico sem arrogância.

### Slogan
> *"O mundo tem a idade dos dados."*

---

## 2. Paleta de Cores

### 2.1 Cores Primárias

| Nome | Hex | Uso |
|---|---|---|
| Verde Entredados | `#00DF82` | CTAs primários, accent, destaques, links |
| Preto Profundo | `#030F0F` | Fundo principal (dark sections), texto sobre claro |
| Branco Frio | `#F1F7F7` | Texto sobre fundos escuros, fundo de seções claras |

### 2.2 Cores Secundárias (sistema expandido)

| Nome | Hex | Uso |
|---|---|---|
| Superfície Elevada | `#0A1A1A` | Cards, navbars, superfícies sobre o fundo principal |
| Borda Sutil | `#1C2E2E` | Bordas de cards, divisores, separadores |
| Verde Hover | `#00C974` | Estado hover do verde primário |
| Verde Pressed | `#00B366` | Estado active/pressed do verde primário |
| Verde Muted | `#00DF8220` | Backgrounds de badges, highlights suaves (20% opacidade) |
| Texto Secundário | `#8AADA8` | Labels, legendas, texto de suporte sobre fundo escuro |
| Texto Terciário | `#4D6B66` | Placeholders, metadados, texto desativado sobre escuro |

### 2.3 Cores Semânticas

| Estado | Hex | Uso |
|---|---|---|
| Sucesso | `#00DF82` | Confirmações, validações positivas (usa o verde marca) |
| Erro | `#FF4D4D` | Erros de formulário, alertas críticos |
| Aviso | `#F5A623` | Alertas não críticos, avisos de atenção |
| Info | `#3B9EE8` | Mensagens informativas neutras |

### 2.4 Estados de Cor — Regras Completas

#### Verde Primário `#00DF82`
```
Default:   #00DF82
Hover:     #00C974  (escurece 8%)
Active:    #00B366  (escurece 15%)
Focus:     #00DF82 + outline 2px offset 2px
Disabled:  #00DF8240 (40% opacidade) + cursor: not-allowed
```

#### Superfície / Cards `#0A1A1A`
```
Default:   #0A1A1A
Hover:     #0F2020
Active:    #142626
Focus:     border 1px #00DF82
Disabled:  opacidade 50%
```

#### Fundo Principal `#030F0F`
```
Não tem estado de hover — é estrutural.
```

---

## 3. Tipografia

### 3.1 Famílias

| Papel | Família | Fonte Google |
|---|---|---|
| Display / Headings | **Oxanium** | `fonts.googleapis.com/css2?family=Oxanium` |
| Body / UI / Labels | **Poppins** | `fonts.googleapis.com/css2?family=Poppins` |

**Regra de uso:** Oxanium nunca aparece em tamanhos abaixo de 16px. Poppins é o padrão para tudo que seja corrido, longo ou de interface.

---

### 3.2 Escala Tipográfica

| Token | Família | Peso | Tamanho | Line-height | Uso |
|---|---|---|---|---|---|
| `--text-display` | Oxanium | 700 | 72px | 1.05 | H1 do Hero |
| `--text-h1` | Oxanium | 700 | 56px | 1.1 | Títulos de seção principais |
| `--text-h2` | Oxanium | 600 | 40px | 1.15 | Sub-seções, títulos de cards grandes |
| `--text-h3` | Oxanium | 600 | 28px | 1.2 | Títulos de cards, itens de lista |
| `--text-h4` | Oxanium | 500 | 20px | 1.3 | Labels de seção (eyebrows em maiúsculas) |
| `--text-body-lg` | Poppins | 400 | 18px | 1.7 | Parágrafos de hero e introdução |
| `--text-body` | Poppins | 400 | 16px | 1.7 | Corpo de texto padrão |
| `--text-body-sm` | Poppins | 400 | 14px | 1.6 | Texto de suporte, descrições de cards |
| `--text-label` | Poppins | 600 | 12px | 1.4 | Eyebrows, badges, tags — sempre UPPERCASE |
| `--text-caption` | Poppins | 400 | 12px | 1.5 | Metadados, timestamps, rodapés |
| `--text-cta` | Poppins | 600 | 16px | 1 | Texto de botões |
| `--text-nav` | Poppins | 500 | 15px | 1 | Links de navegação |
| `--text-number` | Oxanium | 700 | 48px | 1 | Números de destaque (social proof) |

### 3.3 Regras Tipográficas

- **Eyebrows** (labels de seção): sempre `--text-label` em UPPERCASE, cor `#00DF82`, letter-spacing `0.12em`
- **Headings sobre fundo escuro**: cor `#F1F7F7`
- **Headings sobre fundo claro**: cor `#030F0F`
- **Parágrafos sobre fundo escuro**: cor `#8AADA8` (secundário) ou `#F1F7F7` (principal)
- **Nunca** usar Oxanium em pesos abaixo de 500
- **Nunca** usar italic em Oxanium
- **Máximo** de 70 caracteres por linha em parágrafos (legibilidade)

---

## 4. Espaçamento

### 4.1 Escala Base (múltiplos de 4px)

| Token | Valor | Uso típico |
|---|---|---|
| `--space-1` | 4px | Gap mínimo entre elementos inline |
| `--space-2` | 8px | Gap interno de badges, padding de tags |
| `--space-3` | 12px | Gap entre ícone e texto |
| `--space-4` | 16px | Padding interno de elementos pequenos |
| `--space-5` | 20px | Gap entre elementos de formulário |
| `--space-6` | 24px | Padding interno de cards pequenos |
| `--space-8` | 32px | Gap entre cards, padding de cards médios |
| `--space-10` | 40px | Gap entre grupos de elementos |
| `--space-12` | 48px | Padding de seções internas |
| `--space-16` | 64px | Espaço entre seções na página |
| `--space-20` | 80px | Padding vertical de seções (mobile) |
| `--space-24` | 96px | Padding vertical de seções (desktop) |
| `--space-32` | 128px | Padding vertical de seções de destaque (Hero, CTA final) |

### 4.2 Layout Grid

```
Desktop (≥1280px):
  max-width:      1200px
  colunas:        12
  gutter:         24px
  padding lateral: 40px

Tablet (768px–1279px):
  max-width:      100%
  colunas:        8
  gutter:         20px
  padding lateral: 32px

Mobile (< 768px):
  colunas:        4
  gutter:         16px
  padding lateral: 20px
```

### 4.3 Secções da Página — Espaçamento Vertical

```
Padding-top/bottom de cada section:
  Hero:           128px top / 96px bottom
  Padrão:         96px top / 96px bottom
  CTA Final:      128px top / 128px bottom
  Footer:         64px top / 48px bottom

Espaço entre eyebrow → heading:    16px
Espaço entre heading → subtítulo:  20px
Espaço entre subtítulo → conteúdo: 48px
Espaço entre heading → cards:      48px
```

---

## 5. Bordas e Raios

### 5.1 Border Radius

| Token | Valor | Uso |
|---|---|---|
| `--radius-sm` | 4px | Tags, badges, inputs inline |
| `--radius-md` | 8px | Botões, inputs, elementos de formulário |
| `--radius-lg` | 12px | Cards pequenos e médios |
| `--radius-xl` | 16px | Cards grandes, modais |
| `--radius-full` | 9999px | Pills, avatares, indicadores circulares |

### 5.2 Bordas

```
Card padrão:        1px solid #1C2E2E
Card hover:         1px solid #00DF8260
Card focus/active:  1px solid #00DF82
Input padrão:       1px solid #1C2E2E
Input hover:        1px solid #4D6B66
Input focus:        1px solid #00DF82 + outline none
Divisor de seção:   1px solid #1C2E2E (horizontal, opacity 60%)
Linha accent hero:  2px solid #00DF82 (underline da palavra-chave)
```

---

## 6. Componentes — Estados e Especificações

### 6.1 Botão Primário (CTA Principal)

```
Background:      #00DF82
Texto:           #030F0F (Poppins SemiBold 16px)
Padding:         14px 28px
Border-radius:   8px
Border:          none

Estados:
  Hover:         background #00C974 · transform scale(1.01) · transition 150ms ease
  Active:        background #00B366 · scale(0.99)
  Focus:         outline 2px #00DF82 · outline-offset 3px
  Disabled:      background #00DF8240 · color #03 0F0F80 · cursor not-allowed
  Loading:       spinner branco à esquerda · texto "Aguarde..."
```

### 6.2 Botão Secundário (Outline)

```
Background:      transparent
Texto:           #00DF82 (Poppins SemiBold 16px)
Border:          1px solid #00DF82
Padding:         13px 27px
Border-radius:   8px

Estados:
  Hover:         background #00DF8215 · border-color #00C974
  Active:        background #00DF8225 · border-color #00B366
  Focus:         outline 2px #00DF82 · outline-offset 3px
  Disabled:      border-color #1C2E2E · color #4D6B66 · cursor not-allowed
```

### 6.3 Botão Ghost (Navbar / Links)

```
Background:      transparent
Texto:           #8AADA8 (Poppins Medium 15px)
Border:          none
Padding:         8px 0

Estados:
  Hover:         color #F1F7F7 · transition 150ms
  Active:        color #00DF82
  Focus:         underline 1px #00DF82
  Disabled:      color #4D6B66 · cursor not-allowed
```

### 6.4 Input de Texto / Email

```
Background:      #0A1A1A
Texto:           #F1F7F7 (Poppins Regular 16px)
Placeholder:     #4D6B66
Border:          1px solid #1C2E2E
Border-radius:   8px
Padding:         12px 16px
Height:          48px

Estados:
  Hover:         border-color #4D6B66
  Focus:         border-color #00DF82 · outline none · box-shadow 0 0 0 3px #00DF8220
  Erro:          border-color #FF4D4D · box-shadow 0 0 0 3px #FF4D4D20
  Sucesso:       border-color #00DF82
  Disabled:      background #030F0F · color #4D6B66 · cursor not-allowed
```

### 6.5 Card de Serviço

```
Background:      #0A1A1A
Border:          1px solid #1C2E2E
Border-radius:   12px
Padding:         32px

Estados:
  Default:       border #1C2E2E
  Hover:         border #00DF8260 · background #0F2020 · transform translateY(-2px)
                 transition: all 200ms ease
  Active:        border #00DF82 · background #0A1A1A
  Focus:         outline 2px #00DF82 offset 2px
```

### 6.6 Badge / Tag

```
Background:      #00DF8220
Texto:           #00DF82 (Poppins SemiBold 12px UPPERCASE)
Padding:         4px 10px
Border-radius:   4px
Letter-spacing:  0.08em

Variante Neutra:
  Background:    #1C2E2E
  Texto:         #8AADA8
```

### 6.7 Link Inline

```
Cor:             #00DF82
Decoration:      none
Font-weight:     500

Estados:
  Hover:         color #00C974 · underline 1px
  Active:        color #00B366
  Visited:       color #8AADA8
  Focus:         outline 2px #00DF82 offset 2px
```

---

## 7. Iconografia

### 7.1 Biblioteca

**Nenhum ícone decorativo** na landing page. A Entredados comunica por texto e estrutura — não por ilustrações ou ícones infantis.

Quando necessário (formulários, navegação, feedback de estado), usar **Phosphor Icons** (versão Regular / Bold):

```
CDN: https://unpkg.com/phosphor-icons
```

**Por que Phosphor?** Traços limpos, sem serifa, geometry consistente — alinha com o estilo técnico do Oxanium e a precisão do Poppins.

### 7.2 Tamanhos Permitidos

| Contexto | Tamanho | Peso de traço |
|---|---|---|
| Navegação / inline | 20px | Regular |
| Cards / botões | 24px | Regular |
| Seções de destaque | 32px | Bold |
| Nunca acima de | 40px | — |

### 7.3 Ícones Aprovados por Contexto

```
Navegação:
  Menu:            List
  Fechar:          X
  Voltar:          ArrowLeft
  Externo:         ArrowSquareOut

Formulários:
  Email:           EnvelopeSimple
  Empresa:         Buildings
  Utilizador:      User
  Sucesso:         CheckCircle
  Erro:            WarningCircle
  Loading:         CircleNotch (animated)

Serviços (se usados):
  Análise:         ChartBar
  Dashboard:       SquaresFour
  Inteligência:    MagnifyingGlass
  Decisão:         Scales
  Parceria:        Handshake

Social:
  Instagram:       InstagramLogo
  LinkedIn:        LinkedinLogo
  YouTube:         YoutubeLogo
```

### 7.4 Regras de Uso

- Ícones usam **sempre** a cor `#00DF82` quando são de destaque
- Ícones de UI (inputs, erros) usam a cor do estado correspondente
- **Nunca** misturar ícones de bibliotecas diferentes
- **Nunca** usar ícones preenchidos (filled) junto com ícones de contorno (outline) na mesma seção
- Todo ícone standalone tem `aria-label` ou é `aria-hidden="true"` se decorativo

---

## 8. Animações e Transições

### 8.1 Filosofia

Animações servem o conteúdo — nunca o decoram. O padrão é **discreto e rápido**. A única animação de destaque é o scroll reveal das seções.

### 8.2 Tokens de Transição

```css
--transition-fast:    150ms ease          /* hover de botões, links */
--transition-base:    200ms ease          /* cards, inputs */
--transition-slow:    300ms ease          /* aparecimento de seções */
--transition-reveal:  600ms cubic-bezier(0.16, 1, 0.3, 1)  /* scroll reveal */
```

### 8.3 Padrões de Animação

```
Botão hover:
  transform: scale(1.01)
  transition: --transition-fast

Card hover:
  transform: translateY(-2px)
  border-color: #00DF8260
  transition: --transition-base

Scroll reveal (seções):
  from: opacity 0 · translateY 24px
  to:   opacity 1 · translateY 0
  duration: --transition-reveal
  stagger entre elementos: 80ms

Underline do hero (assinatura):
  width: 0 → 100%
  duration: 800ms ease
  delay: 400ms (após carga)

Número contador (social proof):
  count-up de 0 ao valor final
  duration: 1200ms ease-out
  trigger: intersection observer
```

### 8.4 Regras

- **Respeitar `prefers-reduced-motion`** — todas as animações desativam quando o utilizador preferir
- Nenhuma animação acima de 600ms no caminho crítico de leitura
- Sem auto-play de qualquer coisa que pisque ou pulse em loop

---

## 9. Sombras e Profundidade

A Entredados usa profundidade através de **bordas e cor de fundo**, não sombras. A exceção única é o foco de acessibilidade.

```
Profundidade 0 (base):    fundo #030F0F
Profundidade 1 (elevado): fundo #0A1A1A · borda 1px #1C2E2E
Profundidade 2 (flutuante): fundo #0F2020 · borda 1px #00DF8260

Sombra de foco (única sombra permitida):
  box-shadow: 0 0 0 3px #00DF8220
```

---

## 10. Acessibilidade

### 10.1 Contraste Mínimo

| Combinação | Rácio | Nível |
|---|---|---|
| `#F1F7F7` sobre `#030F0F` | 19.5:1 | AAA |
| `#00DF82` sobre `#030F0F` | 8.2:1 | AAA |
| `#030F0F` sobre `#00DF82` | 8.2:1 | AAA |
| `#8AADA8` sobre `#030F0F` | 5.1:1 | AA |
| `#4D6B66` sobre `#030F0F` | 3.1:1 | AA Large only |

### 10.2 Regras

- Todos os botões têm `:focus-visible` visível
- Inputs têm `label` associado (não só placeholder)
- Imagens decorativas têm `alt=""`
- Links têm texto descritivo (não "clique aqui")
- Ordem do DOM corresponde à ordem visual
- Tamanho mínimo de área clicável: 44×44px

---

## 11. Estrutura de Tokens CSS

```css
:root {
  /* Cores */
  --color-brand:           #00DF82;
  --color-brand-hover:     #00C974;
  --color-brand-active:    #00B366;
  --color-brand-muted:     #00DF8220;

  --color-bg-base:         #030F0F;
  --color-bg-surface:      #0A1A1A;
  --color-bg-elevated:     #0F2020;

  --color-border-subtle:   #1C2E2E;
  --color-border-muted:    #4D6B66;
  --color-border-accent:   #00DF82;

  --color-text-primary:    #F1F7F7;
  --color-text-secondary:  #8AADA8;
  --color-text-tertiary:   #4D6B66;
  --color-text-inverse:    #030F0F;

  --color-error:           #FF4D4D;
  --color-warning:         #F5A623;
  --color-info:            #3B9EE8;

  /* Tipografia */
  --font-display:          'Oxanium', sans-serif;
  --font-body:             'Poppins', sans-serif;

  --text-display:          700 72px/1.05 var(--font-display);
  --text-h1:               700 56px/1.1 var(--font-display);
  --text-h2:               600 40px/1.15 var(--font-display);
  --text-h3:               600 28px/1.2 var(--font-display);
  --text-h4:               500 20px/1.3 var(--font-display);
  --text-body-lg:          400 18px/1.7 var(--font-body);
  --text-body:             400 16px/1.7 var(--font-body);
  --text-body-sm:          400 14px/1.6 var(--font-body);
  --text-label:            600 12px/1.4 var(--font-body);
  --text-cta:              600 16px/1 var(--font-body);
  --text-nav:              500 15px/1 var(--font-body);
  --text-number:           700 48px/1 var(--font-display);

  /* Espaçamento */
  --space-1:  4px;
  --space-2:  8px;
  --space-3:  12px;
  --space-4:  16px;
  --space-5:  20px;
  --space-6:  24px;
  --space-8:  32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  --space-24: 96px;
  --space-32: 128px;

  /* Bordas */
  --radius-sm:   4px;
  --radius-md:   8px;
  --radius-lg:   12px;
  --radius-xl:   16px;
  --radius-full: 9999px;

  /* Transições */
  --transition-fast:   150ms ease;
  --transition-base:   200ms ease;
  --transition-slow:   300ms ease;
  --transition-reveal: 600ms cubic-bezier(0.16, 1, 0.3, 1);

  /* Layout */
  --max-width:        1200px;
  --gutter:           24px;
  --section-padding:  96px;
  --hero-padding:     128px;
}
```

---

## 12. Checklist de Implementação

### Antes de codar
- [ ] Importar Oxanium e Poppins do Google Fonts
- [ ] Definir todas as CSS custom properties no `:root`
- [ ] Configurar reset CSS (box-sizing, margin 0, font padrão)
- [ ] Configurar grid de 12 colunas com max-width 1200px

### Durante o desenvolvimento
- [ ] Nunca usar hex hardcoded — sempre tokens
- [ ] Todos os estados interativos implementados (hover, focus, active, disabled)
- [ ] Testar contraste com ferramenta (WebAIM ou similiar)
- [ ] `prefers-reduced-motion` implementado
- [ ] Scroll reveal com IntersectionObserver

### Antes de entregar
- [ ] Testar em Chrome, Firefox, Safari
- [ ] Testar mobile (320px, 375px, 428px)
- [ ] Testar tablet (768px, 1024px)
- [ ] Validar acessibilidade com Lighthouse (meta: ≥ 90)
- [ ] Verificar que nenhum texto tem contraste abaixo de 4.5:1

---

*Entredados Design System · Mantido por Coletivos Digital · v1.0*

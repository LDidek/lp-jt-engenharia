# Layout - JT Engenharia

**Aesthetic Identity:** Industrial Precision — O site deve transmitir a solidez de uma planta industrial com a sofisticacao de uma apresentacao que convence diretores e gerentes de compras. Confianca construida com estrutura visual imponente, numeros concretos e transparencia.

---

## 1. CORE DESIGN SYSTEM

### Palette
- **Primary:** #1A1A1A — Carbono — Background principal, headers, containers escuros. O preto industrial que ancora tudo.
- **Accent:** #F5C518 — Voltagem — Derivado do amarelo do raio no logo. CTAs, highlights, icones, hover states, detalhes energeticos.
- **Accent Dark:** #D4A813 — Voltagem Profundo — Hover state dos CTAs, gradientes com o accent.
- **Surface Light:** #F7F7F5 — Concreto Claro — Background de secoes alternadas, contraste com secoes escuras.
- **Surface Medium:** #E8E6E1 — Cimento — Backgrounds de cards claros, separadores.
- **Text Primary:** #FFFFFF — Texto sobre fundos escuros.
- **Text Dark:** #1A1A1A — Texto sobre fundos claros.
- **Text Muted:** #6B6B6B — Textos secundarios, labels, captions.
- **Border:** rgba(245, 197, 24, 0.15) — Bordas sutis com tom dourado para separadores em fundo escuro.
- **Success:** #2E7D32 — Badges de certificacao, checks de conformidade.

### Typography
- **Headings:** "Space Grotesk" 700 — Geometrica com personalidade industrial, tracking -0.02em em titulos grandes. Peso e presenca sem ser generica.
- **Body:** "Inter Tight" 400 — Legibilidade maxima, line-height 1.6, otimizada para paragrafos tecnicos.
- **Drama/Emphasis:** "Space Grotesk" 800 — Contadores numericos e headlines hero em peso extra-bold para impacto.
- **Labels/Badges:** "Inter Tight" 600 — Uppercase, letter-spacing 0.08em, 12-13px. Para tags como "NR-10", "13 ANOS", "GARANTIA 5 ANOS".

### Visual Texture
- **Noise overlay:** SVG turbulence com opacity 0.03 sobre secoes escuras (#1A1A1A) para textura industrial sutil.
- **Pattern overlay opcional:** Grid de linhas finas (1px, rgba(255,255,255,0.03)) a cada 80px sobre hero — remete a blueprint/projeto tecnico.
- **Border-radius system:** 0px para containers e secoes (industrial, arestas vivas). 4px para botoes e inputs. 8px para cards e elementos flutuantes.
- **Shadow system:** Cards claros: `0 1px 3px rgba(0,0,0,0.08), 0 4px 12px rgba(0,0,0,0.04)`. Cards flutuantes/hover: `0 8px 32px rgba(0,0,0,0.12)`. Glow accent: `0 0 20px rgba(245, 197, 24, 0.15)` em hover de CTAs.
- **Spacing base:** 8px grid. Secoes: 100px padding vertical desktop / 60px mobile. Container max-width: 1200px. Padding lateral: 80px desktop / 24px mobile.
- **Divisores entre secoes:** Transicao hard de cor (escuro→claro→escuro), sem wave/diagonal. Clean e industrial.

---

## 2. COMPONENT ARCHITECTURE & BEHAVIOR

### A. NAVBAR ("The Control Panel")
**Visuals:** Background transparente no topo, transiciona para #1A1A1A com backdrop-filter: blur(12px) e opacity 0.95 apos 80px de scroll. Borda inferior: 1px solid rgba(245, 197, 24, 0.1) quando sticky. Altura: 72px.
**Layout:** Logo JT Engenharia a esquerda (imagem, max-height 40px, usar `/.netlify/images?url=/images/logo.jpg&w=200&q=80`). Links de navegacao ao centro (Servicos, Diferenciais, Sobre Nos, Depoimentos, FAQ) em Inter Tight 500 14px uppercase letter-spacing 0.05em. CTA "Solicitar Orcamento" a direita.
**CTA Navbar:** Background #F5C518, texto #1A1A1A, font Inter Tight 600 14px uppercase. Padding: 12px 28px. Border-radius: 4px. Hover: background #D4A813, scale 1.02, box-shadow 0 0 20px rgba(245,197,24,0.25), transition 0.3s cubic-bezier(0.34, 1.56, 0.64, 1).
**Morphing Logic:** Scroll > 80px: background solid #1A1A1A/0.95 + blur. CSS transition: background 0.3s ease, backdrop-filter 0.3s ease.
**Responsividade:** Mobile (< 768px): Logo a esquerda, hamburger icon a direita (3 linhas #F5C518, 24px). Menu fullscreen overlay: background #1A1A1A, links centralizados, Space Grotesk 700 32px, stagger fade-in 0.1s entre links. CTA no bottom do menu mobile com width 100%. Hamburger anima para X com transition 0.3s.

---

### B. HERO SECTION ("The Powerhouse")
**Visuals:** Altura 100vh (min-height: 600px). Background: imagem `Tecnico + painel.jpeg` (tecnico trabalhando em painel eletrico com fios organizados, mostra competencia tecnica) via `/.netlify/images?url=/images/tecnico-painel.jpg&w=1920&q=80`. Overlay: linear-gradient(135deg, rgba(26,26,26,0.92) 0%, rgba(26,26,26,0.75) 50%, rgba(26,26,26,0.6) 100%). Noise overlay SVG turbulence opacity 0.03. background-size: cover, background-position: center.
**Layout:** Conteudo posicionado no terco central-esquerdo. Grid de 12 colunas, conteudo ocupa colunas 1-7. Padding: 0 80px. Alinhamento vertical: center. O conteudo nao deve ficar colado no topo — deve estar verticalmente centralizado.
**Badge:** Antes da headline: inline-block com background rgba(245,197,24,0.12), border 1px solid rgba(245,197,24,0.3), padding 6px 16px, border-radius 4px. Texto: "13 ANOS DE EXPERIENCIA NO SETOR INDUSTRIAL" em Inter Tight 600, 11px, uppercase, letter-spacing 0.1em, cor #F5C518.
**Typography:** Headline em Space Grotesk 700, 56px desktop / 36px mobile, line-height 1.1, color #FFFFFF. A palavra "Alta Performance" deve ter color #F5C518 para destaque. Subheadline em Inter Tight 400, 18px desktop / 16px mobile, line-height 1.6, color rgba(255,255,255,0.75), max-width 560px. Margin-top: 20px apos headline.
**CTA:** Botao primario: background #F5C518, texto #1A1A1A, Space Grotesk 700 16px uppercase letter-spacing 0.05em. Padding: 18px 40px. Border-radius: 4px. Hover: background #D4A813, scale 1.03, box-shadow 0 4px 24px rgba(245,197,24,0.3). Transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1). Margin-top: 32px.
**Elemento secundario:** Abaixo do CTA, margin-top 24px. Linha com icone SVG de telefone (#F5C518, 16px) + texto "Ou ligue: (XX) XXXXX-XXXX" em Inter Tight 400, 14px, rgba(255,255,255,0.5).
**Scroll indicator:** Na base da viewport, centralizado. Chevron duplo animado para baixo, opacity 0.4, animacao up-down 2s infinite ease-in-out (translateY 0 → 8px → 0).
**Animation:** NENHUMA animacao de ENTRADA no hero. O conteudo aparece instantaneamente. Pos-carregamento: o badge pode ter um sutil pulse glow no border (keyframe: border-color oscila entre rgba(245,197,24,0.3) e rgba(245,197,24,0.5), duration 3s, infinite).
**Responsividade:** Mobile (375px): Headline 36px, subheadline 15px, padding 0 24px. CTA full-width. Badge font 10px. Conteudo centralizado (text-align center). Min-height: 100svh.

---

### C. SERVICOS ("The Blueprint")
**Visuals:** Background #F7F7F5 (claro). Padding: 100px 80px desktop / 60px 24px mobile.
**Layout:** Arquetipo: Split Assimetrico (55/45). Lado esquerdo: bloco de texto com titulo + descricao + lista de servicos. Lado direito: imagem `Engenheiro + Transformador.jpeg` com clip-path: polygon(8% 0, 100% 0, 100% 100%, 0 100%) — corte diagonal na borda esquerda para dinamismo. Imagem via `/.netlify/images?url=/images/engenheiro-transformador.jpg&w=800&q=80`. Gap entre colunas: 60px.
**Overline:** Texto "NOSSOS SERVICOS" em Inter Tight 600, 12px, uppercase, letter-spacing 0.12em, cor #F5C518. Margin-bottom 16px. Com uma linha horizontal de 40px, 2px, #F5C518 antes do texto (ou a esquerda).
**Title:** "O Que a JT Engenharia Faz Por Voce" em Space Grotesk 700, 40px desktop / 28px mobile, color #1A1A1A, line-height 1.15.
**Body:** Paragrafo descritivo em Inter Tight 400, 16px, color #6B6B6B, line-height 1.7, max-width 520px. Margin-top: 16px.
**Lista de servicos:** Margin-top 32px. Cada item: flex row, gap 12px. Icone: circulo 32px background rgba(245,197,24,0.1), icone SVG interno de 16px cor #F5C518 (bolt/lightning para eletrico, building para comercial, clipboard-check para projetos, users para equipe). Texto: Inter Tight 500, 15px, #1A1A1A. Spacing entre itens: 16px. Nao usar bullets tradicionais.
**CTA:** Igual ao padrao. Margin-top 32px.
**Animation:** AOS fade-up no bloco de texto, delay 0. Imagem: AOS fade-left, delay 0.2s. `data-aos="fade-up"` e `data-aos="fade-left"`.
**Responsividade:** Mobile: Stack vertical, imagem primeiro (order: -1), full-width, clip-path removido. Texto abaixo. Imagem max-height: 300px, object-fit: cover.

---

### D. DIFERENCIAIS ("The Precision Dashboard")
**Visuals:** Background #1A1A1A (escuro). Noise overlay SVG opacity 0.03. Padding: 100px 80px desktop / 60px 24px mobile.
**Layout:** Arquetipo: Bento Box assimetrico. Grid com 3 colunas desktop, gap 20px. 7 cards, distribuidos assim:
  - Row 1: 2 cards (span 1 col cada) + 1 card grande (span 1 col, rowspan 2 — card do APP)
  - Row 2: 2 cards (span 1 col cada) + card do APP continua
  - Row 3: 2 cards (span 1 col cada) + vazio ou card adicional

**Overline:** "POR QUE NOS ESCOLHER" em Inter Tight 600, 12px, uppercase, letter-spacing 0.12em, cor #F5C518. Centralizado. Linha decorativa: 40px, 2px, #F5C518 acima do texto.
**Title:** "Por Que Escolher a JT Engenharia" em Space Grotesk 700, 40px desktop / 28px mobile, #FFFFFF, text-align center. Margin-top 16px. Margin-bottom 60px.

**Cards Padrao (6 cards):**
- Background: #242424. Border: 1px solid rgba(255,255,255,0.06). Border-radius: 8px. Padding: 32px.
- Icone topo: 48px, circulo background rgba(245,197,24,0.1), icone SVG 24px #F5C518. Icones distintos para cada: shield-check (garantia), smartphone (app), award (qualificacao), target (foco), eye (transparencia), map-pin (presenca), clock (experiencia).
- Titulo: Space Grotesk 700, 20px, #FFFFFF, margin-top 20px.
- Descricao: Inter Tight 400, 14px, rgba(255,255,255,0.6), line-height 1.6, margin-top 12px.
- Hover: border-color rgba(245,197,24,0.2), transform translateY(-4px), box-shadow 0 8px 32px rgba(0,0,0,0.3). Transition: all 0.3s ease.

**Card Especial — APP Diario de Obra (maior):**
- Span 1 coluna, rowspan 2 (altura dupla). Background: linear-gradient(180deg, #2A2520 0%, #242424 100%) — leve tom quente.
- Border: 1px solid rgba(245,197,24,0.15).
- Topo: titulo "APP com Diario da Obra em Tempo Real" em Space Grotesk 700, 22px, #FFFFFF. Descricao em Inter Tight 400, 14px, rgba(255,255,255,0.6).
- Centro: Mockup de smartphone centralizado. Usar a imagem `Foto 3.jpg` (screenshot do relatorio diario do app) dentro de um frame CSS de celular. Frame: border-radius 24px, border 3px solid #3A3A3A, background #000, padding 8px, width 200px. Notch: pseudo-element centralizado no topo, 60px x 6px, border-radius 3px, #3A3A3A. A imagem do app ocupa o "screen" inteiro com border-radius 16px e overflow hidden.
- Abaixo do mockup: 3 mini-stats em row: "287 Relatorios", "2.710 Fotos", "6 Obras" — Inter Tight 600, 14px, #F5C518 para numero, Inter Tight 400, 11px, rgba(255,255,255,0.5) para label. Esses dados vem dos screenshots do app.

**Animation:** Cards com AOS fade-up, stagger 0.1s entre eles. Mockup do app: AOS fade-up com delay 0.3s.
**Responsividade:** Mobile: Grid single-column. Todos os cards em stack. Card do APP nao tem rowspan, aparece normalmente. Mockup do phone menor (width 160px).

---

### E. NUMEROS ("The Voltage Counter")
**Visuals:** Background #F7F7F5. Padding: 80px desktop / 60px mobile.
**Layout:** Arquetipo: Single Focus + Counter Animation. Flex row com 4 contadores, justify-content: space-around. Max-width: 1000px, centralizado. Separador vertical entre contadores: 1px solid #E8E6E1, height 60px.
**Contadores:**
1. "13+" — "Anos de Experiencia"
2. "3" — "Regioes de Atuacao"
3. "5" — "Anos de Garantia"
4. "100%" — "Foco em Execucao"

**Typography:** Numero: Space Grotesk 800, 56px desktop / 40px mobile, #1A1A1A. Label: Inter Tight 400, 14px, #6B6B6B, uppercase, letter-spacing 0.05em. Margin-top 8px.
**Animation:** Counter animation com JS vanilla: numeros contam de 0 ate o valor final. Duration 2s, ease-out. Trigger: IntersectionObserver quando a secao entra no viewport (threshold 0.5). Cada contador tem delay staggered de 0.15s.
**Responsividade:** Mobile: Grid 2x2, gap 32px. Separadores verticais removidos. Separador horizontal entre rows: 1px solid #E8E6E1.

---

### F. QUEM SOMOS ("The Founders")
**Visuals:** Background #1A1A1A. Padding: 100px 80px desktop / 60px 24px mobile.
**Layout:** Arquetipo: Split Vertical com Overlap. Grid 2 colunas (50/50), gap 60px. Lado esquerdo: imagem `Sócios JT Engenharia.jpeg` — foto dos 3 socios/equipe em frente ao logo da empresa. Via `/.netlify/images?url=/images/socios.jpg&w=800&q=80`. Border-radius 8px. Lado direito: bloco de texto.
**Overline:** "QUEM SOMOS" em Inter Tight 600, 12px, uppercase, letter-spacing 0.12em, cor #F5C518.
**Title:** "Especialistas em Execucao Eletrica Industrial" em Space Grotesk 700, 36px desktop / 26px mobile, #FFFFFF, line-height 1.2.
**Body:** Texto da copy em Inter Tight 400, 16px, rgba(255,255,255,0.7), line-height 1.7. Margin-top 20px.
**Destaques inline:** Os 3 pilares mencionados na copy ("Mao de obra altamente qualificada", "Processos transparentes", "Compromisso real com prazos e seguranca") como lista com icone check-circle #F5C518 + texto Inter Tight 500, 15px, #FFFFFF. Margin-top 28px. Spacing entre itens: 12px.
**Imagem decorativa:** Corner badge no topo-esquerdo da imagem: bloco absolute, background #F5C518, padding 12px 20px, texto "DESDE 2012" em Inter Tight 700, 12px, uppercase, #1A1A1A.
**Animation:** Imagem: AOS fade-right. Texto: AOS fade-left. Delay 0.2s entre eles.
**Responsividade:** Mobile: Stack vertical. Imagem primeiro, full-width, max-height 350px, object-fit cover. Texto abaixo. Badge "DESDE 2012" mantido.

---

### G. DEPOIMENTOS ("The Voltage Reports")
**Visuals:** Background #F7F7F5. Padding: 100px 80px desktop / 60px 24px mobile.
**Layout:** Arquetipo: Carousel Standard. Overline + titulo centralizado no topo. 3 depoimentos em carrossel (1 visivel por vez em desktop, navigation arrows laterais).
**Overline:** "DEPOIMENTOS" em Inter Tight 600, 12px, uppercase, letter-spacing 0.12em, cor #F5C518. Centralizado.
**Title:** "O Que Dizem Sobre Nos" em Space Grotesk 700, 40px desktop / 28px mobile, #1A1A1A, text-align center. Margin-bottom 60px.
**Card de depoimento:**
- Max-width: 720px, centralizado. Background: #FFFFFF. Border-radius: 8px. Padding: 48px. Box-shadow: 0 1px 3px rgba(0,0,0,0.06), 0 4px 16px rgba(0,0,0,0.04).
- Aspas decorativas: Icone SVG de aspas duplas, 40px, color rgba(245,197,24,0.2), posicao absolute topo-esquerdo dentro do card (top 20px, left 24px).
- Texto do depoimento: Inter Tight 400, 17px, #1A1A1A, line-height 1.7, font-style italic.
- Rodape do card: Margin-top 28px. Borda top: 1px solid #E8E6E1. Padding-top 20px. Nome/cargo: Inter Tight 600, 14px, #1A1A1A. Empresa/cidade: Inter Tight 400, 13px, #6B6B6B.
- Estrelas: 5 estrelas SVG preenchidas, 16px, #F5C518, acima do texto do depoimento.
**Navigation:** Setas laterais fora do card. Circulos 48px, border 1px solid #E8E6E1, background transparent. Icone chevron, 20px, #1A1A1A. Hover: background #F5C518, border-color #F5C518, icone #1A1A1A. Transition 0.3s ease.
**Dots:** 3 dots abaixo do card, 8px, gap 8px. Ativo: background #F5C518, width 24px, border-radius 4px. Inativo: background #D4D4D4, border-radius 50%.
**Animation:** Card: AOS fade-up. Transicao entre slides: CSS transform translateX com transition 0.5s ease.
**Responsividade:** Mobile: Setas removidas, apenas dots + swipe gesture nativo. Card padding 28px. Font do depoimento 15px.

---

### H. FAQ ("The Technical Manual")
**Visuals:** Background #1A1A1A. Padding: 100px 80px desktop / 60px 24px mobile.
**Layout:** Arquetipo: Accordion. Grid 2 colunas: esquerda com titulo + descricao, direita com accordion. Gap: 80px.
**Lado esquerdo:**
- Overline: "FAQ" em Inter Tight 600, 12px, uppercase, letter-spacing 0.12em, cor #F5C518.
- Title: "Duvidas Frequentes" em Space Grotesk 700, 36px desktop / 28px mobile, #FFFFFF, line-height 1.2.
- Subtexto: "Nao encontrou sua resposta? Entre em contato conosco." em Inter Tight 400, 15px, rgba(255,255,255,0.6). Margin-top 16px.
- CTA secundario: "Falar com a Equipe" — border 1px solid #F5C518, background transparent, texto #F5C518, Inter Tight 600 14px uppercase. Padding: 14px 28px. Hover: background #F5C518, texto #1A1A1A. Transition 0.3s ease. Margin-top 24px.
**Lado direito — Accordion:**
- Cada item: border-bottom 1px solid rgba(255,255,255,0.08). Padding: 24px 0.
- Pergunta: Inter Tight 600, 16px, #FFFFFF. Display flex, justify-content space-between, align-items center. Icone plus/minus a direita, 20px, #F5C518. Cursor pointer.
- Resposta: Inter Tight 400, 15px, rgba(255,255,255,0.6), line-height 1.7. Max-height: 0 → auto com transition 0.4s ease. Padding-top 16px quando aberto.
- Hover na pergunta: color #F5C518, transition 0.2s.
- Primeiro item aberto por default.
**Animation:** Lado esquerdo: AOS fade-right. Accordion: AOS fade-left, delay 0.2s.
**Responsividade:** Mobile: Stack vertical. Titulo em cima, accordion abaixo. Full-width.

---

### I. CTA FINAL + FORMULARIO ("The Circuit Closer")
**Visuals:** Background: imagem `Tecnico dando assessoria.jpeg` (equipe em obra) via `/.netlify/images?url=/images/tecnico-assessoria.jpg&w=1920&q=80`. Overlay: linear-gradient(135deg, rgba(26,26,26,0.93) 0%, rgba(26,26,26,0.85) 100%). Padding: 100px 80px desktop / 60px 24px mobile.
**Layout:** Arquetipo: Split Vertical (55/45). Grid 2 colunas. Esquerda: bloco persuasivo. Direita: formulario.
**Lado esquerdo:**
- Overline: "SOLICITE UM ORCAMENTO" em Inter Tight 600, 12px, uppercase, letter-spacing 0.12em, cor #F5C518.
- Title: "Precisa de Profissionais para Instalacoes Eletricas?" em Space Grotesk 700, 40px desktop / 28px mobile, #FFFFFF, line-height 1.15.
- Body: Texto da copy em Inter Tight 400, 17px, rgba(255,255,255,0.75), line-height 1.7. Margin-top 20px.
- Slogan: "Voce traz o projeto, nos executamos com excelencia!" em Space Grotesk 700, 20px, #F5C518, font-style italic. Margin-top 28px.
- Trust badges: Margin-top 32px. Row de 3 badges inline: icone SVG 20px + texto 13px. "Garantia 5 Anos" / "Equipe Certificada" / "13 Anos de Mercado". Cor: rgba(255,255,255,0.5). Icones: #F5C518.
**Lado direito — Formulario:**
- Background: #242424. Border: 1px solid rgba(255,255,255,0.08). Border-radius: 8px. Padding: 40px.
- Titulo do form: "Preencha para solicitar seu orcamento" em Space Grotesk 600, 18px, #FFFFFF. Margin-bottom 28px.
- Campos: input com background #1A1A1A, border 1px solid rgba(255,255,255,0.1), border-radius 4px, padding 14px 16px, color #FFFFFF, font Inter Tight 400 15px. Placeholder: rgba(255,255,255,0.35). Focus: border-color #F5C518, box-shadow 0 0 0 3px rgba(245,197,24,0.1). Transition 0.2s.
- Campos: Nome, Telefone (com intl-tel-input), Email, Select "Tenho interesse em..." (Instalacoes Industriais, Instalacoes Comerciais, Outro).
- Spacing entre campos: 16px.
- Botao submit: Full-width. Background #F5C518, texto #1A1A1A, Space Grotesk 700 16px uppercase. Padding: 16px. Border-radius: 4px. Hover: background #D4A813, box-shadow 0 4px 20px rgba(245,197,24,0.3). Margin-top 24px.
- Nota de privacidade: "Seus dados estao protegidos conosco." em Inter Tight 400, 12px, rgba(255,255,255,0.35). Margin-top 12px. Icone lock 12px inline.
**Animation:** Lado esquerdo: AOS fade-right. Formulario: AOS fade-up, delay 0.2s.
**Responsividade:** Mobile: Stack vertical. Texto primeiro, formulario abaixo. Formulario full-width.

---

### J. FOOTER ("The Ground Wire")
**Visuals:** Background #111111. Border-top: 1px solid rgba(245,197,24,0.1). Padding: 60px 80px 32px desktop / 40px 24px 24px mobile.
**Layout:** Grid 3 colunas: Logo + descricao | Links rapidos | Contato. Gap: 40px.
**Coluna 1:** Logo (max-height 36px, filter brightness para funcionar em fundo escuro se necessario). Abaixo: descricao curta em Inter Tight 400, 14px, rgba(255,255,255,0.5), max-width 280px. Margin-top 16px.
**Coluna 2:** Titulo "Links Rapidos" em Inter Tight 600, 14px, #FFFFFF, uppercase, letter-spacing 0.05em. Links: Servicos, Diferenciais, Sobre, FAQ. Inter Tight 400, 14px, rgba(255,255,255,0.5). Hover: color #F5C518, translateX(4px). Spacing: 12px.
**Coluna 3:** Titulo "Contato" em Inter Tight 600, 14px, #FFFFFF, uppercase. Telefone e email em Inter Tight 400, 14px, rgba(255,255,255,0.5). Icones SVG inline 16px #F5C518 antes de cada. Redes sociais: icones Instagram/LinkedIn/WhatsApp, 20px, rgba(255,255,255,0.4). Hover: color #F5C518, scale 1.1.
**Barra inferior:** Margin-top 40px. Border-top: 1px solid rgba(255,255,255,0.06). Padding-top: 24px. "2026 JT Engenharia. Todos os direitos reservados." Inter Tight 400, 13px, rgba(255,255,255,0.3). Centralizado.
**Responsividade:** Mobile: Stack vertical. Colunas empilhadas com gap 32px. Barra inferior centralizada.

---

## 3. TECHNICAL REQUIREMENTS

### Bibliotecas CDN
- **Google Fonts:** Space Grotesk (700, 800) + Inter Tight (400, 500, 600, 700)
  `https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@700;800&family=Inter+Tight:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap`
- **AOS (Animate On Scroll):** Para animacoes de entrada no scroll
  CSS: `https://unpkg.com/aos@2.3.1/dist/aos.css`
  JS: `https://unpkg.com/aos@2.3.1/dist/aos.js`
  Init: `AOS.init({ duration: 800, once: true, offset: 80, disableMutationObserver: true })`

### Imagens (mapeamento de arquivo → uso)
| Arquivo Original | Renomear para | Uso na Pagina |
|---|---|---|
| Logomarca - JT Engenharia.jpeg | logo.jpg | Navbar + Footer |
| Tecnico + painel.jpeg | tecnico-painel.jpg | Hero background |
| Engenheiro + Transformador.jpeg | engenheiro-transformador.jpg | Secao Servicos |
| Sócios JT Engenharia.jpeg | socios.jpg | Secao Quem Somos |
| Tecnico dando assessoria.jpeg | tecnico-assessoria.jpg | Secao CTA Final |
| Engenheiro ajustando painel - JT Engenharia.jpeg | engenheiro-painel.jpg | Reserva (uso opcional) |
| Frota JT Engenharia.jpeg | frota.jpg | Reserva (uso opcional na secao Presenca Regional) |
| Foto 1.jpg | app-relatorios.jpg | Card APP - Opcional |
| Foto 2.jpg | app-visao-geral.jpg | Card APP - Opcional |
| Foto 3.jpg | app-relatorio-diario.jpg | Card APP - Mockup principal |
| Foto 4.jpg | app-fotos-obra.jpg | Card APP - Opcional |

Todas as imagens devem estar na pasta `/images/` na raiz do projeto e serem servidas via `/.netlify/images?url=/images/[nome]&w=[largura]&q=80`.

### Micro-interacoes globais
- **Links de navegacao:** Underline animado da esquerda para direita usando pseudo-element ::after. Width 0 → 100% no hover. Height 2px, background #F5C518. Transition: width 0.3s ease.
- **Botoes primarios (CTA amarelo):** Hover: scale 1.03, background #D4A813, box-shadow glow. Active: scale 0.98. Transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1).
- **Botoes secundarios (outline):** Hover: background fills, color inverts. Transition 0.3s ease.
- **Cards:** Hover: translateY(-4px), shadow deepens, border-color brightens. Transition 0.3s ease.
- **Icones SVG:** todos inline, 24px default, stroke-width 1.5 ou 2. Estilo lucide/feather icons.
- **Smooth scroll:** CSS `html { scroll-behavior: smooth; }`. Nao usar Lenis (simplicidade).
- **Focus states:** Todos os elementos interativos: outline 2px solid #F5C518, outline-offset 2px. Acessibilidade garantida.

### Diretiva de qualidade
- Zero gaps de cor entre secoes (alternar #1A1A1A ↔ #F7F7F5 de forma limpa)
- Todos os textos devem ter contraste WCAG AA minimo
- Todas as imagens devem ter alt text descritivo
- Performance: imagens via CDN Netlify com w= e q= adequados. Lazy loading em imagens abaixo do fold.
- Nenhum scroll horizontal acidental em mobile
- O hero deve carregar instantaneamente — imagem hero com fetchpriority="high"

---

## 4. DETALHES DE CRAFT

### Transicoes entre secoes
- Alternancia ritmica: ESCURO (Hero) → CLARO (Servicos) → ESCURO (Diferenciais) → CLARO (Numeros) → ESCURO (Quem Somos) → CLARO (Depoimentos) → ESCURO (FAQ) → ESCURO com imagem (CTA Final) → ESCURO (Footer). Isso cria um ritmo visual de "respiracao" e separa contextos sem precisar de divisores decorativos.

### Micro-interacoes unicas
- **Badge do hero:** Pulsing border sutil (border-color oscila entre opacidade 0.3 e 0.5 com animation de 3s infinite).
- **Counter da secao Numeros:** Numeros contam de 0 ao valor com easing deceleration. O "+" aparece com um sutil scale bounce (1 → 1.2 → 1) ao finalizar a contagem.
- **Card do APP:** O mockup do celular tem uma sombra que simula profundidade: `0 20px 60px rgba(0,0,0,0.4), 0 8px 20px rgba(0,0,0,0.3)`. No hover do card, o celular faz um sutil translateY(-4px) adicional, como se flutuasse.
- **FAQ accordion:** O icone +/- rotaciona 45 graus ao abrir (o + vira x). Transition: transform 0.3s ease.

### Consistencia visual com a marca
- O amarelo #F5C518 e usado APENAS como accent — nunca como background de secoes inteiras. Isso mantem o impacto.
- O preto #1A1A1A nao e pure black (#000), tem um tom ligeiramente quente que reduz fadiga visual.
- A paleta reflete diretamente o logo: preto solido + raio amarelo. Tudo na pagina amplifica essa identidade sem inventar cores novas.

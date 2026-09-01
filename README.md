# Apresentação Anotável — Deck Premium + Prancheta

> Apresentação HTML única que combina **slides premium** com **anotação em tempo real** (lápis, caneta, marca-texto, borracha). Feita pra gravar vídeo, dar aula ou apresentar riscando por cima do conteúdo.

## ✨ Features

- **🖊️ Anotação calibrada** — lápis, caneta grossa, marca-texto e borracha (apaga de verdade). O traço acompanha o cursor 1:1, sem deslocamento.
- **🎨 Pincel completo** — tamanho ajustável (slider) + 8 cores premium + preview do traço.
- **📑 Modo Slides** — 9 páginas 16:9 em moldura padronizada, navegação por setas, contador.
- **🖼️ Modo Livre** — prancheta em branco pra desenhar à vontade.
- **💾 Salvar PNG** — exporta o slide + anotações (html2canvas).
- **↩ Desfazer** — Ctrl+Z ou botão.
- **⌨️ Atalhos** — `← →` navega · `N` anotação · `H` esconde UI · `P/M/L/E` ferramentas · `S` salva.
- **📊 Figuras visuais** — funis em SVG, gráfico de barras, cards com emojis didáticos (menos texto, mais metáfora visual).
- **✅ Validação visual** — cada slide é validado (overflow, contraste, alinhamento) antes de entregar.

## 🚀 Como usar

1. Abra o `index.html` no navegador (ou arraste pra aba).
2. Navegue os slides com as setas do teclado.
3. Clique na caneta ✏️ e risque por cima pra explicar.
4. `S` salva o slide como PNG. `H` esconde a interface pra gravar limpo.

## 🎨 Personalizar conteúdo

Os slides são montados no JavaScript do `index.html` (função `addSlide`). Cada slide é um bloco HTML:

```js
addSlide(`
  <span class="kicker">Sua seção</span>
  <h1>Seu <span class="g">título</span></h1>
  <p class="sub">Sua mensagem.</p>
`);
```

Troque os textos, emojis e cards. As cores usam variáveis CSS no topo (`--green`, `--blue`, `--ink`...).

## 🤖 Como pedir pro robô montar

Veja `COMO-PEDIR-SLIDES-VISUAIS.md` — o fluxo pra gerar apresentações com metáforas visuais (SVGs desenhados, imagens geradas por IA, cards com ícones).

## 📁 Estrutura

```
apresentacao-anotavel/
├── index.html                    # o deck completo (HTML único, zero dependências locais)
└── COMO-PEDIR-SLIDES-VISUAIS.md  # receita do robô pra slides visuais
```

> O `index.html` é 100% autocontido (só usa uma imagem de QR via CDN no slide final). Funciona offline pra tudo o resto.

## 🧪 Testado

- Anotação calibrada (traço no ponto exato do cursor)
- Borracha com `destination-out` (apaga, não pinta)
- Desfazer / Salvar PNG / navegação
- Validação visual dos slides (zero overflow)

---

*Feito com o método DesignMAX. Premium, anotável, pronto pra gravar.*

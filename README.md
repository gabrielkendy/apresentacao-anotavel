# Apresentação Anotável — Deck Premium + Prancheta

> Apresentação HTML única que combina **slides premium** com **anotação em tempo real** (lápis, caneta, marca-texto, borracha). Feita pra gravar vídeo, dar aula ou apresentar riscando por cima do conteúdo.

## ✨ Features

- **🖊️ Anotação calibrada** — lápis, caneta grossa, marca-texto e borracha (apaga de verdade). O traço acompanha o cursor 1:1, sem deslocamento.
- **🎨 Pincel completo** — tamanho ajustável (slider) + 8 cores premium + preview do traço.
- **📑 Modo Slides** — páginas 16:9 em moldura padronizada, navegação por setas, contador.
- **🖼️ Modo Livre** — prancheta em branco pra desenhar à vontade.
- **💾 Salvar PNG** — exporta o slide + anotações (html2canvas).
- **↩ Desfazer** — Ctrl+Z ou botão.
- **⌨️ Atalhos** — `← →` navega · `N` anotação · `H` esconde UI · `P/M/L/E` ferramentas · `S` salva · `F` encaixa.
- **📊 Figuras visuais** — SVG inline (gráficos, fluxos), grids de cards (g2/g3/g4/g5), emojis didáticos.

## 🚀 Como usar

1. Abra o `index.html` no navegador (ou https://gabrielkendy.github.io/apresentacao-anotavel/).
2. Navegue os slides com as setas do teclado.
3. Clique na caneta ✏️ e risque por cima pra explicar.
4. `S` salva o slide como PNG. `H` esconde a interface pra gravar limpo.

## 🎨 Como criar UMA NOVA apresentação (3 jeitos)

### 1. Pedir pro robô (recomendado)
Peça: *"Faz uma apresentação sobre [TEMA] no template apresentacao-anotavel"*.
O agente copia o arquivo, troca os slides, monta figuras visuais, valida cada slide visualmente e entrega pronto pra gravar.

### 2. Editar na mão (5 min)
Cada slide é um bloco `addSlide(\`...\`)` no fim do arquivo:

```js
addSlide(`
  <span class="kicker">Sua seção</span>
  <h1>Seu <span class="g">título</span></h1>
  <div class="grid g3">
    <div class="card"><div class="emo">📱</div><b>Pilar 1</b><p>descrição</p></div>
    <div class="card"><div class="emo">✉️</div><b>Pilar 2</b><p>descrição</p></div>
    <div class="card"><div class="emo">📲</div><b>Pilar 3</b><p>descrição</p></div>
  </div>
`);
```

**Classes prontas:**
- `.kicker` — label verde no topo · `h1` com `.g` (verde) `.b` (azul) `.a` (âmbar) `.r` (vermelho)
- `.grid` + `.g2/.g3/.g4/.g5` — colunas de cards
- `.card` com `.emo` (emoji) `<b>` (título) `<p>` (texto)
- `.formula` + `.fcell` — fórmula com células
- `.split` — duas colunas · `.cover` + `.stats` — capa com números
- SVG inline pra gráficos e fluxos

### 3. Copiar de uma apresentação existente
Use a `AULA-07` da Zápia como referência completa (12 slides com cards, SVG, plano, CTA).

## ⌨️ Atalhos

| Tecla | Ação |
|---|---|
| `←` `→` | Navegar slides |
| `N` | Liga/desliga anotação |
| `H` | Esconde a UI (gravação limpa) |
| `P` `M` `L` `E` | Lápis / Caneta / Marca-texto / Borracha |
| `S` | Salvar PNG do slide |
| `F` | Encaixa slide na tela |
| `Ctrl+Z` | Desfazer |

## 📁 Estrutura

```
apresentacao-anotavel/
├── index.html                    # o template completo (HTML único)
└── COMO-PEDIR-SLIDES-VISUAIS.md  # receita do robô pra slides visuais
```

> O `index.html` é 100% autocontido. Funciona offline. Nenhuma dependência de build.

## 🧪 Testado

- Anotação calibrada (traço no ponto exato do cursor)
- Borracha com `destination-out` (apaga, não pinta)
- Desfazer / Salvar PNG / navegação / modo livre
- Validação visual dos slides (zero overflow)

---

*Feito com o método DesignMAX. Premium, anotável, pronto pra gravar.*

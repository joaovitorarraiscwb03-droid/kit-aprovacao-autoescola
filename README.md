# Kit Aprovação Autoescola — Static Export

Landing page estática (HTML puro + Tailwind via CDN). Pronta para subir no GitHub e publicar na Vercel.

## Estrutura
```
.
├── index.html
├── vercel.json
└── assets/
    └── kit-mockup.png
```

## Tracking já incluso
- **Meta Pixel (Facebook Ads):** `1294772135575724` — eventos `PageView` (auto) e `InitiateCheckout` (no clique do botão).
- **Utmify UTMs:** script `cdn.utmify.com.br/scripts/utms/latest.js` com `data-utmify-prevent-xcod-sck` e `data-utmify-prevent-subids` — captura e propaga UTMs para o checkout.
- **Utmify Pixel:** `pixelId = 6a0f9d418dd9aa642c34ce72`.
- **Checkout:** `https://pay.wiapy.com/0xRMHrqGBl` (em todos os CTAs).

## Como publicar na Vercel
1. Crie um repositório no GitHub e suba estes arquivos (`index.html`, `vercel.json`, `assets/`).
2. Em https://vercel.com → **Add New Project** → importe o repositório.
3. Framework Preset: **Other** (deixe campos de build vazios).
4. Deploy. Pronto.

## Como testar localmente
```bash
npx serve .
# ou
python3 -m http.server 8080
```

## Observações
- Página totalmente **mobile-first**: botões grandes, fontes responsivas, sem scroll horizontal, viewport com `viewport-fit=cover`.
- Os scripts da Utmify reescrevem automaticamente os links de checkout com as UTMs capturadas — não é preciso configurar mais nada.
- Para customizar preço/texto, edite `index.html` (busque por `R$19,90` ou pelo texto que quiser trocar).

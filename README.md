# Jorge Resolve — Landing Page

Landing page de conversão da marca **Jorge Resolve**, focada em levar pequenos e
médios empresários ao WhatsApp.

> **Fala com o Jorge que ele resolve.**

## Stack

Site estático, sem build step:

- `index.html` — marcação semântica da LP curta focada no Raio-X Jorge Resolve
- `styles.css` — design system, componentes e responsividade
- `script.js` — interações leves (menu mobile, FAQ, header blur e ano dinâmico)
- `assets/` — foto, favicon e imagem OG
- `_headers`, `_redirects` — configuração da Cloudflare Pages
- `robots.txt`, `sitemap.xml` — SEO

## Rodar localmente

Como é estático, basta abrir o `index.html` no navegador. Para servir via HTTP
(recomendado, evita restrições de file://):

```bash
python3 -m http.server 8080
# acesse http://localhost:8080
```

## Deploy — Cloudflare Pages

### Opção A — pelo painel (Git)

1. Suba o repositório no GitHub/GitLab.
2. No painel da Cloudflare: **Workers & Pages → Create → Pages → Connect to Git**.
3. Selecione o repositório e a branch.
4. **Build settings:**
   - Framework preset: **None**
   - Build command: *(vazio)*
   - Build output directory: **`/`** (raiz)
5. **Save and Deploy.**
6. Em **Custom domains**, conecte `jorgeresolve.com` (e, se quiser, o redirect
   de `falacomojorge.com.br` — ver `_redirects`).

### Opção B — pela CLI (Wrangler)

```bash
npm install -g wrangler
wrangler login
wrangler pages deploy . --project-name=jorge-resolve
```

## Personalização rápida

| O quê | Onde |
|---|---|
| Número de WhatsApp | buscar `554892087242` em `index.html` |
| E-mail / Instagram | rodapé do `index.html` |
| Cores | variáveis `:root` em `styles.css` |
| Textos | seções no `index.html` |

## Hospedagem

Cloudflare Pages (gratuito, CDN global, HTTPS automático).

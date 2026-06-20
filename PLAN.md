# Plano de Execução — Landing Page Jorge Resolve

> **Objetivo:** Construir e publicar a landing page da marca **Jorge Resolve** —
> moderna, azul, responsiva e focada 100% em conversão para WhatsApp.
> **Hospedagem:** Cloudflare Pages (site estático, sem build step).
> **Stack:** HTML semântico + CSS puro + JavaScript vanilla (rápido e leve).
>
> **Regra de execução:** cada passo tem status `todo`, `doing` ou `done`.
> Ao terminar um passo, este arquivo é atualizado e seguimos para o próximo.
> Branch: `feat/jorge-resolve-landing`.

---

## Dados da marca (referência única)

| Campo | Valor |
|---|---|
| Nome | Jorge Resolve |
| Bordão | Fala com o Jorge que ele resolve. |
| WhatsApp | `554892087242` |
| Link WhatsApp | `https://wa.me/554892087242?text=Oi%20Jorge,%20quero%20entender%20como%20voc%C3%AA%20pode%20ajudar%20minha%20empresa%20a%20encontrar%20oportunidades.` |
| E-mail | jorgediasdsg@gmail.com |
| Instagram | @jorgeresolve |
| Localização | Florianópolis, SC |
| Cor principal | `#0B5CFF` |
| Verde WhatsApp | `#25D366` |
| Fonte | Inter (Google Fonts / fallback system) |

---

## Passos de construção

### Fase 0 — Preparação

- **[done] Passo 1 — Branch e limpeza da pasta**
  Criar branch `feat/jorge-resolve-landing`. Remover arquivos do portfólio antigo
  (index.html, styles.css, script.js, README antigo, assets de devicons/banner).
  Preservar `docs/`, `prompt.md` e a foto do Jorge. Reorganizar a foto em `assets/`.

- **[done] Passo 2 — Estrutura base de arquivos**
  Criar esqueleto: `index.html`, `styles.css`, `script.js`, `assets/`,
  `README.md` novo, e arquivos de deploy Cloudflare (`_headers`, `_redirects`).

### Fase 1 — Construção da página

- **[done] Passo 3 — HTML semântico completo**
  Marcar todas as 13 seções do prompt: header, hero, problema, solução,
  como funciona, serviços, oportunidade, por que o Jorge, projetos, CTA
  intermediário, FAQ, CTA final, rodapé. Tags semânticas, SEO e acessibilidade.

- **[done] Passo 4 — Design system (CSS base)**
  Variáveis de cor/espaçamento/tipografia, reset, fonte Inter, gradientes azuis,
  estilos de botões, cards e utilitários.

- **[done] Passo 5 — CSS do header + hero**
  Header fixo com blur, menu, hero com gradiente, painel dashboard flutuante,
  selos de confiança e CTAs.

- **[done] Passo 6 — CSS das seções de conteúdo**
  Cards de dores, blocos de solução, timeline "como funciona", grid de serviços,
  três colunas de oportunidade, cards "por que o Jorge", projetos, CTAs e FAQ.

- **[done] Passo 7 — Responsividade mobile-first + botão flutuante WhatsApp**
  Breakpoints, menu hambúrguer mobile, botão flutuante fixo de WhatsApp com
  animação sutil. Garantir leitura e toque no celular.

- **[done] Passo 8 — JavaScript (interações)**
  Menu mobile, reveal on scroll (IntersectionObserver), acordeão do FAQ,
  blur do header ao rolar, scroll suave e ano dinâmico no rodapé.

- **[done] Passo 9 — Assets, SEO e acessibilidade finais**
  Foto do Jorge otimizada, favicon SVG, imagem OG, meta tags completas,
  `robots.txt`, `sitemap.xml`, contraste e atributos ARIA revisados.

### Fase 2 — Deploy Cloudflare

- **[done] Passo 10 — Configuração Cloudflare Pages**
  `_headers` (cache + segurança), `_redirects`, instruções de deploy no README
  (via dashboard e via Wrangler CLI).

- **[done] Passo 11 — Verificação final e checklist**
  Testado via servidor local (todos os arquivos retornam HTTP 200), links de
  WhatsApp validados, responsividade e SEO conferidos. Commit final feito.

---

## Checklist de qualidade (Passo 11)

- [x] Abre sem erros no navegador (HTTP 200 em todos os arquivos)
- [x] Todos os CTAs levam ao WhatsApp correto (6 pontos de contato)
- [x] Botão flutuante de WhatsApp visível em todas as telas
- [x] 100% responsivo (mobile, tablet, desktop)
- [x] Meta title e description corretos
- [x] Tags semânticas e ARIA
- [x] Contraste adequado
- [x] Animações suaves e leves (respeitam `prefers-reduced-motion`)
- [x] Pronto para deploy no Cloudflare Pages

---

## ✅ Plano concluído

Landing page Jorge Resolve construída e verificada na branch
`feat/jorge-resolve-landing`. Próximo passo manual: conectar o repositório à
Cloudflare Pages (instruções no `README.md`).

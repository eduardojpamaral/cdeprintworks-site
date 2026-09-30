# CDE Print Works — site (cdeprintworks.com)

Site da CDE Print Works: impressão 3D personalizada, feita em Massachusetts, com envio para todo os EUA.

## Endereços

| O quê | Onde |
|---|---|
| Site | https://cdeprintworks.com (também www. e https://cdeprintworks-site.pages.dev) |
| Hospedagem | Cloudflare Pages → projeto `cdeprintworks-site` (publica sozinho a cada commit na branch `main`) |
| Domínio e DNS | Cloudflare → `cdeprintworks.com` |
| Painel para editar | https://app.pagescms.org (login com GitHub) |
| Loja | https://www.etsy.com/shop/CDEPrintWorks |
| Redes | @cdeprintworks no Instagram, TikTok e Facebook |
| E-mail | contact@cdeprintworks.com |

## Estrutura dos arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | Página única do site (visual, textos fixos, seções). Monta os cards de produto a partir do JSON |
| `data/products.json` | Cards de produto: `title`, `photo`, `description`, `details` (lista), `price`, `badge`, `button_text`, `link`, `published` |
| `data/settings.json` | Links gerais: `etsy_url`, `facebook_url`, `messenger_url`, `instagram_url`, `tiktok_url`, `email` |
| `images/` | `logo.png`, `logo-full.png` (logo com slogan), `favicon.png`, fotos dos produtos |
| `.pages.yml` | Configuração do painel Pages CMS (campos de Products e Site settings) |

## Como editar

**Pelo painel (mais fácil):** app.pagescms.org → `cdeprintworks-site`
- **Products**: adicionar, editar ou esconder produtos (desmarcar "Show on site")
- **Site settings**: trocar links do Etsy, redes e e-mail
- **Media**: subir fotos (vão para `images/`)
- Cada **Save** vira um commit e o site atualiza em 1–2 minutos

**Pelo GitHub:** editar ou subir arquivos direto no repositório (Add file → Upload files). Também publica sozinho.

## Visual

- Fundo creme `#F6ECDF`, azul-marinho `#0E2554`, azul `#1E50A0`, teal `#1CA8AA`
- Fonte Poppins (Google Fonts)
- Menu: Home · Shop · Custom Orders · About · Contact (sem logo no topo)
- Início com o logo completo e o slogan "Quality. Creativity. Service."
- Rodapé com ícones das redes e @cdeprintworks

## E-mail

- Cloudflare Email Routing: `contact@cdeprintworks.com` e catch-all (qualquer @cdeprintworks.com) → Gmail pessoal
- Envio como contact@ pelo Gmail ("Enviar e-mail como", smtp.gmail.com, senha de app)
- SPF: `v=spf1 include:_spf.mx.cloudflare.net include:_spf.google.com ~all`

## Observações

- A foto das tulipas vem direto do anúncio do Etsy. Se a foto do anúncio mudar, trocar no painel
- O card de Natal é "Coming Soon" e o botão leva para a seção de pedidos personalizados (`#custom`)

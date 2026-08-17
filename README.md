# AgendaVip — landing page do produto

Landing page de produto do **AgendaVip**: vende a agenda online para
barbearias (agendamento sem sobreposição de horário, aviso automático no
WhatsApp, painel de faturamento por barbeiro). Reaproveita a mesma paleta,
tipografia (Inter) e cards do painel real do app como identidade visual, pra
ficar reconhecível como o mesmo produto.

Não confundir com o [LandPageConvito](../LandPageConvito) ou o
[LandPageImpulsoTech](../LandPageImpulsoTech): aquelas vendem outros
produtos/serviços da Contech; esta vende o AgendaVip.

## Stack

Página estática, sem build nem dependências:

- `index.html` — HTML + CSS puro (sem JavaScript além do `<details>` nativo
  do FAQ); fontes (Inter, Instrument Serif, IBM Plex Mono) embutidas como
  `data:` URI no próprio CSS, funciona offline
- Tema claro/escuro automático (`prefers-color-scheme`), com paleta idêntica
  à do painel do AgendaVip (`--color-ambar-*` / `--color-carvao-*` em
  `agendaVip/src/app/globals.css`)

Preços e recursos exibidos vêm direto do código do produto
(`agendaVip/src/lib/planos.ts` e `README.md`), não são inventados.

## Rodando localmente

```bash
# Windows
start index.html
```

## Deploy

HTML estático, publica em qualquer hospedagem sem configuração:

- **GitHub Pages**: Settings → Pages → Deploy from branch
- **Vercel / Netlify**: importe o repositório, sem build command

## Publicado em

https://maiconqatech.github.io/agendashow-landing/

## Pendências antes de divulgar

- Os botões "Criar conta grátis" / "Entrar" / "Começar" ainda apontam pra
  `#`: trocar pela URL pública do app assim que o AgendaVip tiver um
  domínio de produção (hoje só existe `NEXT_PUBLIC_APP_URL=localhost` no
  `.env.example` do app).
- Sem `og-image.png` ainda: as tags `og:image`/`twitter:card` foram
  deixadas de fora de propósito pra não referenciar uma imagem que não
  existe; adicionar quando tiver uma arte de compartilhamento.

## Outros protótipos considerados

Esta landing page ("Painel ao Vivo") foi uma de três opções de layout
geradas para escolha; as outras duas (uma com a agenda como régua de
horários, outra no formato de ficha/bilhete de barbearia) ficaram só como
protótipos descartados, não versionadas neste repositório.

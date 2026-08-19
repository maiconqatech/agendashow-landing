# AgendaVip — redirecionamento pro login

Este site (`https://maiconqatech.github.io/agendashow-landing/`) não é mais
uma landing page de vendas: é só uma página de redirecionamento automático
pra tela de login do app real
(`https://agendavip-six.vercel.app/login`). Continua publicado nesta URL
por causa de links/divulgação antigos que já apontam pra ela.

Não confundir com o [LandPageConvito](../LandPageConvito) ou o
[LandPageImpulsoTech](../LandPageImpulsoTech): aquelas vendem outros
produtos/serviços da Contech.

## Stack

Página estática, sem build nem dependências:

- `index.html` — HTML + CSS mínimo, com `<meta http-equiv="refresh">` e
  `location.replace()` em JS pra redirecionar pra
  `https://agendavip-six.vercel.app/login`; um link de fallback fica
  visível caso o redirecionamento automático seja bloqueado.

## Histórico

Até agosto/2026 este repositório publicava uma landing page de vendas
completa (hero, preços, FAQ) reaproveitando a paleta/tipografia do painel
do AgendaVip. Foi substituída por este redirecionamento simples porque o
app já tem sua própria tela de login/registro pública; ver histórico do
git pra recuperar o conteúdo antigo se precisar.

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

## Pendências

- Se o domínio de produção do app mudar, atualizar a URL de destino em
  `index.html` (`<meta http-equiv="refresh">`, `location.replace()` e o
  link de fallback) e neste README.

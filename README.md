# Ajuda Beefans, documentação

Documentação pública da Beefans, publicada em
**https://beefans.com.br/docs**.

Feita com [Mintlify](https://mintlify.com): as páginas são arquivos `.mdx` e a
navegação inteira sai do `docs.json`.

## Rodar localmente

```bash
npm i -g mint
mint dev        # na raiz do repositório, onde está o docs.json
```

Abre em http://localhost:3000.

## Como as páginas são organizadas

Cada tutorial segue o mesmo formato:

1. Uma frase de resultado ("ao fim disso, quem assinar entra sozinho no VIP")
2. O vídeo do YouTube, pelo componente `<Video id="..." />` (`snippets/video.mdx`)
3. O que você vai precisar (`<Check>`)
4. Passo a passo (`<Steps>`)
5. Perguntas frequentes (`<AccordionGroup>`). O texto vem da descrição do
   vídeo no YouTube, para as duas fontes nunca divergirem
6. Próximo passo (`<CardGroup>`)

## Identidade visual

Os valores vêm dos tokens reais do `bee-front`, não de aproximação:

| Item | Valor | Origem |
| --- | --- | --- |
| Rosa da marca | `#fc3a68` | `--primary: 343 97% 61%` em `src/app/globals.css` |
| Fundo escuro | `#0a0a0a` | `--background: 0 0% 3.9%` |
| Fonte de texto | Plus Jakarta Sans | `tailwind.config.ts` |
| Fonte de título | Fraunces | `tailwind.config.ts` (display) |
| Logo / favicon | monograma rosa | `bee-front/public/icon/` |

Ajustes finos de CSS ficam em `style.css`.

## Vídeos

Canal: https://www.youtube.com/@beefanss

| # | Tutorial | Página | Vídeo |
| --- | --- | --- | --- |
| 1 | Criar e verificar sua conta | `comecar/criar-conta` | a gravar |
| 2 | Publicar: feed e exclusivo | `publicar/feed-e-exclusivo` | a gravar |
| 3 | Bot do Telegram e VIP automático | `telegram/criar-bot` | `ceEo4PU50xs` |
| 4 | Mensagem de boas-vindas | `chat/mensagens-automaticas` | a gravar |
| 5 | Criar e vender packs | `vender/packs` | a gravar |
| 6 | Chat ao vivo | `chat/chat-ao-vivo` | `SDenfzDNA-E` |
| 7 | Leads do bot: disparos | `telegram/leads-e-disparos` | `ovifNq8Vp4E` |

Quando um vídeo novo sair, troque o `<EmBreve>` da página pelo `<Video>` com o
ID e copie o bloco de FAQ da descrição do YouTube.

## De onde vem o passo a passo

Os rótulos citados nas páginas são os textos reais das telas do `bee-front`, não
paráfrase. Antes de escrever ou revisar um passo, abra a tela correspondente:

| Página do docs | Tela |
| --- | --- |
| `comecar/criar-conta` | `src/fan/components/become-creator/BecomeCreatorWizard.tsx` + `src/fan/i18n/domains/profile.ts` |
| `publicar/feed-e-exclusivo` | `dashboard/midias/page.tsx`, `components/gallery/CreateCarouselPostSheet.tsx` |
| `vender/packs` | `dashboard/produtos/[slug]/packs/`, `components/conteudos/addButton.tsx` |
| `chat/mensagens-automaticas` | `dashboard/automations/page.tsx` |
| `telegram/criar-bot` | `dashboard/telegram/page.tsx` |
| `telegram/leads-e-disparos` | `dashboard/disparos/page.tsx`, `dashboard/produtos/[slug]/leads/` |

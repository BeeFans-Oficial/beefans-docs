# Ajuda Beefans — documentação

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
5. Perguntas frequentes (`<AccordionGroup>`) — o texto vem da descrição do
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

| # | Tutorial | Vídeo |
| --- | --- | --- |
| 1 | Criar e verificar sua conta | a gravar |
| 2 | Publicar: feed social e exclusivo | a gravar |
| 3 | Bot do Telegram e VIP automático | `ceEo4PU50xs` |
| 4 | Mensagem de boas-vindas | a gravar |
| 5 | Criar e vender packs | a gravar |
| 6 | Chat ao vivo | `SDenfzDNA-E` |
| 7 | Leads do bot: disparos | `ovifNq8Vp4E` |

Quando um vídeo novo sair, troque o `<EmBreve>` da página pelo `<Video>` com o
ID e copie o bloco de FAQ da descrição do YouTube.

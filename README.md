# Roteiro no Claude

Um comentário com milhares de curtidas é o que milhares de pessoas estão pensando. Esta skill pega os comentários mais curtidos de um Reel viral e transforma em **10 roteiros de Reels para o seu negócio**.

Você escreve:

> Me faz roteiros de Reels a partir deste vídeo: instagram.com/reel/...

E o Claude:
1. pergunta o que você vende, pra quem e qual palavra você quer nos comentários;
2. pega os comentários do vídeo (sozinho, com o Apify conectado, ou você cola);
3. separa o que as pessoas estão pensando: dúvida, objeção, desejo, crítica, identificação;
4. entrega 10 roteiros com gancho, virada, explicação e chamada, cada um mostrando de qual comentário saiu.

Nada é inventado: os roteiros não usam número, resultado ou depoimento que você não tenha dado.

## Instalação em 1 passo

Abra o Claude Code e cole:

```
Instala pra mim o https://github.com/brabruno13/roteiro-no-claude. Lê o INSTALL.md e segue os passos.
```

O que você vai precisar:
- Claude Code;
- opcional: uma conta no Apify, para buscar os comentários sozinho. Sem ela, você cola os comentários e funciona igual.

## O que tem aqui
- `skills/roteiro-no-claude/`: a skill com o método.
- `INSTALL.md`: o passo a passo que o Claude Code segue para instalar.

## Créditos
A busca automática de comentários usa o [Instagram Comments Scraper](https://apify.com/apify/instagram-comment-scraper), do Apify, pelo servidor MCP oficial [@apify/actors-mcp-server](https://github.com/apify/actors-mcp-server). Este repositório não tem ligação com o Instagram, a Meta ou o Apify.

## Quer ir mais rápido?
Um mês inteiro de roteiros num comando, 3 ganchos por roteiro e a biblioteca de ganchos por formato estão no **Roteiro PRO**: **https://roteiro-no-claude.vercel.app**

Feito por [@o.brabruno](https://instagram.com/o.brabruno) · DHG

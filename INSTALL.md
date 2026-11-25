# Instalação (para o Claude Code seguir)

Você é o Claude Code instalando o "Roteiro no Claude" no computador do usuário. Faça tudo você mesmo e só peça ao usuário o que só ele pode fazer (o token do Apify, se ele quiser o caminho automático, e confirmações). Explique cada pedido em português simples. Nunca mostre o token na tela depois que o usuário colar.

## O que precisa existir

1. A skill `roteiro-no-claude` copiada para a pasta de skills do Claude. Isso é obrigatório e é tudo o que precisa para usar a skill colando os comentários.
2. Opcional: o servidor MCP oficial do Apify, para buscar os comentários sozinho a partir do link do Reel.

## Passos

### 1. Skill

```bash
mkdir -p ~/.claude/skills
cp -r ./skills/roteiro-no-claude ~/.claude/skills/
```
(rode de dentro da pasta deste repositório)

### 2. Pergunte se o usuário quer o caminho automático

Explique: "A skill funciona colando os comentários do Reel aqui. Se você quiser que ela busque os comentários sozinha pelo link, dá pra conectar o Apify. A conta grátis do Apify traz só os 15 comentários mais recentes. Para pegar os mais curtidos, precisa de um plano pago do Apify (confira o preço no site deles). Quer conectar?"

Se ele disser que não, pule para o passo 4.

### 3. Apify (opcional)

Peça para ele:
1. Criar uma conta em apify.com (dá para entrar com o Google).
2. Abrir console.apify.com/settings/integrations e copiar o "Personal API token".
3. Colar o token aqui quando você pedir.

Confira se o Node.js existe com `node --version` (precisa ser 18 ou mais novo). Se não existir, mostre ao usuário o comando de instalação do sistema dele e espere ele confirmar.

Peça o token uma vez e registre o servidor sem ecoar o valor:
```bash
claude mcp add apify --scope user -e APIFY_TOKEN="$TOKEN" -- npx -y @apify/actors-mcp-server --tools apify/instagram-comment-scraper
```

### 4. Teste

Peça ao usuário para reiniciar o Claude Code. Depois diga que está pronto e sugira o primeiro pedido:

"Me faz roteiros de Reels a partir deste vídeo: [link de um Reel viral do seu nicho]"

## Segurança

- O token do Apify dá acesso à sua conta e aos seus créditos. Não compartilhe e não publique.
- A skill só lê comentários públicos. Ela não posta, não comenta e não manda mensagem por você.

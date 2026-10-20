PÁGINA DE RETORNO OAUTH — MEU PAINEL FINANCEIRO

Conteúdo público, sem Client Secret nem tokens.

CONFIGURAÇÃO
1. Crie no GitHub um repositório público chamado: meu-painel-oauth
2. Envie os arquivos index.html e callback.html para a raiz (branch main).
3. Abra Settings > Pages.
4. Em Build and deployment, selecione Deploy from a branch; Branch: main; Folder: /(root); salve.
5. Aguarde o GitHub Pages publicar o site.
6. A Redirect URI será exatamente:
   https://SEU-USUARIO.github.io/meu-painel-oauth/callback.html
   Substitua SEU-USUARIO pelo seu nome de usuário real do GitHub.
7. Cadastre essa URI no DevCenter do Mercado Livre e configure a MESMA URI em Monitor de preços > Pesquisa automática — Mercado Livre > Configurar autorização OAuth 2.0.
8. Confirme que a URL pública termina em /callback.html antes de usar no OAuth.

SEGURANÇA
- Nunca coloque Client Secret, access token ou refresh token no repositório.
- A URL de retorno contém um código temporário e state. Não compartilhe a URL completa retornada pelo Mercado Livre; cole somente no aplicativo local que iniciou o fluxo.
- Essa página não armazena nem envia os parâmetros a um serviço próprio; só os lê no navegador e oferece um botão para copiar a URL completa.
- Se a autorização no DevCenter exigir uma callback com backend/HTTPS dinâmico ou rejeitar o GitHub Pages project URL, não tente improvisar. Pare e revise o formato aceito na documentação do Mercado Livre.

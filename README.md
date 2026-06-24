# BergamoTech Portfolio

Portfólio pessoal de Vinícius Trindade Bérgamo para o domínio `bergamotech.com.br`.

## Estrutura

- `index.html`: site estático pronto para deploy.
- `assets/`: imagens e arquivos públicos usados pelo site.
- `favicon.ico`, `site.webmanifest`, `robots.txt` e `sitemap.xml`: arquivos raiz usados por navegadores e buscadores.
- `vercel.json`: configuração pequena para servir assets com cache e URLs limpas.

## Contato público

- E-mail principal: `contato@bergamotech.com.br`
- Telefone/WhatsApp: `+55 35 98449-0651`

## Busca, favicon e prévias sociais

O site publica a identidade visual da BergamoTech em vários formatos para aumentar a chance de Google, Bing, navegadores e redes sociais exibirem a marca correta:

- `/favicon.ico`: fallback raiz para navegadores e buscadores.
- `/assets/favicon-48.png`: ícone PNG quadrado, múltiplo de 48 px, referenciado no HTML.
- `/assets/favicon-192.png` e `/assets/favicon-512.png`: ícones do manifest e dados estruturados.
- `/assets/apple-touch-icon.png`: ícone para dispositivos Apple.
- `/assets/bergamotech-og.png`: imagem Open Graph/Twitter para compartilhamentos.
- `site.webmanifest`, `robots.txt` e `sitemap.xml`: descoberta e metadados básicos para rastreadores.

Depois do deploy, solicite nova indexação no Google Search Console e no Bing Webmaster Tools. A troca do símbolo genérico pela logo depende do cache e do recrawl de cada buscador, então pode levar alguns dias ou semanas.

## Deploy sugerido na Vercel

1. Crie um projeto Vercel apontando para este repositório.
2. Em `Root Directory`, mantenha a raiz do repositório.
3. Adicione os domínios:
   - `bergamotech.com.br`
   - `www.bergamotech.com.br`
4. Configure o DNS no Registro.br ou no provedor escolhido.
5. Rode a inspeção do domínio na Vercel e ajuste os registros conforme ela pedir.

Depois do deploy, o domínio raiz fica para este portfólio e os outros projetos podem usar subdomínios como `financeiro.bergamotech.com.br` e `racha.bergamotech.com.br`.

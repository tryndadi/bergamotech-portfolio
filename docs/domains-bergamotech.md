# Domínios BergamoTech

Plano recomendado para `bergamotech.com.br`.

## Mapa

| Endereço | Projeto | Observação |
| --- | --- | --- |
| `bergamotech.com.br` | Portfólio pessoal | Site raiz da marca BergamoTech |
| `www.bergamotech.com.br` | Portfólio pessoal | Redirecionar para o domínio raiz |
| `financeiro.bergamotech.com.br` | Controle Financeiro | App web/mobile de finanças |
| `racha.bergamotech.com.br` | RACHA | Centralizador de eventos |
| `api.bergamotech.com.br` | API compartilhada ou gateway | Use só se fizer sentido ter uma API comum |
| `wiki.bergamotech.com.br` | Wiki/cases | Melhor publicar apenas conteúdo permitido pela empresa |

## DNS sugerido

Se o DNS ficar no Registro.br e os projetos ficarem na Vercel, adicione primeiro cada domínio no projeto Vercel correto. Depois use `vercel domains inspect` para confirmar os valores exatos.

| Tipo | Nome | Valor típico na Vercel |
| --- | --- | --- |
| `A` | `@` | `76.76.21.21` |
| `CNAME` | `www` | `cname.vercel-dns-0.com` |
| `CNAME` | `financeiro` | `cname.vercel-dns-0.com` |
| `CNAME` | `racha` | `cname.vercel-dns-0.com` |
| `CNAME` | `api` | `cname.vercel-dns-0.com` |

## Ordem de execução

1. Deploy do portfólio como projeto próprio, usando a raiz do repositório como root directory.
2. Adicionar `bergamotech.com.br` e `www.bergamotech.com.br` no projeto do portfólio.
3. Adicionar `financeiro.bergamotech.com.br` no projeto do Controle Financeiro.
4. Adicionar `racha.bergamotech.com.br` no projeto do RACHA quando ele estiver pronto.
5. Configurar a zona DNS no Registro.br com os registros apontados pela Vercel.
6. Aguardar propagação e verificar SSL na Vercel.

## Estado observado em 2026-06-24

- `bergamotech.com.br` responde com registros `A` públicos `104.21.91.64` e `172.67.167.127`.
- `www.bergamotech.com.br` responde com `CNAME` para `87874a343435e86a.vercel-dns-017.com`.
- `bergamotech.com.br` tem MX do Zoho (`mx.zoho.com`, `mx2.zoho.com`, `mx3.zoho.com`), compatível com o e-mail público `contato@bergamotech.com.br`.

## Busca e identidade visual

Para ajudar Google, Bing e outros rastreadores a exibirem a marca em vez de um símbolo genérico, o portfólio publica:

- `/favicon.ico` no root do domínio.
- Ícones PNG em `/assets/favicon-48.png`, `/assets/favicon-192.png`, `/assets/favicon-512.png` e `/assets/apple-touch-icon.png`.
- `site.webmanifest` com os ícones de app.
- Metatags Open Graph/Twitter e JSON-LD `Organization` com `logo` e `email` em `index.html`.
- `robots.txt` apontando para `https://bergamotech.com.br/sitemap.xml`.

Após cada deploy que altere favicon, logo ou metadados, use a inspeção de URL no Google Search Console e no Bing Webmaster Tools para solicitar recrawl. Mesmo com tudo correto, a exibição final é controlada pelo buscador e pode continuar mostrando cache antigo por alguns dias ou semanas.

## Referências

- Vercel: https://vercel.com/docs/domains/set-up-custom-domain
- Registro.br: https://registro.br/tecnologia/caracteristicas-tecnicas/

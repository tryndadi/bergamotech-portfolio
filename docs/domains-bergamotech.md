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

1. Deploy do portfólio como projeto próprio, com `portfolio` como root directory.
2. Adicionar `bergamotech.com.br` e `www.bergamotech.com.br` no projeto do portfólio.
3. Adicionar `financeiro.bergamotech.com.br` no projeto do Controle Financeiro.
4. Adicionar `racha.bergamotech.com.br` no projeto do RACHA quando ele estiver pronto.
5. Configurar a zona DNS no Registro.br com os registros apontados pela Vercel.
6. Aguardar propagação e verificar SSL na Vercel.

## Estado observado em 2026-05-25

`bergamotech.com.br` já responde com SOA, mas ainda não encontrei registros públicos `A`/`CNAME` para o domínio raiz, `www`, `financeiro` ou `api`. Ou seja: o domínio existe, mas ainda parece não estar apontando para nenhum deploy público.

## Referências

- Vercel: https://vercel.com/docs/domains/set-up-custom-domain
- Registro.br: https://registro.br/tecnologia/caracteristicas-tecnicas/

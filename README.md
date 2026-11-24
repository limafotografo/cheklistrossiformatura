# Checklist Rossi Formatura

Aplicativo web responsivo para cadastrar itens de estoque, organizar materiais por formatura e salvar ou imprimir cada checklist em PDF.

## Acesso e dados

- O app usa login por link enviado ao e-mail.
- Somente diretores autorizados na tabela `event_checklist_directors` podem consultar ou alterar os dados.
- O estoque e os eventos ficam na tabela `event_checklist_state` do Supabase.
- Organizadores recebem o checklist exportado em PDF; não precisam de acesso ao app.
- O banco usa Row Level Security (RLS). A chave publishable no HTML é pública e depende dessas políticas; nunca coloque uma chave `service_role` ou `sb_secret` no site.

## Abrir o app

https://limafotografo.github.io/cheklistrossiformatura/

Para o login por e-mail funcionar, adicione este endereço em **Authentication → URL Configuration → Redirect URLs** no projeto Supabase:

`https://limafotografo.github.io/cheklistrossiformatura/`

O GitHub Pages publica o arquivo `index.html` da branch `main`.

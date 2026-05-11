# Fluxus Auth Landing — versão breve profissional

Página minimalista para confirmação de e-mail do Fluxus PDV.

## O que ela mostra

- Logo transparente do app
- Texto breve: **E-mail autenticado**
- Botão: **Voltar para o app**
- Efeitos visuais sutis com degradê, brilho, glassmorphism e animação leve

## GitHub Pages

Publique estes arquivos em um repositório e ative em:

`Settings > Pages > Deploy from a branch > main > /root`

## Supabase

Em `Authentication > URL Configuration`:

```text
Site URL:
https://SEU_USUARIO.github.io/fluxus-auth-landing

Redirect URLs:
https://SEU_USUARIO.github.io/fluxus-auth-landing/**
https://SEU_USUARIO.github.io/fluxus-auth-landing/auth/callback/**
fluxuspdv://auth/callback
```

## E-mails

Cole os arquivos de `supabase/email_templates/` nos templates correspondentes do Supabase.

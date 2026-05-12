# Fluxus Auth Landing conectado ao app

Arquivos prontos para GitHub Pages.

## Fluxo

1. Supabase envia e-mail de confirmação.
2. Usuário abre o link.
3. Supabase redireciona para `https://http-gauchin.github.io/fluxus-auth-landing/auth/callback/`.
4. A página mostra o botão **Voltar para o app**.
5. O botão abre `fluxuspdv://auth/callback` com os parâmetros recebidos.
6. O app Android recebe o deep link e o Supabase Kotlin tenta importar a sessão.

## Configuração no Supabase

Em **Authentication > URL Configuration**:

- Site URL: `https://http-gauchin.github.io/fluxus-auth-landing/`
- Redirect URL: `https://http-gauchin.github.io/fluxus-auth-landing/auth/callback/`
- Redirect URL opcional: `fluxuspdv://auth/callback`

## Arquivos principais

- `index.html`
- `auth/callback/index.html`
- `supabase/email_templates/confirm-signup.html`
- `supabase/email_templates/recovery.html`

# Fluxus Auth Landing — abrir APK instalado

Esta versão deixa o botão **Voltar para o app** abrindo o APK instalado no Android usando deep link:

```text
fluxuspdv://auth/callback
```

E no Chrome Android usa Intent URL apontando para o package:

```text
com.gauchin.pdvpremium
```

## Obrigatório no Android

No `AndroidManifest.xml`, dentro da `MainActivity`, precisa existir:

```xml
<intent-filter>
    <action android:name="android.intent.action.VIEW" />

    <category android:name="android.intent.category.DEFAULT" />
    <category android:name="android.intent.category.BROWSABLE" />

    <data
        android:scheme="fluxuspdv"
        android:host="auth"
        android:pathPrefix="/callback" />
</intent-filter>
```

Depois precisa gerar um APK novo e instalar no dispositivo.

## Supabase

Em `Authentication > URL Configuration`:

```text
Site URL:
https://SEU_USUARIO.github.io/NOME_DO_REPO

Redirect URLs:
https://SEU_USUARIO.github.io/NOME_DO_REPO/**
https://SEU_USUARIO.github.io/NOME_DO_REPO/auth/callback/**
fluxuspdv://auth/callback
```

## Teste

1. Instale o APK com o deep link.
2. Abra no navegador do Android:
   `https://SEU_USUARIO.github.io/NOME_DO_REPO/auth/callback/`
3. Toque em **Voltar para o app**.
4. O Fluxus PDV deve abrir.

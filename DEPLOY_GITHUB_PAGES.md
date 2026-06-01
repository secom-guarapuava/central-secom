# Deploy no GitHub Pages

Este projeto já está configurado para publicar um app Next.js estático no GitHub Pages usando GitHub Actions.

## Arquivo obrigatório

O workflow precisa existir exatamente neste caminho:

```txt
.github/workflows/deploy.yml
```

A pasta `.github` é uma pasta oculta no macOS. Se você abrir a pasta no Finder e ela não aparecer, pressione:

```txt
Command + Shift + .
```

## Configuração no GitHub

No repositório, vá em:

```txt
Settings > Pages
```

Deixe assim:

```txt
Source: GitHub Actions
```

Depois suba os arquivos para a branch `main`. A Action deve rodar automaticamente.

## Como conferir

Vá na aba:

```txt
Actions
```

Espere o workflow `Deploy Next.js to GitHub Pages` terminar com check verde.

Depois volte em:

```txt
Settings > Pages
```

O link aparecerá em `Your site is live at...`.

## Firebase

O Firebase pode ser configurado depois, em:

```txt
src/lib/firebaseConfig.ts
```

Depois de preencher as chaves, faça novo commit/push. O deploy roda novamente.

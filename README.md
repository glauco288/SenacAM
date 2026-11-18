# Senac Universo – Landing Page

Página de captação de leads da Faculdade Senac Amazonas. Um único `index.html` + o logo, sem build.

## 1. Publicar no GitHub Pages

```bash
git init
git add index.html senac-universo-logo.png README.md
git commit -m "Landing page Senac Universo"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/senac-universo.git
git push -u origin main
```

No GitHub: **Settings > Pages > Build and deployment > Source: Deploy from a branch**, branch `main`, pasta `/ (root)`. O site fica em `https://SEU-USUARIO.github.io/senac-universo/`.

## 2. Receber os dados do formulário

GitHub Pages é só estático, então o formulário precisa de um serviço externo. Recomendado: **Formspree** (plano gratuito).

1. Crie uma conta em https://formspree.io e clique em **New Form**.
2. Copie o ID do formulário (algo como `xyzabcd`).
3. Em `index.html`, troque `SEU_ID_AQUI` pelo ID, na linha:
   ```js
   const ENDPOINT = 'https://formspree.io/f/SEU_ID_AQUI';
   ```
4. Faça o commit e o push. Os envios chegam no seu e-mail e ficam no painel do Formspree.

Os campos enviados são `nome`, `email`, `telefone`, `unidade` e `curso`.

Alternativa sem conta externa: Google Forms ou uma planilha do Google Sheets com Apps Script. Se preferir, eu adapto.

## 3. Antes de divulgar

- Confirme os cursos e as unidades com a faculdade.
- Adicione a política de privacidade e o consentimento de contato, se a instituição exigir.
- Teste o formulário em produção e confira se o e-mail chegou.

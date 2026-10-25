# Minhas Finanças (PWA + Firebase + GitHub Pages)

O site é publicado no GitHub Pages; o login com Google e os dados continuam no Firebase (projeto financas-13c64).

## Publicar no GitHub Pages
1. Crie um repositório no GitHub (público, a menos que seu plano permita Pages em repositório privado) e envie todos os arquivos desta pasta, inclusive a pasta oculta `.github`, na branch `main`.
2. No repositório: Settings > Pages > Source: **GitHub Actions**.
3. Cada push na `main` publica o site automaticamente (aba Actions). O endereço será `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.
4. **Obrigatório:** no Console Firebase, Authentication > Settings > Authorized domains > adicionar `SEU-USUARIO.github.io`. Sem isso o login com Google dá erro `auth/unauthorized-domain`.
5. No celular, abra o endereço e use "Instalar app" / "Adicionar à tela inicial".

## Regras do Firestore
Cole o conteúdo de `firestore.rules` em Firestore Database > Regras > Publicar (ou `firebase deploy --only firestore:rules`).

## Observações
- Não abre direto pelo arquivo (file://). Para testar local: `npx serve` na pasta (e adicione `localhost` aos domínios autorizados, que já vem por padrão).
- Nunca coloque chaves de conta de serviço no repositório. O `firebaseConfig` web não é segredo; as regras do Firestore protegem os dados.

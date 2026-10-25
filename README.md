# Minhas Finanças (PWA + Firebase)

1. No Console Firebase, crie um projeto.
2. Authentication > Sign-in method > ative **Google**.
3. Firestore Database > criar banco (modo produção).
4. Configurações do projeto > Seus apps > adicione um app **Web** e copie o `firebaseConfig` para `firebase-config.js`.
5. No terminal, dentro desta pasta: `firebase login`, `firebase use --add` (escolha o projeto), depois `firebase deploy --only firestore:rules,hosting`.
6. Abra o endereço `.web.app` no celular e use "Instalar app" / "Adicionar à tela inicial".

Notas: não abre direto pelo arquivo (file://); teste com `firebase serve` ou depois do deploy. Nunca coloque chaves de conta de serviço neste projeto. O `firebaseConfig` web não é segredo; quem protege os dados são as regras em `firestore.rules`.

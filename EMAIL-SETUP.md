# Configurer l’envoi des confirmations e-mail

Le formulaire utilise EmailJS pour envoyer un accusé de réception depuis un site statique GitHub Pages. La configuration du compte EmailJS est nécessaire avant que l’envoi fonctionne.

## 1. Créer le service et les modèles

1. Créez un compte sur [EmailJS](https://www.emailjs.com/) et connectez l’adresse d’envoi de JEFIE.
2. Dans **Email Services**, créez le service e-mail. Notez son **Service ID**.
3. Créez un modèle principal de notification destiné à l’équipe JEFIE. Son contenu doit inclure `{{email}}` pour identifier l’adresse inscrite. Notez son **Template ID**.
4. Créez un modèle de confirmation destiné au participant. Réglez **To Email** sur `{{email}}`; vous pouvez utiliser `{{site_name}}`, `{{event_dates}}` et `{{event_location}}` dans son contenu.
   - **Objet suggéré :** Merci pour votre intérêt pour JEFIE Paris 2026
   - **Message suggéré :**

     Bonjour,

     Merci pour votre intérêt pour JEFIE Paris 2026 ! Nous avons bien reçu votre demande et vous tiendrons informé(e) dès l'ouverture officielle des inscriptions.

     Nous espérons vous retrouver à Paris les 27 et 28 novembre 2026.

     À bientôt,
     L'équipe JEFIE
5. Dans le modèle principal, ouvrez l’onglet **Auto-Reply**, associez le modèle de confirmation, puis enregistrez. Ainsi, une soumission envoie une notification à l’équipe et une confirmation au participant.

## 2. Renseigner les identifiants dans le site

Dans `index.html`, cherchez la constante `emailService` et remplacez les trois valeurs `YOUR_...` :

- `serviceId` : le Service ID EmailJS;
- `templateId` : le Template ID du modèle principal de notification;
- `publicKey` : la clé publique EmailJS, visible dans **Account → General**.

La clé publique est conçue pour être utilisée dans le navigateur. Ne mettez jamais de clé privée ni de mot de passe dans le code du site. Dans les réglages de sécurité EmailJS, limitez les domaines autorisés à votre domaine de site et à votre domaine GitHub Pages.

## 3. Tester l’inscription

Publiez les changements, soumettez une adresse de test et vérifiez la réception du message dans la boîte de l’équipe et dans celle du participant (y compris les courriers indésirables). Le formulaire affiche un succès seulement si EmailJS confirme l’envoi.

# Liste e-mail et campagnes JEFIE

## État actuel

Le formulaire du site n’est pas encore relié au compte Brevo. Il ne transmet ni n’enregistre les adresses saisies, et il l’indique clairement aux visiteurs. Ne pas le présenter comme une inscription active avant son raccordement.

## Raccordement à Brevo

Utiliser le compte détenu par JEFIE afin que l’équipe conserve l’accès aux contacts, à leur export et aux campagnes :

1. Dans Brevo, ouvrir **Marketing > Forms > Sign-up** et créer un formulaire intégré (ou ouvrir celui de JEFIE déjà créé).
2. L’associer à la liste dédiée à l’ouverture des inscriptions. Activer la confirmation double opt-in et le champ de consentement adapté.
3. Dans **Share**, copier le code d’intégration **Iframe** recommandé par Brevo. Transmettre ce code pour l’intégrer à la fenêtre du site. Ne jamais partager la clé API privée ni l’insérer dans `index.html`.
4. Tester une inscription, vérifier que le contact apparaît dans la bonne liste et tester son export depuis le compte JEFIE avant d’ouvrir le formulaire.
5. Vérifier dans le forfait Brevo la capacité d’envoi mensuelle et journalière correspondant au nombre de destinataires prévu pour l’annonce.

Brevo indique une limite de 300 e-mails par jour pour son offre gratuite. Un envoi à plusieurs milliers de personnes le même jour nécessite de vérifier et, si nécessaire, d’augmenter la capacité du forfait. Voir [les limites et forfaits Brevo](https://help.brevo.com/hc/fr/articles/8292912279954-Ajouter-ou-supprimer-des-emails-%C3%A0-votre-offre).

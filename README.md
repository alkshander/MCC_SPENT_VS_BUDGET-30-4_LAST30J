Voici la version synthétique et formatée pour votre fichier README.md sur GitHub.

Google Ads 30-Day Budget Alert (MCC) 🚨
Ce script MCC surveille la cohérence budgétaire sur une fenêtre glissante de 30 jours. Il identifie les campagnes dont la dépense réelle récente dépasse la capacité théorique définie par leur budget quotidien actuel.

⚡ Fonctionnalités
Analyse 30 Jours Glissants : Compare le coût réel des 30 derniers jours vs le budget mensuel théorique.

Détection d'Anomalies : Utile pour repérer les campagnes dont le budget a été récemment baissé mais qui ont accumulé beaucoup de dépenses avant, ou les sur-diffusions.

Exécution Parallèle : Traitement rapide de tous les comptes du MCC.

Alerte Email : Envoi d'un rapport HTML clair classé par gravité de dépassement.

📐 La Formule
L'alerte se déclenche si :

Co 
u
^
 t 
30j
​	
 >(BudgetQuotidien×30.4)
>
Voici la version synthétique et formatée pour votre fichier README.md sur GitHub.

Google Ads 30-Day Budget Alert (MCC) 🚨
Ce script MCC surveille la cohérence budgétaire sur une fenêtre glissante de 30 jours. Il identifie les campagnes dont la dépense réelle récente dépasse la capacité théorique définie par leur budget quotidien actuel.

⚡ Fonctionnalités
Analyse 30 Jours Glissants : Compare le coût réel des 30 derniers jours vs le budget mensuel théorique.

Détection d'Anomalies : Utile pour repérer les campagnes dont le budget a été récemment baissé mais qui ont accumulé beaucoup de dépenses avant, ou les sur-diffusions.

Exécution Parallèle : Traitement rapide de tous les comptes du MCC.

Alerte Email : Envoi d'un rapport HTML clair classé par gravité de dépassement.

📐 La Formule
L'alerte se déclenche si :

Co 
u
^
 t 
30j
​	
 >(BudgetQuotidien×30.4)
⚙️ Configuration
Modifiez la variable CONFIG au début du script :

JavaScript
var CONFIG = {
  // 1. Multiplicateur mensuel (Standard Google : 30.4)
  DAYS_MULTIPLIER: 30.4, 

  // 2. Emails pour recevoir l'alerte (Requis)
  RECIPIENT_EMAILS: "votre.email@domaine.com", 

  // 3. Filtrer les comptes par libellé (Optionnel, laisser "" pour tout scanner)
  ACCOUNT_LABEL: "" 
};
📦 Installation
Dans votre compte MCC Google Ads, allez dans Scripts.

Créez un nouveau script et collez le code complet.

Renseignez votre adresse email dans RECIPIENT_EMAILS.

Autorisez le script et lancez un Aperçu.

Planifiez une exécution (ex: Hebdomadaire le Lundi matin).

⚠️ Cas d'usage typique
Ce script est particulièrement efficace pour détecter les erreurs de gestion budgétaire post-optimisation :

Exemple : Une campagne a dépensé 1000€ ce mois-ci. Hier, vous avez baissé son budget à 10€/jour (Capacité théorique ~304€). Le script vous alertera que la dépense passée (1000€) est incohérente avec le nouveau paramétrage (304€).

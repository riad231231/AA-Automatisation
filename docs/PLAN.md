# Plan de Réalisation Pas à Pas

## Phase 1 : Infrastructure de Données (La Fondue)
1. **Airtable** : Création d'une base avec les tables suivantes :
   - `Contacts` : Clients et prospects.
   - `Chantiers` : Détails techniques, dates, statut.
   - `Devis/Factures` : Lié aux chantiers, montants, statut de paiement.
   - `Documents` : Pièces jointes (Photos, Attestations, PPSPS).

## Phase 2 : Flux de Capture (Le "Lead Magnet")
1. **Formulaire Tally** :
   - Champs : Identité, Adresse intervention, Type de toiture/fçade, Upload photos.
2. **Workflow n8n (Capture)** :
   - Trigger : Nouvel envoi Tally.
   - Action : Créer record dans Airtable.
   - Action : Analyse GPT-4o Vision des photos.
   - Action : Réponse SMS/Email automatisée.

## Phase 3 : Automatisation Documentaire
1. **Google Docs Template** : Création de modèles avec variables.
2. **Workflow n8n (Document)** :
   - Trigger : Changement de statut dans Airtable ("Générer Devis").
   - Action : Fusion des données avec Google Doc via n8n.
   - Action : Conversion PDF et stockage Drive.

## Phase 4 : Suivi et Maintenance
1. **Workflow n8n (Relance)** :
   - Trigger : Date de paiement dépassée.
   - Action : Envoi SMS automatisé.

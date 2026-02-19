# Structure de la Base de Données (Airtable)

Pour que les automatisations fonctionnent, nous avons besoin d'une structure solide dans Airtable. Voici les tables à créer :

## 1. Table : `PROSPECTS` (OU `CONTACTS`)
Cette table reçoit les données du formulaire Tally.
- **Nom du Prospect** (Texte court)
- **Email** (Email)
- **Téléphone** (Téléphone)
- **Adresse du Chantier** (Texte long)
- **Photos / Documents** (Pièce jointe) - *Crucial pour l'IA*
- **Description du besoin** (Texte long)
- **Statut** (Option unique : Nouveau, Qualifié, Devis envoyé, Perdu)
- **Date de création** (Date de création automatique)

## 2. Table : `CHANTIERS`
Liée aux prospects, elle contient les détails techniques.
- **Nom du Chantier** (Formule : Nom Prospect + Date)
- **Difficulté IA** (Nombre 1-5)
- **Notes de Sécurité** (Texte long - Analyse IA)
- **Matériel Requis** (Texte long)
- **Dates d'intervention** (Plage de dates)
- **Statut Chantier** (Option unique : À planifier, En cours, Terminé)
- **Lien Dossier Drive** (URL)

## 3. Table : `DOCUMENTS_ADMIN`
Pour générer les Devis et PPSPS.
- **Type** (Option unique : Devis, Facture, PPSPS, Rapport Photo)
- **Fichier PDF** (Pièce jointe)
- **Lien Chantier** (Lien vers une autre fiche : Table Chantiers)
- **Montant HT** (Devise)
- **Statut Paiement** (Option unique : Non payé, Payé, Retard)

---

### Prochaines étapes :
1. Créez un compte gratuit sur [Airtable.com](https://airtable.com).
2. Créez une base nommée "Gestion Cordiste".
3. Créez ces 3 tables avec les colonnes indiquées.

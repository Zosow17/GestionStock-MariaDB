# Mini-projet GestionStock – MariaDB

Projet réalisé dans le cadre du BUT RT R310.

## Objectif
Déployer une base MariaDB sécurisée pour la gestion de stock d’une PME.

## Contenu
- Création de la base et des tables
- Relations (clés primaires / étrangères)
- Requêtes SQL métier
- Gestion des utilisateurs et privilèges
- Tests de droits
- Sauvegarde et restauration

## Outils
- WAMP
- MariaDB
- phpMyAdmin

## Sécurité
- Utilisation d’utilisateurs dédiés
- Privilèges limités
- Connexion restreinte par IP
			








#le shéma

┌───────────────┐
│  typeProduit  │
├───────────────┤
│ id (PK)       │
│ libelle       │
└───────┬───────┘
        │ 1
        │
        │ N
┌───────▼───────┐
│    produit    │
├───────────────┤
│ id (PK)       │
│ nom           │
│ stock         │
│ prix          │
│ type_id (FK)  │
└───────────────┘

┌───────────────┐
│     User      │
├───────────────┤
│ id (PK)       │
│ username      │
│      │
└───────┬───────┘
        │ 1
        │
        │ N
┌───────▼───────┐
│    Facture    │
├───────────────┤
│ id (PK)       │
│ date_facture  │
│ montant       │
│ user_id (FK)  │
└───────────────┘

La période d'analyse court du 1er janvier 2023 au 31 décembre 2026, soit une période de 3 années.

# 📊 Data Dictionary

## 🏗️ Table: `Chantiers`

| Colonne        | Description |
|----------------|------------|
| chantier_id    | Identifiant unique du chantier |
| nom_chantier   | Nom fictif du chantier |
| client         | Nom du client (entreprise, collectivité ou particulier) |
| type_client    | Type de client (Entreprise, Collectivité, Particulier) |
| type_travaux   | Nature des travaux (gros œuvre, rénovation, industriel…) |
| code_postal    | Code postal du chantier (zone d’intervention) |
| date_debut     | Date de début du chantier |
| date_fin       | Date de fin du chantier |
| ca_facture     | Chiffre d’affaires total facturé pour ce chantier |
| ca_prevu       | Chiffre d’affaires initialement estimé (devis) |

---

## 💸 Table: `Couts`

| Colonne      | Description |
|--------------|------------|
| chantier_id  | Identifiant du chantier associé |
| date         | Date de la dépense |
| type_cout    | Catégorie de coût (Achats, Charges externes, Personnel) |
| montant      | Montant de la dépense |

---

## 🧾 Table: `Factures`

| Colonne        | Description |
|----------------|------------|
| facture_id     | Identifiant unique de la facture |
| chantier_id    | Chantier associé à la facture |
| date_facture   | Date d’émission de la facture |
| date_echeance  | Date limite de paiement |
| montant        | Montant de la facture |
| date_paiement  | Date de paiement (vide si non payé) |

---

## 🧠 Lecture du modèle

- `Chantiers` : table centrale (niveau projet)  
- `Couts` : dépenses opérationnelles  
- `Factures` : flux de facturation et encaissement  

Ce modèle permet de :
- reconstruire la rentabilité (EBE)  
- suivre la trésorerie  
- identifier les retards de paiement  

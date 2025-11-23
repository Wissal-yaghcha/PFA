                                                          MediData Guardian AI — Plateforme intelligente de fiabilisation des données médicales

**Profil de chacun:**
1er membre: YAGHCHA Wissal
            email: yaghchawissal@gmail.com
            tel: 0610976010
2eme membre: BENRITOUNIA Imad
            email: benritouniaimad07@gmail.com
            tel: 0622854828
            
**Cahier des charges:**
🎯 Objectif général

Développer une plateforme permettant de contrôler la qualité des données médicales (patients, consultations, mesures médicales), d’identifier automatiquement les valeurs aberrantes, et d’assurer la fiabilité des informations de santé avant leur analyse ou intégration dans les systèmes hospitaliers.

🧰 Objectifs fonctionnels 

🔹 Acquisition de données médicales
Lecture de fichiers CSV ou API contenant des données :
    tension artérielle
    fréquence cardiaque
    glycémie
    température
    saturation O₂
    données patients

🔹 ETL — Pipeline complet
    Extract : Importation des données médicales brutes
    Transform : Nettoyage + calcul de mesures dérivées
    Validate : Application de règles médicales (domaines de valeurs)
    IA Anomalies : Détection de valeurs physiologiques anormales
    Load : Stockage dans une base de données PostgreSQL

🔹 Règles métier médicales (exemples)
    Glycémie entre 70 et 180 mg/dL
    Fréquence cardiaque entre 50 et 160 bpm
    Tension systolique entre 80 et 180 mmHg
    Température entre 35°C et 42°C
    Saturation O₂ ≥ 90%
    Les valeurs hors plage → erreurs médicales ou anomalies.

🔹 Tableau de bord
    Dashboard Streamlit affichant :
    mesures normales vs anormales
    patients à risque
    anomalies IA
    KPIs (qualité, taux d’erreur…) 
    
**Étude Comparative**

| Projet / Outil             | Ce qu'il fait                 | Limites                            |
| -------------------------- | ----------------------------- | ---------------------------------- |
| **OpenMRS**                | Gestion patients hospitalier  | Ne fait pas la qualité des données |
| **MIMIC-III pipeline**     | Données hospitalières réelles | Très lourd, difficile à déployer   |
| **Google Healthcare API**  | Normalisation HL7/FHIR        | Pas de détection IA intégrée       |
| **Clinical ETL pipelines** | Nettoyage + intégration       | Peu d’IA, approche traditionnelle  |

**Dataset**
Dataset synthétique 

Créer un script Python pour générer un dataset de signes vitaux :
Exemples à générer :
    patient_id
    heart_rate (50–160)
    blood_pressure_systolic (80–180)
    blood_pressure_diastolic (50–120)
    temperature (35–42)
    glucose (70–300)
    oxygen_saturation (80–100)
    timestamp
💡 Avantage :
Pas de confidentialité, totalement contrôlé, facile à tester.

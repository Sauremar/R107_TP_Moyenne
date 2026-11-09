Markdown

# Application de Saisie et Calcul des Notes (Tkinter)

Cette application graphique développée en Python permet de saisir des notes pour différentes ressources et SAE, de récupérer les coefficients depuis un fichier Excel (`coefficients.xlsx`), de calculer les moyennes par Unité d'Enseignement (UE), d'évaluer la validation selon les règles du jury, et d'afficher un graphique récapitulatif.

## Prérequis

Assurez-vous d'avoir installé Python ainsi que les bibliothèques nécessaires :

```bash
pip install openpyxl matplotlib

Le fichier coefficients.xlsx doit être présent dans le même répertoire que le script principal pour que l'application puisse charger les coefficients.
Fonctionnalités

    Interface graphique (GUI) : Saisie intuitive des notes pour chaque matière et indication du semestre.

    Extraction des coefficients : Lecture dynamique des coefficients depuis le fichier Excel selon le semestre spécifié.

    Calcul des moyennes : Pondération des notes par leurs coefficients respectifs pour chaque UE.

    Simulation de jury : Évaluation automatique de la validation du semestre/année en fonction des seuils (notes inférieures à 8 ou 10).

    Visualisation graphique : Affichage d'un graphique en barres des moyennes obtenues par UE.

⚠️ Bug Connu

    Attention : Un bug est actuellement répertorié concernant la gestion des semestres supérieurs à 3. L'application peut rencontrer des comportements inattendus lors du traitement des coefficients ou de l'affichage des résultats pour ces semestres. Une correction est prévue dans une prochaine mise à jour.

Utilisation

    Lancez le script Python :
    Bash

    python nom_du_script.py

    Remplissez les champs de notes correspondants.

    Indiquez le semestre concerné dans le champ prévu à cet effet.

    Cliquez sur Valider pour afficher les résultats dans la console et ouvrir la fenêtre du graphique
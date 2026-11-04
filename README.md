📊 Calculateur de Moyennes (Interface Tkinter)
Ce projet est une application graphique développée en Python permettant de saisir ses notes de BUT (Ressources et SAE), de calculer les moyennes par Unité d'Enseignement (UE), d'évaluer la validation de l'année selon les règles du jury, et d'afficher un graphique récapitulatif.

🚀 Fonctionnalités
Interface Graphique (GUI) : Basée sur tkinter et ttk, permettant une saisie simple et intuitive des notes pour chaque ressource et SAE (R101 à R115, SAE11 à SAE16).

Calcul des Moyennes : Calcule automatiquement les moyennes pondérées pour 3 UE distinctes.

Simulation de Jury : Vérifie si l'année est validée, compensée ou non validée selon les notes obtenues (règles des seuils à 10 et 8).

Visualisation Graphique : Génère un graphique en barres avec matplotlib pour visualiser rapidement les moyennes obtenues par UE.

🛠️ Prérequis
Assurez-vous d'avoir Python installé sur votre machine, ainsi que la bibliothèque matplotlib (Tkinter est généralement inclus par défaut avec Python).

Pour installer matplotlib, exécutez la commande suivante dans votre terminal :

Bash
pip install matplotlib
⚙️ Utilisation
Téléchargez ou copiez le code source du script (par exemple dans un fichier main.py).

Lancez le script depuis votre terminal ou votre EDI favori :

Bash
python main.py
Renseignez vos notes dans les champs correspondants de la fenêtre qui s'ouvre.

Cliquez sur le bouton "Valider" pour :

Afficher le détail de vos moyennes dans la console.

Obtenir le verdict du jury.

Ouvrir le graphique interactif des moyennes.

📂 Structure du Code
res / entries : Définition de la liste des matières et création dynamique des champs de saisie (Entry).

coefficients_ue1, ue2, ue3 : Tableaux de pondération associés à chaque ressource pour le calcul des moyennes.

calcul(lst_notes, coefficients) : Fonction mathématique calculant la moyenne pondérée.

jury(moyennes) : Logique conditionnelle simulant la décision d'un jury de validation d'année.

valider() : Récupération des données utilisateur, déclenchement des calculs, affichage des résultats et génération du diagramme matplotlib.
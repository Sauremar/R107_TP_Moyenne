Calculateur de moyennes des trois UE — Version 3
📌 Présentation du projet

Ce programme Python permet de calculer les moyennes de trois unités d'enseignement (UE) à partir des notes obtenues dans différentes ressources et SAE.

Il utilise des coefficients spécifiques à chaque UE pour calculer les moyennes pondérées. Il affiche ensuite les résultats, donne une indication sur la validation de l'année selon les règles du jury et représente les moyennes sous forme de graphique.

🎯 Objectifs
Demander les notes de chaque ressource et SAE une seule fois.
Calculer la moyenne pondérée de chaque UE.
Afficher les trois moyennes obtenues sur 20.
Vérifier les conditions de validation de l'année.
Représenter les résultats avec un graphique en barres.
🛠️ Technologies utilisées
Python : langage de programmation utilisé pour développer le programme.
Matplotlib : bibliothèque utilisée pour créer et afficher le graphique des moyennes.
⚙️ Fonctionnement du programme
1. Définition des coefficients

Le programme commence par créer trois dictionnaires :

coefficients_ue1 : contient les coefficients des ressources et des SAE pour l'UE1.
coefficients_ue2 : contient les coefficients des ressources et des SAE pour l'UE2.
coefficients_ue3 : contient les coefficients des ressources et des SAE pour l'UE3.

Chaque dictionnaire associe une ressource ou une SAE à son coefficient. Un coefficient égal à zéro signifie que l'élément ne compte pas dans le calcul de la moyenne de l'UE concernée.

2. Saisie des notes

La fonction demande_note(ressource) demande à l'utilisateur de saisir sa note pour une ressource donnée.

Les notes sont ensuite enregistrées dans un dictionnaire appelé notes, qui associe chaque ressource à la note saisie.

Cette méthode permet de demander chaque note une seule fois, puis de la réutiliser pour calculer les moyennes des trois UE.

3. Calcul des moyennes

La fonction calcul(notes, coefficients) calcule la moyenne pondérée d'une UE.

Elle multiplie chaque note par le coefficient correspondant, additionne les résultats, puis divise cette somme par le total des coefficients.

La formule utilisée est :

Moyenne pondérée = somme des (notes × coefficients) / somme des coefficients.

La fonction est appelée trois fois, une fois pour chaque UE, en utilisant le dictionnaire de coefficients correspondant.

Les résultats sont stockés dans les variables moyenne_ue1, moyenne_ue2 et moyenne_ue3.

4. Vérification des résultats du jury

La fonction jury(moyennes) analyse les moyennes des trois UE afin d'afficher un message concernant la validation de l'année.

Elle distingue plusieurs situations :

Si toutes les UE ont une moyenne supérieure ou égale à 10, le programme annonce que l'année est validée.
Si au moins une UE a une moyenne strictement inférieure à 8, le programme indique que l'année n'est pas validée.
Si une seule UE a une moyenne strictement inférieure à 10, mais qu'aucune n'est inférieure à 8, le programme indique que les trois UE devront être validées en deuxième année.

Ces messages correspondent aux règles de décision programmées dans la fonction.

5. Affichage des moyennes

Le programme affiche dans la console les moyennes obtenues pour l'UE1, l'UE2 et l'UE3.

Ces résultats sont ensuite regroupés dans deux listes :

ue : contient les noms des trois unités d'enseignement.
moyennes : contient les moyennes calculées correspondantes.

Ces listes servent à préparer l'affichage graphique.

6. Création du graphique

La bibliothèque Matplotlib est utilisée pour représenter les moyennes sous forme de diagramme en barres.

Le graphique comporte :

Une barre pour chaque UE.
Une couleur différente pour chaque barre.
Un titre : « Moyennes des trois UE ».
Un axe horizontal indiquant les unités d'enseignement.
Un axe vertical représentant les moyennes sur 20.
Une échelle verticale allant de 0 à 20.
La valeur de chaque moyenne affichée au-dessus de sa barre.

Le graphique permet de comparer rapidement les résultats obtenus dans les trois UE.

▶️ Installation et utilisation
Prérequis

Python doit être installé sur l'ordinateur.

La bibliothèque Matplotlib doit également être disponible. Pour l'installer, exécutez la commande suivante dans un terminal :

pip install matplotlib

Lancement du programme
Enregistrez le code dans un fichier Python, par exemple main.py.
Ouvrez un terminal dans le dossier contenant le fichier.
Exécutez la commande suivante :
python main.py

Saisissez les notes demandées par le programme.
Consultez les moyennes affichées dans la console, le message du jury et le graphique obtenu.
🚀 Améliorations apportées dans la version 3

Cette version améliore l'organisation du programme en séparant les données, les calculs et l'affichage des résultats.

Les principales améliorations sont :

La création de trois dictionnaires distincts pour gérer les coefficients de chaque UE.
La saisie des notes une seule fois, grâce à un dictionnaire commun.
La réutilisation d'une fonction unique pour calculer les trois moyennes.
L'ajout d'une fonction dédiée à l'analyse des résultats du jury.
L'utilisation de listes pour regrouper les moyennes et préparer le graphique.
La visualisation des résultats avec un diagramme en barres.

Cette organisation rend le code plus lisible, limite les répétitions et facilite les modifications futures.

⚠️ Points à vérifier
Les notes doivent être saisies sous forme numérique, par exemple 12 ou 14.5.
Les notes saisies doivent correspondre à une échelle sur 20.
Le programme suppose que les coefficients définis sont corrects et que leur somme est non nulle pour chaque UE.
Les règles de validation appliquées par la fonction jury doivent correspondre aux règles officielles de la formation.

Remarque technique : dans le code fourni, la liste des unités est nommée ue, mais le graphique utilise ues. Il faut remplacer ues par ue dans l'appel à plt.bar() pour éviter une erreur. De plus, si plusieurs UE sont sous 10 sans qu'aucune soit sous 8, la fonction jury ne prévoit actuellement aucun message pour ce cas.

📌 Conclusion

La version 4 permet de calculer et de comparer les moyennes de trois UE à partir d'une seule saisie des notes. Grâce aux dictionnaires, aux fonctions et à Matplotlib, le programme est plus structuré et offre une représentation visuelle des résultats, tout en fournissant une première indication sur la validation de l'année.

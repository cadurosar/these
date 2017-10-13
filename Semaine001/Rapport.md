# Rapport hebdomadaire - Thèse Carlos

## Semaine 001 - 02/10/2017 - 07/10/2017

### Activités

* Lecture d'articles (Geometric deep learning, Convolutional Neural Network on Graphs)

* Instalation ordinateur

* Taches administratifs, formulaires d'inscription...

* Neurostic

* Définition de couche de pooling pour les CNN sur graphe 
    * Je suis en train d'implémenter cette couche
    * L'idée ce d'ameliorer les réseau que font partie de la thèse de Bastien 

* Code de Reinforcement Learning pour PyRat

### Pooling pour les réseau convolutionneles profonds sur graphe

Nous avons 4 pas pour faire le pooling:

#### 1 - Choisir les noeuds du graphe à garder

* On va apeller ces noeuds «vivants»
    * Les noeuds que nous allons jeter seront les noeuds «morts»
* Pour le moment les noeuds seront choisis de manière aleatoire

#### 2 - Conecter les «noeuds morts» aux «vivants» 
* Prendre la matrice de covariance
* Lines des «vivants» seront mis à 0
* Colonnes des «morts» seron mis à 0
* Sur chaque line des «morts» nous allons prendre la colonne de plus grande valeur
    * Cette colonne represente le noeud «vivant»
    * La line represente le noeud «mort»
    * Metre ce valeur à 1 et tous les autres à 0
* Maintenant nous avons la matrice de connexion entre les «morts» et les «vivants»
    * Où chaque noeud «mort» est connecté à un et seulement un vivant
    * Où chaque noeud «vivant» est connecté seulement à des noeuds morts
    * Ce que nous permets de faire le pooling

#### 3 - Fonction de Pooling

* Chaque noeud «vivant» a une vecteur de noeuds (tous les noeuds «morts» plus lui même)
* Nous allons garder pour chaque vecteur seulement la valeur la plus grande.
* Cette valeur va être la valeur du noeud «vivant»

#### 4 - Reconstruire le graphe
* Prendre la matrice de covariance
* Lines et colonnes des «morts» seront mis à 0
* 4-KNN sur chaque line
* Multiplier, element par element, la matrice d'adjacence et la matrice du 4-KNN  

Il peux avoir un cinquième pas, dans le cas du réseau de Bastien il faut passer la nouvelle matrice d'adjacence par le processus de translation que va créer le nouveau S. 
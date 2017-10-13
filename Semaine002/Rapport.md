# Rapport hebdomadaire - Thèse Carlos

## Semaine 002 - 09/10/2017 - 13/10/2017

### Activités

* Lecture d'articles (Geometric deep learning)

* Visite medicale d'embauche

* Premier essaie du Pooling 
    * environ 50% avec un code qu'avait un pétit erreur de concept (la partie de max pooling n'était pas vraiment coerent)
    * environ x% sans l'erreur de concept
    * Le code utilise trop de memoire
        * Tester matrice sparse
        * Reflechir code du pooling sans multiplication de matrice
    * [Jupyter notebook qu'explique l'implémentation du Pooling](Pooling.pdf)

* Code de Reinforcement Learning pour PyRat
    * J'arrive à entrainer le rat pour 5x5 et 10x10 sur le code «FakeRat»
        * Code «FakeRat» c'est une simulation de «PyRat»
        * Rats entrainés sur «FakeRat» marchent sur «PyRat»
        * Pas encore arrivè à entrainer sur 20x20
        * [«FakeRat» notebook](), [Trained Rat 10x10](FakeRat.pdf)
    * Je n'arrive pas trop à entrainer le rat sur «PyRat»
        * Problèmes de chiffre aleatoire que ne sont pas vraiment aleatoires (Bug random seed?)
        * Memê sans utiliser d'aleatoire, le rat arrive à 70,80% sur 5x5 
    
# Rapport hebdomadaire - Thèse Carlos

## Semaine 002 - 09/10/2017 - 13/10/2017

### Activités

* Lecture d'articles (Geometric deep learning)

* Visite medicale d'embauche

* Premier essaie du Pooling 
    * Le résultat reste toujours environ 50%
        * Meme si la version «image» et pas «graphe» du réseau depasse 70%
        * conv + pooling < conv pour les «graphes»
            * conv + pooling > conv pour les «images»
    * Le code utilise trop de memoire
        * Tester matrice sparse
        * Reflechir code du pooling sans multiplication de matrice
    * [Jupyter notebook qu'explique l'implémentation du Pooling](Pooling.html)

* Code de Reinforcement Learning pour PyRat
    * J'arrive à entrainer le rat pour 5x5 et 10x10 sur le code «FakeRat»
        * Code «FakeRat» c'est une simulation de «PyRat»
        * Rats entrainés sur «FakeRat» marchent sur «PyRat»
        * Pas encore arrivè à entrainer sur 20x20
        * [«FakeRat» notebook](FakeRat.html), [Trained Rat 10x10](fakerat.h5)
    * Je n'arrive pas trop à entrainer le rat sur «PyRat»
        * Problèmes de chiffre aleatoire que ne sont pas vraiment aleatoires (Bug random seed?)
        * Memê sans utiliser d'aleatoire, le rat arrive à 70,80% sur 5x5 
    
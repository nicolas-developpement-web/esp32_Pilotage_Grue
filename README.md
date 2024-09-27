# Pilotage d'une grue de modélisme avec Esp32
> Création d'une interface web de pilotage à base d'ESP32 à 8 relais

Creation d'un interface avec des boutons pour declencher des actions de type rotation/monte/descendre

## La page d'accueil permet les choix d'apparition des bouttons pour:
* La grue
* La rotonde
* le soudeur

### Caracteristique de la grue:
(On touche le bouton pour lancer l'action ce qui a pour effet de stoper les autres)
* Rotation (activation au touch uniquement, état off de l'autre relai pour éviter le cours circuit)
    * Un relai Normalement Ouvert pour rotation gauche
    * Un relai Normalement Ouvert pour rotation droite
* Monte (activation au touch uniquement, état off de l'autre relai pour éviter le cours circuit)
    * Un relai Normalement Ouvert pour monter
    * Un relai Normalement Ouvert pour descendre
* Action (activation au touch par togglering)
    * Un relai Normalement Ouvert pour activer l'aimant

### Caracteristique de la rotonde:
(On choisi son sens de rotation puis ont appuis sur action)
* Relai Normalement collé pour une préparation de rotation à gauche qui peut étre basculé à droite
* Second relai Normalement Ouvert qui change d'état pour 2 secondes au push et qui lance l'action de rotation prédefini

### Caracteristique du soudeur:
(On active le soudeur)
* Simple relai Normalement Ouvert qui change d'état pour 60 secondes au push avec blockage des nouvelles actions pour eviter le spam
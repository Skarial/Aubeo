# Backlog MVP - Aubeo

## Regles de priorisation

- P0 : indispensable au premier usage credible
- P1 : important pour stabiliser l'experience MVP
- P2 : utile ensuite, sans bloquer la premiere version

## Lot 0 - Cadrage produit et depot

### AB-001 - Initialiser la base documentaire
- Priorite : P0
- Objectif : poser le README, l'identite produit, le cahier fonctionnel v1 et le backlog MVP.
- Definition de fini : les documents sont presents, coherents entre eux et limites au perimetre Aubeo.

## Lot 1 - Coeur du reveil progressif Android

### AB-010 - Configurer une heure cible de reveil
- Priorite : P0
- Objectif : permettre a l'utilisateur de definir l'heure finale du reveil.
- Critere d'acceptation : une heure cible peut etre enregistree et relue sans ambiguite.

### AB-011 - Definir une duree totale de preparation
- Priorite : P0
- Objectif : permettre a l'utilisateur de choisir combien de temps avant l'heure cible la sequence commence.
- Critere d'acceptation : l'heure de debut de sequence est calculee a partir de l'heure cible et de la duree choisie.

### AB-012 - Declencher la phase lumiere
- Priorite : P0
- Objectif : lancer une premiere phase visuelle progressive au debut de la sequence.
- Critere d'acceptation : l'intensite lumineuse augmente progressivement jusqu'au niveau configure.

### AB-013 - Declencher les vibrations douces
- Priorite : P0
- Objectif : ajouter une phase haptique progressive apres la lumiere.
- Critere d'acceptation : les vibrations commencent apres la lumiere selon l'ordre defini et restent dans une intensite douce puis croissante.

### AB-014 - Declencher l'ambiance sonore
- Priorite : P0
- Objectif : ajouter une phase sonore progressive avant l'heure cible.
- Critere d'acceptation : le son demarre apres les vibrations et monte jusqu'au niveau configure.

### AB-015 - Garantir un reveil final a l'heure cible
- Priorite : P0
- Objectif : assurer un declenchement final si la sequence preparatoire n'a pas ete arretee avant.
- Critere d'acceptation : un reveil final distinct se declenche a l'heure cible.

### AB-016 - Arreter la sequence de reveil
- Priorite : P0
- Objectif : permettre a l'utilisateur de couper la sequence lorsqu'il est reveille.
- Critere d'acceptation : un arret utilisateur met fin a la phase en cours et enregistre localement le moment d'arret.

## Lot 2 - Reglages essentiels et lisibilite

### AB-020 - Regler les intensites maximales
- Priorite : P1
- Objectif : laisser l'utilisateur definir le niveau maximal de lumiere, de vibrations et de son.
- Critere d'acceptation : chaque canal dispose d'un niveau maximal simple a regler et a retrouver.

### AB-021 - Expliquer la sequence de reveil dans l'interface
- Priorite : P1
- Objectif : rendre le fonctionnement par phases immediatement compréhensible.
- Critere d'acceptation : l'utilisateur peut identifier l'ordre des phases et le role du reveil final sans documentation externe.

### AB-022 - Gérer les permissions Android nécessaires
- Priorite : P1
- Objectif : demander uniquement les autorisations indispensables au fonctionnement du reveil.
- Critere d'acceptation : les permissions requises sont demandées au bon moment et leur absence est expliquée clairement.

## Lot 3 - Adaptation simple et fiabilisation MVP

### AB-030 - Enregistrer l'historique local des arrets
- Priorite : P1
- Objectif : conserver les informations minimales nécessaires a l'ajustement progressif.
- Critere d'acceptation : pour chaque reveil, l'application stocke localement l'heure cible, l'heure d'arret et la phase atteinte.

### AB-031 - Ajuster legerement l'anticipation selon l'usage
- Priorite : P1
- Objectif : faire varier la preparation de facon simple et explicable selon les reveils precedents.
- Critere d'acceptation : l'application avance ou retarde legerement le debut de sequence selon une regle visible et bornée.

### AB-032 - Permettre le retour au reglage manuel
- Priorite : P1
- Objectif : laisser l'utilisateur annuler l'ajustement automatique.
- Critere d'acceptation : un reglage permet de revenir instantanément au parametre manuel de reference.

### AB-033 - Assurer le fonctionnement hors ligne du coeur du reveil
- Priorite : P1
- Objectif : ne pas dépendre du reseau pour le scenario principal.
- Critere d'acceptation : le reveil progressif reste utilisable sans connexion une fois configure.

## Lot 4 - Suite logique apres MVP

### AB-040 - Preparer l'extension iOS
- Priorite : P2
- Objectif : identifier les écarts de plateforme a traiter apres la stabilisation Android.
- Critere d'acceptation : une note de cadrage precise ce qui est specifiquement Android et ce qui pourra etre porte sur iOS plus tard.

# Backlog MVP - Aubeo

## Règles de priorisation

- P0 : indispensable pour un MVP crédible
- P1 : important pour stabiliser et rendre le MVP utile
- P2 : utile ensuite, sans bloquer le premier cycle produit

## Lot 0 - Fondations produit et documentation

- Priorité : P0
- Objectif : disposer d’un socle documentaire cohérent avant toute implémentation.
- Contenu :
  - aligner le README sur la vision produit ;
  - formaliser l’identité produit ;
  - formaliser le cahier fonctionnel v1 ;
  - formaliser un backlog MVP limité au périmètre réel.
- Dépendances :
  - aucune
- Critères d’acceptation :
  - les documents portent la même promesse produit ;
  - la séquence lumière -> vibrations douces -> ambiance sonore ou mode expérimental -> réveil final est explicitée partout de manière cohérente ;
  - aucune promesse médicale ou pseudo-scientifique n’apparaît ;
  - le périmètre Android d’abord est clair.

## Lot 1 - Expérience réveil v1

- Priorité : P0
- Objectif : rendre possible un réveil progressif complet et compréhensible autour d’une heure cible.
- Contenu :
  - définir une heure cible ;
  - définir une durée totale de préparation ;
  - proposer des profils de réveil simples ;
  - régler les intensités maximales de lumière, vibrations et son ;
  - exécuter la séquence progressive dans l’ordre prévu ;
  - permettre l’arrêt de la séquence ;
  - garantir le réveil final à l’heure cible.
- Dépendances :
  - lot 0
- Critères d’acceptation :
  - un utilisateur peut créer, modifier, activer et désactiver un réveil sans aide externe ;
  - un réveil comporte au minimum une heure cible, une durée de préparation et un profil ;
  - l’ordre des phases est fixe, visible dans l’interface et correspond à l’exécution attendue ;
  - le réveil final se déclenche si la séquence n’a pas été arrêtée avant l’heure cible ;
  - le mode expérimental, s’il est présent, est clairement étiqueté comme tel.

## Lot 2 - Logique adaptative v1

- Priorité : P1
- Objectif : ajuster légèrement l’anticipation du réveil à partir de signaux simples, locaux et explicables.
- Contenu :
  - enregistrer la phase d’arrêt ;
  - enregistrer le moment d’arrêt par rapport à l’heure cible ;
  - prendre en compte le feedback post-réveil lorsqu’il est fourni ;
  - ajuster légèrement le début de préparation à partir de signaux simples et locaux ;
  - exposer à l’utilisateur l’ajustement appliqué ;
  - permettre de désactiver l’adaptation et de revenir au réglage manuel.
- Dépendances :
  - lot 1
  - lot 3
- Critères d’acceptation :
  - les règles d’ajustement sont explicites ;
  - aucun changement brutal n’est appliqué ;
  - l’utilisateur peut comprendre et annuler l’ajustement ;
  - l’adaptation ne repose sur aucun discours d’analyse scientifique du sommeil.

## Lot 3 - Historique et feedback

- Priorité : P1
- Objectif : conserver une trace locale utile des réveils et recueillir un retour minimal après usage.
- Contenu :
  - stocker localement les réveils passés ;
  - conserver les informations minimales utiles à la compréhension et à l’adaptation ;
  - proposer un feedback post-réveil court ;
  - exposer un historique simple des réveils récents.
- Dépendances :
  - lot 1
- Critères d’acceptation :
  - l’historique reste lisible et non médicalisé ;
  - le feedback post-réveil ne bloque pas la sortie du réveil ;
  - seules les données définies comme utiles dans le cahier fonctionnel v1 sont conservées ;
  - aucune donnée biométrique ou médicale n’est stockée ;
  - l’utilisateur peut comprendre ce qui est retenu de ses réveils passés.

## Lot 4 - Cadrage technique du cœur du réveil

- Priorité : P1
- Objectif : cadrer les points techniques nécessaires au MVP sans entrer trop tôt dans une architecture lourde.
- Contenu :
  - cadrer le fonctionnement Android du réveil ;
  - cadrer les besoins minimaux de stockage local ;
  - cadrer les besoins liés à la planification locale du réveil ;
  - cadrer les besoins liés aux canaux lumière, vibrations et son ;
  - cadrer le fonctionnement hors ligne du cœur du réveil ;
  - cadrer le traitement du mode expérimental pour qu’il reste optionnel et correctement formulé.
- Dépendances :
  - lot 0
  - lot 1
- Critères d’acceptation :
  - les contraintes techniques principales du réveil sont identifiées sans figer prématurément l’architecture ;
  - les contraintes Android principales sont connues ;
  - le cœur du réveil ne dépend pas du réseau ;
  - le vocabulaire produit reste cohérent entre technique et documentation.

## Ordre recommandé d’exécution

1. Lot 0 - Fondations produit et documentation
2. Lot 1 - Expérience réveil v1
3. Lot 3 - Historique et feedback
4. Lot 2 - Logique adaptative v1
5. Lot 4 - Cadrage technique du cœur du réveil



# Cahier fonctionnel v1 - Aubeo

## 1. Objet du document

Ce document cadre la premiere version fonctionnelle d'Aubeo.
Il decrit le perimetre produit initial, le parcours principal, les regles de fonctionnement et les limites assumees pour la v1.

## 2. Vision produit

Aubeo est une application mobile de reveil progressif.
Son objectif est de remplacer un declenchement brutal a l'heure cible par une sequence preparatoire en plusieurs phases :

1. lumiere
2. vibrations douces
3. ambiance sonore
4. reveil final

La v1 vise une experience claire, locale et explicable.
Elle ne cherche pas a detecter les cycles du sommeil ni a fournir un accompagnement medical.

## 3. Perimetre v1

### Inclus

- Application mobile Android en priorite
- Configuration d'une heure cible de reveil
- Lancement automatique d'une sequence progressive avant l'heure cible
- Enchainement des phases dans l'ordre fixe : lumiere -> vibrations douces -> ambiance sonore -> reveil final
- Reglages essentiels de duree et d'intensite dans des bornes simples
- Logique adaptative locale, limitee et explicable
- Fonctionnement centre sur un usage individuel et quotidien

### Hors perimetre v1

- Version iOS
- Analyse du sommeil ou des cycles biologiques
- Promesses de bien-etre medical ou therapeutique
- Objets connectes externes
- Fonctions communautaires ou sociales
- Automatisations complexes difficiles a expliquer

## 4. Utilite utilisateur

Aubeo s'adresse a une personne qui souhaite un reveil moins abrupt que celui d'une alarme classique.
Le besoin principal est de preparer l'eveil avant l'heure cible au lieu de tout concentrer sur une sonnerie finale.

## 5. Parcours principal

1. L'utilisateur definit une heure cible de reveil.
2. L'utilisateur choisit une duree totale de preparation avant cette heure cible.
3. L'application planifie la sequence progressive.
4. A l'heure de debut calculee, la phase lumiere commence.
5. Les vibrations douces prennent le relais selon le plan prevu.
6. L'ambiance sonore demarre ensuite de facon progressive.
7. Si l'utilisateur n'a pas arrete la sequence avant, le reveil final se declenche a l'heure cible.
8. L'application enregistre localement le moment d'arret de la sequence pour alimenter l'ajustement simple des jours suivants.

## 6. Regles fonctionnelles v1

### 6.1 Heure cible

- L'heure cible est l'heure de reveil souhaitee par l'utilisateur.
- Le reveil final ne doit pas partir apres cette heure.
- Toute la sequence preparatoire doit se terminer au plus tard a cette heure.

### 6.2 Sequence progressive

- L'ordre des phases est fixe et non inversable en v1.
- Chaque phase doit monter progressivement en intensite, sans changement brusque volontaire.
- La sequence doit rester comprehensible par l'utilisateur : il doit pouvoir identifier qu'il s'agit d'une progression vers le reveil final.

### 6.3 Reglages essentiels

La v1 doit permettre a minima :

- de definir l'heure cible
- de definir la duree totale de preparation avant l'heure cible
- d'ajuster l'intensite maximale de la lumiere
- d'ajuster l'intensite maximale des vibrations
- d'ajuster le niveau maximal de l'ambiance sonore

## 7. Logique adaptative simple et explicable

La logique adaptative v1 repose uniquement sur des signaux locaux et observables dans l'application.
Elle n'utilise ni capteurs de sommeil, ni inference opaque.

### Regle proposee

- L'application observe a quelle phase l'utilisateur arrete la sequence et a combien de temps de l'heure cible cela se produit.
- Si l'utilisateur arrete la sequence tot, de facon repetee sur plusieurs reveils, Aubeo peut reduire legerement l'anticipation les jours suivants.
- Si l'utilisateur n'arrete la sequence qu'au reveil final, de facon repetee sur plusieurs reveils, Aubeo peut avancer legerement le debut de la preparation les jours suivants.
- Les ajustements doivent rester bornes, progressifs et toujours visibles dans les reglages.

### Garde-fous

- Ajustement local uniquement
- Pas de changement cache
- Pas de variation brutale d'un jour a l'autre
- Possibilite pour l'utilisateur de revenir au reglage manuel de base

## 8. Exigences produit non fonctionnelles

- Priorite Android pour la v1
- Fonctionnement fiable meme sans reseau pour le coeur du reveil
- Reglages simples a comprendre
- Terminologie produit coherente avec la promesse de reveil progressif
- Comportement predictible et explicable

## 9. Criteres de reussite v1

La v1 est consideree comme cadree si elle permet de definir un reveil progressif simple, de l'executer selon les quatre phases prevues, et d'appliquer une adaptation legere sans opacite ni promesse excessive.

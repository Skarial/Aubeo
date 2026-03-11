# Cahier fonctionnel v1 - Aubeo

## 1. Objet du document

Ce document cadre la première version fonctionnelle d’Aubeo. Il décrit ce que la v1 doit couvrir, ce qu’elle exclut, les règles métier à rendre explicites et les hypothèses produit à valider avant toute extension.

## 2. Vision produit

Aubeo est une application mobile de réveil progressif. Sa logique centrale consiste à préparer l’éveil avant l’heure cible au lieu de concentrer toute l’expérience sur une sonnerie brutale à l’instant final.

## 3. Problème adressé

Une alarme classique déclenche le réveil sur un point unique et abrupt. Aubeo cherche à réduire cette rupture en proposant une montée progressive, lisible et paramétrable, sans prétendre analyser scientifiquement le sommeil ni produire un effet médical.

## 4. Objectif v1

Livrer un premier produit Android capable de :

- planifier un réveil à heure cible ;
- dérouler une séquence progressive en plusieurs phases ;
- permettre un réglage simple des principaux paramètres ;
- conserver un historique local minimal ;
- appliquer une adaptation légère, bornée et explicable.

## 5. Public cible

La v1 s’adresse en priorité à des utilisateurs qui :

- veulent un réveil moins abrupt qu’une alarme classique ;
- utilisent leur téléphone comme réveil principal ;
- acceptent de régler une heure cible et quelques paramètres simples ;
- recherchent une expérience crédible plutôt qu’un discours pseudo-scientifique.

## 6. Plateformes

- Android : plateforme cible de la v1.
- iOS : hors périmètre initial, à traiter plus tard.

## 7. Principes non négociables

- transition vers l’éveil, pas alarme brutale immédiate ;
- ordre fixe des phases : lumière -> vibrations douces -> ambiance sonore ou mode expérimental -> réveil final ;
- comportement compréhensible par l’utilisateur ;
- adaptation locale, légère, explicable et désactivable ;
- aucune promesse médicale ;
- aucun discours pseudo-scientifique sur le sommeil ;
- tout mode binaural ou assimilé reste présenté comme une option expérimentale, jamais comme un effet prouvé.

## 8. Séquence fonctionnelle du réveil

### 8.1 Déclenchement de la séquence

L’utilisateur définit une heure cible et une durée totale de préparation. Aubeo calcule un début de séquence avant l’heure cible et répartit les phases de réveil dans cette fenêtre.

### 8.2 Lumière

La lumière est la première phase. Son rôle est d’amorcer la transition vers l’éveil de façon douce et progressive. En v1, cette phase doit rester simple à comprendre et réglable en intensité maximale.

### 8.3 Vibrations douces

Les vibrations démarrent après la lumière. Elles doivent rester progressives, sans bascule brutale, et pouvoir être réglées dans une plage simple à comprendre.

### 8.4 Ambiance sonore ou mode expérimental

La phase sonore commence après les vibrations. Le mode par défaut repose sur une ambiance sonore progressive. Une variante expérimentale peut exister, à condition d’être clairement étiquetée comme expérimentale et de ne jamais être présentée comme scientifiquement prouvée.

### 8.5 Réveil final

Le réveil final se déclenche à l’heure cible si l’utilisateur n’a pas déjà arrêté la séquence. Il constitue le point de garantie de la v1.

## 9. Paramètres utilisateur v1

La v1 doit permettre au minimum :

- de définir une heure cible ;
- de définir une durée totale de préparation ;
- de choisir un profil de réveil ;
- d’ajuster l’intensité maximale de la lumière ;
- d’ajuster l’intensité maximale des vibrations ;
- d’ajuster le niveau maximal du son ;
- de choisir le mode sonore disponible ;
- d’activer ou désactiver l’adaptation légère.

## 10. Profils de réveil

Les profils de réveil v1 servent à proposer des réglages de départ simples, modifiables ensuite par l’utilisateur. Ils ne changent pas l’ordre des phases.

### 10.1 Profil doux

- préparation plus enveloppante ;
- montée plus progressive ;
- intensités finales modérées.

### 10.2 Profil standard

- profil par défaut ;
- équilibre entre anticipation, progression et intensité ;
- point de départ pour la majorité des usages.

### 10.3 Profil tonique

- progression plus marquée ;
- intensités finales plus franches ;
- usage destiné aux personnes qui veulent un réveil moins brutal qu’une alarme sèche, mais plus affirmé que le profil standard.

## 11. Lumière, vibrations et sons

### 11.1 Lumière

- premier canal de stimulation ;
- rôle préparatoire ;
- réglage simple en intensité maximale.

### 11.2 Vibrations

- deuxième canal ;
- rôle de relance douce après la lumière ;
- réglage simple en intensité maximale.

### 11.3 Sons

- troisième canal ;
- rôle d’accompagnement progressif avant le réveil final ;
- ambiance sonore comme mode de base ;
- mode expérimental explicitement présenté comme option non prouvée.

## 12. Interaction utilisateur

### 12.1 Avant le réveil

L’utilisateur configure son heure cible, sa durée de préparation, son profil et ses intensités principales.

### 12.2 Pendant la séquence

L’application doit permettre à l’utilisateur :

- de reconnaître qu’une séquence de réveil est en cours ;
- d’identifier la phase active ;
- d’arrêter la séquence lorsqu’il est réveillé.

### 12.3 Après le réveil

L’application peut demander un retour simple sur le ressenti du réveil afin d’alimenter l’historique et l’ajustement léger.

## 13. Feedback post-réveil

Le feedback post-réveil v1 doit rester très simple. Il peut reposer sur un retour court tel que :

- trop tôt ;
- bon moment ;
- trop tard.

Ce feedback reste facultatif pour l’utilisateur et ne doit pas compliquer la sortie du réveil.

## 14. Logique adaptative v1

La logique adaptative v1 repose uniquement sur des données locales, observables et compréhensibles.

### 14.1 Signaux pris en compte

- phase à laquelle la séquence a été arrêtée ;
- moment d’arrêt par rapport à l’heure cible ;
- éventuel feedback post-réveil.

### 14.2 Règle d’ajustement

- si l’utilisateur arrête régulièrement la séquence très tôt, Aubeo peut réduire légèrement l’anticipation ;
- si l’utilisateur atteint régulièrement le réveil final ou juge le réveil trop tardif, Aubeo peut avancer légèrement le début de la préparation ;
- si les signaux sont contradictoires, aucun ajustement automatique n’est appliqué.

### 14.3 Garde-fous

- adaptation bornée ;
- variation légère d’un jour à l’autre ;
- visibilité du réglage actif ;
- retour possible au réglage manuel de référence ;
- aucune décision opaque.

## 15. Historique

La v1 conserve un historique local minimal des réveils afin de :

- rendre les réveils passés consultables ;
- alimenter la logique adaptative ;
- donner un retour simple à l’utilisateur sur son usage récent.

L’historique n’a pas vocation à devenir un tableau de bord médical.

## 16. Parcours utilisateur

### 16.1 Premier cadrage

1. l’utilisateur ouvre l’application ;
2. il définit une heure cible ;
3. il choisit une durée de préparation ;
4. il sélectionne un profil ;
5. il ajuste si besoin les intensités principales ;
6. il active le réveil.

### 16.2 Réveil nominal

1. la phase lumière démarre ;
2. les vibrations douces prennent le relais ;
3. l’ambiance sonore ou le mode expérimental démarre ;
4. l’utilisateur arrête la séquence s’il est réveillé ;
5. sinon, le réveil final se déclenche à l’heure cible.

### 16.3 Après le réveil

1. l’application enregistre le résultat localement ;
2. elle peut demander un feedback court ;
3. elle met à jour l’historique et l’éventuel ajustement léger.

## 17. Écrans v1

La v1 doit au minimum prévoir :

- un écran principal avec le prochain réveil ;
- un écran de réglage du réveil ;
- un écran ou bloc de choix du profil ;
- un écran de séquence active ;
- un écran ou bloc de feedback post-réveil ;
- un écran d’historique simple.

## 18. Données fonctionnelles à stocker

En local, la v1 doit pouvoir stocker :

- heure cible ;
- durée totale de préparation ;
- profil sélectionné ;
- intensités maximales par canal ;
- mode sonore choisi ;
- état de l’adaptation légère ;
- historique des réveils ;
- feedback post-réveil s’il existe ;
- réglage manuel de référence utilisé pour revenir à un comportement stable.

## 19. Règles métier v1

- la séquence doit toujours se terminer au plus tard à l’heure cible ;
- l’ordre des phases est fixe ;
- le réveil final ne doit pas être sauté tant que l’utilisateur n’a pas explicitement arrêté la séquence ;
- les profils n’autorisent pas d’inversion des phases ;
- le mode expérimental doit être identifiable comme tel ;
- l’adaptation ne doit jamais modifier brutalement le comportement ;
- l’utilisateur doit pouvoir revenir à un réglage manuel stable ;
- l’historique reste local dans la v1.

## 20. Exclusions de périmètre

Sont exclus de la v1 :

- version iOS ;
- synchronisation cloud ;
- fonctions sociales ou communautaires ;
- objets connectés externes ;
- analyse de cycles du sommeil ;
- promesses de santé ou de bien-être médical ;
- automatisations opaques ;
- discours présentant un mode binaural comme scientifiquement validé.

## 21. Critères de succès

La v1 remplit son rôle si :

- l’utilisateur comprend la promesse produit dès la lecture ou le premier réglage ;
- la séquence progressive est perçue comme ordonnée et lisible ;
- le réveil final reste garanti à l’heure cible ;
- l’adaptation légère reste compréhensible ;
- l’historique et le feedback ajoutent de la valeur sans alourdir l’expérience.

## 22. Risques fonctionnels

- trop de réglages peuvent compliquer le premier usage ;
- une adaptation trop discrète peut paraître inutile ;
- une adaptation trop visible peut paraître arbitraire ;
- le mode expérimental peut être mal compris s’il n’est pas clairement encadré ;
- un historique trop détaillé pourrait faire dériver le produit vers un faux discours d’analyse du sommeil.

## 23. Hypothèses produit à valider

- une transition par phases est perçue comme préférable à une alarme unique ;
- trois profils simples suffisent à couvrir les besoins initiaux ;
- un feedback post-réveil court est acceptable ;
- une adaptation légère et explicable est comprise comme utile ;
- le libellé expérimental suffit à éviter une lecture pseudo-scientifique des options sonores.

## 24. Priorisation v1

### Priorité indispensable

- heure cible ;
- durée de préparation ;
- séquence progressive complète ;
- arrêt utilisateur ;
- réveil final ;
- réglages essentiels ;
- cadrage clair du mode expérimental.

### Priorité importante

- profils de réveil ;
- historique local ;
- feedback post-réveil ;
- adaptation légère désactivable.

### Priorité différable

- enrichissements non essentiels de personnalisation ;
- extension iOS ;
- variantes secondaires au-delà du socle MVP.

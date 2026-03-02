# hackathon-2025-26 — LaRéponse

## Contexte du projet

LaRéponse est le nouveau nom de la structure précédemment connue sous “Hex Makina”. Le projet combine une position philosophique (ne pas mentir sur la complexité, rendre la structure visible) et une offre de services numériques (sites, portails, automatisations). Pour le hackathon, l’enjeu est de transformer un corpus de textes déjà fournis (manifesto, ethos, tarifs, méthode, brief logo) en un site vitrine lisible, crédible et orienté conversion.

Le point clé transversal est une exigence **mobile-first** : le contenu est dense, donc la hiérarchie, le rythme de lecture, et la clarté des CTA doivent être pensés d’abord pour écran étroit. Le desktop vient ensuite.

## URLs et structure actuelle (référence technique)

À ce stade, il n’y a pas de site “existant” imposant une charte ou des gabarits à respecter. On est donc dans un cas “création”, avec une marge de proposition élevée, mais avec une contrainte forte : rester **minimal**, **rapide**, et **cohérent** avec la thèse (structure visible, pas de décor gratuit).

À compléter côté équipe au démarrage :

* URL de déploiement (GitHub Pages / domaine)
* arborescence finale (one-page vs multi-pages)
* repères techniques (stack retenue, contraintes d’hébergement, solution de contact)

## Objectif général

Produire en 3 jours une vitrine web qui explique clairement **“ce qu’est LaRéponse”** et qui déclenche l’action (**prise de contact / demande de devis**), sans ambiguïté sur la méthode et les limites (périmètre de la garantie, exclusions, conditions des projets lucratifs). Le site doit incarner la promesse : simplicité radicale, structure exposée, et absence de complexité artificielle.

## Cohérence globale (valable sur tout le site)

* **Priorité mobile-first** : largeur de texte contrôlée, paragraphes courts, intertitres fréquents, encadrés pour les règles, navigation simple.
* **Lisibilité avant style** : la mise en forme doit “révéler la structure” (sommaire, sections nettes, repères), pas l’habiller.
* **Crédibilité et cadrage** : la promesse “garantie à vie” doit être formulée de manière strictement cadrée (conditions, exclusions, périmètre).
* **Accessibilité** : focus visible, contrastes solides, navigation clavier, structure HTML sémantique, ARIA seulement si nécessaire.
* **Performance** : page légère (CSS minimal, peu de JS), images optimisées, pas d’animations lourdes, pas de dépendances inutiles.

## Pages / sections recommandées (structure cible)

Le dossier peut être traité comme un site en **4 à 6 sections (one-page)** ou **4 à 6 pages**. Sections minimales recommandées :

### Accueil (promesse + CTA)

Le haut de page doit donner immédiatement : (1) la thèse en une phrase, (2) ce qu’ils font concrètement, (3) le prochain pas (contact). Il faut deux CTA : “Décrire mon besoin” et “Voir la méthode”.

**Livrable attendu** : hero mobile-first + 2 CTA + 3 preuves courtes (ex. 30 jours, jamais deux fois facturé, accessibilité).

### Manifeste (thèse, éditorialisée pour le web)

Le texte “Reality is complex…” est dense mais central. Il doit être éditorialisé : phrases groupées, intertitres, et mise en avant de la règle (“do not lie about complexity”). Option utile : un résumé court au-dessus, puis la version complète dessous.

**Livrable attendu** : page/section manifeste lisible sur mobile, avec hiérarchie claire.

### Méthode (30 jours, garantie, limites)

Section critique : phase facturable, validation 30 jours, garantie/mise à jour “à vie” dans le périmètre, et **exclusions** “fair & square”. Il faut un bloc “ce qui est inclus” et un bloc “ce qui ne l’est pas”.

**Livrable attendu** : schéma en 4 étapes + encadré exclusions + formulation non ambiguë.

### Tarifs (grille + projets lucratifs)

La table doit être **responsive** : sur mobile, éviter les tables larges (cartes empilées ou table scrollable). Expliquer clairement “crédits prépayés, débités à la minute”. La section “projets générateurs de revenus” doit être séparée et explicite (minimum mensuel **ou** % CA, jamais cumulés, facturé au plus élevé).

**Livrable attendu** : rendu mobile robuste + explication courte + section e-commerce.

### Services (ce que nous faisons, concret)

Traduire “What” en offres compréhensibles : sites vitrines, portails, e-commerce, automatisations, crawlers/parsers, traitement documentaire, systèmes de reporting. Chaque item doit dire **le bénéfice** (pourquoi c’est utile), pas seulement le nom.

**Livrable attendu** : 6 cartes services maximum, orientées bénéfices.

### Projets (écosystème, preuve de méthode)

Section “inventaire” : montrer que LaRéponse fabrique des outils parce que le réel le demande. Objectif : crédibilité (ingénierie), cohérence (thèse), et projection (voici ce qu’on peut réutiliser / adapter).

Format recommandé : 5 à 7 cartes, chacune avec **Pourquoi / Pour qui / Ce que c’est / Statut**, et une ligne **Étymologie** (le nom porte la thèse). Sur mobile : cartes empilées, intertitres courts, pas de pavés.

**Livrable attendu** : une section Projets lisible et actionnable (CTA secondaire “Voir la méthode” / “Décrire mon besoin”).

#### BADHAT

* Pourquoi : ne plus travestir le réel derrière des abstractions commodes. BADHAT naît d’un métier pratiqué depuis vingt-cinq ans, entre contraintes corporate et exigences associatives : livrer, maintenir, répondre, sans ajouter de poids inutile. La thèse est simple : la complexité existe ; on peut la rendre visible, traçable, assumable.
* Pour qui : développeurs qui privilégient la causalité à la doctrine, la lecture au “setup”, l’imputable au magique. Profils sensibles à la performance, à la stabilité et à l’architecture “à plat” ; équipes qui veulent un socle petit, maîtrisé, et compatible avec des outils standards (serveur web, OS, PDO, PHPUnit…).
* Ce que c’est : un noyau PHP minimal qui fait trois gestes — fiabiliser un chemin (hook), le résoudre en fichier (seek), exécuter proprement (loot) — puis émettre une réponse HTTP. Le système de fichiers tient lieu de carte ; chaque route est un fichier ; un fichier peut retourner une valeur, mieux, une closure qui capture l’intention. Les décisions d’exécution sont portées par bitmasks (un entier lisible au call-site), et l’échec est explicite (pas de faux silencieux). Autour du noyau : modules “plomberie” (http, pdo, auth, csrf, rfc, trap) sans prétendre remplacer des briques mûres.
* Statut : socle utilisable, volontairement réduit ; progression lente et disciplinée. Projet de terrain, affiné par itérations, destiné à servir de base à des livraisons réelles.
* Étymologie : “Bits Are Decisive. HTTP As Terminal.” Le nom associe le bit (décision explicite, imputable) et HTTP (frontière réelle, sortie). “Hat” rappelle le trompe-l’œil : ce qui ressemble à un chapeau peut cacher un éléphant ; BADHAT refuse de masquer la masse sous une forme rassurante.

#### Dashbored

* Pourquoi : parce que beaucoup d’outils promettent une structure “déjà là”, puis finissent par figer le vivant. Les workflows changent, les mots glissent, les relations se recomposent ; l’outil, lui, durcit et devient obstacle. Dashbored part du doute : la structure se gagne par l’usage, et ce qui ne survit pas au réel ne mérite pas d’être permanent.
* Pour qui : collectifs, associations, petites équipes, et travailleurs du savoir qui construisent en avançant. Contextes où l’on explore avant de conclure, où l’on doit garder l’ambiguïté visible, et où l’on refuse les systèmes qui “décident à votre place” au nom du confort.
* Ce que c’est : un environnement de pensée, pas une surface de reporting. Il autorise les structures provisoires, les regroupements faibles, les liens inachevés. Les motifs ne sont promus que s’ils se répètent, se stabilisent, et résistent à plusieurs points de vue. Dashbored refuse d’être un CRUD/CMS/form-first, refuse les mutations silencieuses du modèle, et préfère l’intention explicite à l’automatisation opaque. Des contraintes assumées (vocabulaire limité d’actions/relations, charge visuelle contenue) servent d’hygiène cognitive : éviter l’entropie, forcer le sens à remonter.
* Statut : manifeste solide et direction produit claire ; base conceptuelle prête à être prototypée dès qu’un cas d’usage “long” s’y prête.
* Étymologie : mot-valise : “dashboard” retourné contre lui-même, et “bored” (lassé). Le “dash” reste (le trait, la poussée), mais la “board” cesse d’être un panneau de contrôle : c’est une planche de travail, provisoire et reconfigurable.

#### DunDun

* Pourquoi : rétablir une discipline d’exécution sans calendrier, sans tableaux culpabilisants, sans notifications qui fragmentent. DunDun traite le travail comme un rythme : un battement après l’autre, avec une structure minimale qui empêche la fuite en avant.
* Pour qui : personnes qui veulent agir sur mobile sans se perdre dans l’arrière-plan, et équipes qui ont besoin de voir les ruptures plutôt que de les camoufler. Utile quand la friction principale n’est pas “manque d’outils”, mais surcharge cognitive et dispersion.
* Ce que c’est : des séquences linéaires à pointeur, composées de tâches, chaque tâche générant trois slots obligatoires (Préparer → Faire → Clore). Une règle globale : un seul slot actif par utilisateur. Si un slot bloque, on l’éjecte vers l’Inbox — mais un ghost reste à sa place : la cassure est visible, donc analysable. Le téléphone est un “remote d’exécution” (un écran, un slot, timer, actions simples), sans vue backlog ; le desktop est le “métier à tisser” : Inbox (captures + éjectés), remaillage (rethread/split/fork/swap/defer), vue des fractures et de leurs causes (temps, personnes, dépendances, énergie), signaux de pression (surtemps, goulots, vieillissement).
* Statut : spécification détaillée (objets, règles, états, UX phone/desktop) ; concept prêt pour un MVP fonctionnel.
* Étymologie : “done and done”. Deux coups, deux clôtures. Le nom encode la mécanique centrale : terminer une unité, puis enchaîner la suivante sans backlog mental. Onomatopée de finition, pas de planification.

#### tenpoken

* Pourquoi : pratiquer le temps plutôt que le dompter. Tenpoken refuse la fiction de la maîtrise totale (agenda) comme celle du récit rétrospectif (journal). Il propose un geste : encoder le moment, puis le laisser respirer, afin que des patterns apparaissent sans contrainte. Le drift — l’écart entre plan et occurrence — devient instrument de vérité.
* Pour qui : profils qui cherchent une précision calme : créatifs, indépendants, personnes sensibles au bruit, ou toute personne qui veut une discipline légère sans taxonomie, sans objectifs imposés, sans “productivité performative”.
* Ce que c’est : une structure réduite à quelques couches (Event, Now, Window, Drift). Aucun projet, aucune catégorie, aucun tag : seulement des événements et des états (potentiel, attendu, planifié, survenu, résolu). Interaction doctrine stricte : navigation par fenêtres (heure/jour/semaine), pas de scroll infini, peu d’actions, peu de taps. Mobile pour encoder en mouvement ; desktop pour observer le drift, relire par fenêtres, et marquer la résolution (hygiène de clôture). Identité : géométrie sobre, neutrals + un accent signal, typographie mono/semi-mono, un symbole simple “temps en mouvement”.
* Statut : doctrine d’usage et identité déjà posées ; base solide pour une application minimaliste.
* Étymologie : dérive de *tenpo ken* (toki pona) : “temps possible”, “temps en puissance”. “Tenpo” pose le temps comme matière ; “ken” pose la possibilité. Le nom conserve une étrangeté utile : il appelle une pratique.

#### JDAD (JSON Data And Directions)

* Pourquoi : cesser de confondre donnée et navigation dans les APIs, et faire payer ce mélange en parsing, en mémoire, en latence, et en confusion. JDAD propose un geste net : séparer le plan dénotatif (records) du plan connotatif (affordances), pour que l’hypermedia redevienne optionnelle et proportionnée au besoin.
* Pour qui : équipes API et clients mobiles/contraints (IoT, edge, réseaux lents) qui veulent un format prédictible, peu profond, et facilement validable. Contexte typique : beaucoup de lecture “simple” et, ponctuellement, besoin de navigation/permissions/transitions — sans devoir tout décoder à chaque réponse.
* Ce que c’est : un format JSON où `_` est le signifiant de la connotation : soit une URI vers une hyperdoc (mode data-only), soit une table de liens/transitions (mode hyper-only), soit un document combiné. Les collections sont des buckets indexés par IDs, et les relations sont des références directes `["collection", id…]` traversables en temps constant. La grammaire est outillée par des schémas JSON-Schema, des routines de détection et de résolution, et un media type `application/jdad+json`.
* Statut : spécification avancée (schémas, exemples, ébauche de client, évaluation de perf) ; draft sérieux, prêt à être consolidé en outillage (validateurs, CI, générateurs) si adopté.
* Étymologie : triple lecture. (1) Acronyme : “JSON Data And Directions”. (2) Jeu “JSON / dad” : la discipline posée sur JSON, pour le rendre lisible, stable, validable. (3) Jeu “dad / son” : “data” comme parent (ce qui demeure), “directions” comme enfant (ce qui se propose) ; liés, mais non confondus.

#### KORAL

* Pourquoi : répondre à un besoin CRM concret, façonné par le terrain : suivi de clients, services rendus, sessions, notes, travailleurs, items, et la nécessité de relier ces éléments sans lourdeur. Koral vise l’utile avant le prestige, et l’adaptation avant le prêt-à-porter.
* Pour qui : structures qui veulent un CRM sur mesure, maintenable en PHP, et aligné sur leurs pratiques — souvent petites organisations, métiers de service, et contextes associatifs où les processus réels ne rentrent pas dans une grille SaaS.
* Ce que c’est : une application CRM construite sur Kadro (framework MVC interne) : routing (AltoRouter), templating (Smarty), container PSR-11, logs PSR-3, ORM PDO, auth/permissions/ACL, i18n. Koral apporte la couche métier : planification (journaliers/planners), suivi de sessions, gestion de notes avec associations client/item, affectation de travailleurs. L’architecture compose les comportements des contrôleurs via un système de traits (“Traitor”) qui injecte des étapes de détection de contexte (client, service, session, items). Le tout suit une approche convention-over-configuration (noms de classes ↔ routes ↔ tables).
* Statut : application existante, sous licence MIT, en maintenance/évolution avec son socle Kadro.
* Étymologie : KORAL est un nom court, mémorisable, et un acronyme opératoire : “KOLLECTO · RAPPORTO · LISTO”. Trois verbes-outils : collecter sans forcer, relier pour rendre imputable, tenir une liste praticable.

### Contact (conversion)

Formulaire minimal (si possible) ou mailto propre. Micro-texte rassurant (ce qu’il faut fournir, délai de réponse). CTA final visible.

**Livrable attendu** : section contact efficace + validation basique + anti-spam simple si formulaire.

### Logo / identité (optionnel)

Si nécessaire, une section “Logo” reprenant le brief interrobang (‽) et des déclinaisons attendues (favicon, monochrome, petite taille).

**Livrable attendu** : page courte utilisable par un graphiste et par l’équipe UI.

---

# LaRéponse — Informations fournies par le client

Ce dépôt regroupe les documents fournis par l’équipe **LaRéponse**, traduits intégralement en français et normalisés en **Markdown** pour une lecture et une utilisation sur GitHub.

---

## Sommaire

- [1) Manifeste](#1-manifeste)
- [2) Grille tarifaire et philosophie de travail](#2-grille-tarifaire-et-philosophie-de-travail)
- [3) Ethos](#3-ethos)
- [4) Présentation synthétique](#4-présentation-synthétique)
- [5) Brief design — Logo “La Réponse”](#5-brief-design--logo-la-réponse)

---

# 1) Manifeste

## LA RÉPONSE — Manifesto

La réalité est complexe, et tout ce qui prétend le contraire ne fait que déplacer cette complexité vers un fardeau caché, une perte d’agence, et un pouvoir sans responsabilité.

Ce qui dissimule sa complexité ment sur lui-même, exigeant la confiance plutôt que la compréhension ; c’est une forme de coercition.

La clarté n’est pas la simplicité, mais l’exposition véridique de la structure.

Le minimalisme n’est pas une réduction, mais un refus : le refus de masquer ce qui fait fonctionner une chose.

Les formes humaines acceptent les limites humaines, tandis que les formes qui exigent l’adaptation — au lieu de rencontrer les personnes là où elles sont — exportent leur coût.

Quand l’effort est supprimé avant la compréhension, l’autonomie s’effondre en dépendance ; et la facilité sans lisibilité affaiblit celles et ceux qui s’y appuient.

Une transmission qui lisse la structure produit de la conformité, non de la compréhension ; comprendre exige une résistance.

Le pouvoir croît là où la structure disparaît ; rendre la structure visible devient alors un acte de résistance.

Celles et ceux qui façonnent les choses sont responsables non seulement des résultats, mais de ce qu’ils cachent, car il n’y a pas de neutralité là où la forme dirige le comportement.

LaRéponse est une discipline avec une règle unique, non négociable : **ne pas mentir sur la complexité**.

Ce qui est visible peut être questionné ; et ce qui peut être questionné peut être changé.

---

# 2) Grille tarifaire et philosophie de travail

## Grille tarifaire

Je travaille avec une **grille de tarifs transparente** et une **philosophie claire** :

- Vous payez une seule fois pour la mise en œuvre et les **30 premiers jours d’utilisation réelle**.
- Au-delà, le travail est **garanti et mis à jour à vie**, sans jamais être refacturé.

Tous les travaux sont réalisés contre **crédits prépayés**, débités **à la minute**.

### Tarifs horaires

| Tarif | Quand |
|------:|------|
| **37 €/h — Coup de pouce** | Projets sociaux, associatifs ou non lucratifs |
| **73 €/h — Standard** | Lun–Ven, 09:00–19:00 (heures normales) |
| **96 €/h — Étendu** | Samedi, 09:00–19:00 |
| **127 €/h — Urgence** | Nuits (19:00–09:00), dimanches, jours fériés |
| **301 €/h — Vacances** | Périodes de congés annoncées *(1 client = 3 personnes privées de vacances)* |

---

## Philosophie de travail

### Phase facturable
La mise en œuvre et les corrections pendant les **30 premiers jours** sont facturées **à la minute**.

### Validation de 30 jours
Une fois qu’un livrable fonctionne correctement pendant **30 jours** en conditions normales, il est considéré comme **validé**.

### Garantie à vie
Après validation :

- **Garanti à vie** : si le travail échoue à cause de mon implémentation, je le corrige gratuitement.
- **Mis à jour à vie** : si votre environnement évolue (serveur, CMS, PHP), j’adapte gratuitement le livrable, tant que cela reste dans mon périmètre.
- **Jamais deux fois facturé** : vous ne paierez plus jamais pour ce même livrable.

### Exclusions (fair & square)
Ne sont pas couverts :

- Changements de navigateurs (Chrome, Safari, etc.)
- Logiciels ou plugins tiers
- APIs externes
- Migrations d’hébergement
- Modifications côté client
- Nouvelles fonctionnalités ou évolutions

Si l’un de ces éléments casse un livrable existant, cela constitue un **nouveau travail**.

---

## Cas des projets générateurs de revenus

Pour les sites e-commerce, systèmes de réservation ou plateformes d’abonnement, les règles sont différentes :

- Un **minimum mensuel garanti** (ex. 500 € HT)
- **ou** un **% du chiffre d’affaires en ligne** (ex. 3 %)
- **Jamais les deux cumulés** : le montant facturé est toujours le **plus élevé** des deux.

Ainsi, mes intérêts sont alignés sur les vôtres :

**plus votre activité en ligne réussit, plus je gagne — et plus je suis investi dans sa réussite.**

---

## En résumé

- **Projets non lucratifs** : “Payez une fois. Validé en 30 jours. Gratuit à vie.”
- **Projets lucratifs** : “Un minimum mensuel ou un pourcentage du chiffre d’affaires — jamais les deux.”

---

# 3) Ethos

## Notre Ethos

- **Accessibilité d’abord** : tout ce que nous construisons vise à inclure, pas à exclure.
- **Responsabilité écologique** : minimiser le gaspillage, concevoir pour durer.
- **Accessibilité financière et transparence** : prix justes, pas de coûts cachés.
- **Simplicité et minimalisme** : solutions sobres, sans complexité inutile.
- **Renforcement communautaire** : consolider les réseaux, partager outils et soutien.
- **Éducation comme croissance** : apprendre vient naturellement quand les fondations sont posées.

---

# 4) Présentation synthétique

# { la réponse } — Simplicité radicale, garantie à vie

> Un code n’est pas une marchandise jetable.  
> C’est une structure logique, reproductible, attestable.  
> Une fois comprise, corrigée et testée, elle ne se défait plus.

---

## Who — Qui nous sommes

Nous sommes des praticiens du minimalisme fonctionnel.  
Notre rôle n’est pas de vendre des heures, mais de livrer des systèmes stables et transmissibles.

Un système n’a pas besoin d’être massif pour être robuste.  
Il doit être clair, proportionné et régi par des règles simples.

Nous refusons :

- les dépendances fragiles,
- la facturation de la répétition,
- les couches inutiles qui gonflent les devis.

Nous affirmons qu’un travail bien fait s’honore par sa **durabilité**,  
et non par la multiplication des factures.

---

## What — Ce que nous faisons

Nous concevons et déployons :

- sites, portails et plateformes cohérents,
- outils calibrés pour indépendants, associations et petites structures,
- architectures sobres et stables, conçues pour durer sans dette cachée.

Chaque livrable est accompagné de ses **tests automatisés**.  
Chaque bug est corrigé **une seule fois**.  
Chaque correction devient un **acquis irréversible**.

---

## How — Comment nous travaillons

Notre philosophie s’inspire de **BADHAT** :

- déléguer chaque responsabilité au niveau le plus efficace (serveur, base, code),
- supprimer tout décor, toute complexité arbitraire,
- optimiser l’exécution en respectant la logique des machines.

LaRéponse en est l’application pratique :

- **jamais deux fois facturé** pour le même travail,
- une **période de stabilisation** de trente jours,
- puis une **garantie illimitée** tant que le bug est reproductible.

Si le test échoue, nous réparons.  
Si le test réussit mais qu’un problème survient,  
c’est un **nouveau contexte** — et donc un **nouveau travail**.

---

## Whom — Pour qui

Nous travaillons pour celles et ceux qui refusent le gaspillage.  
Pour celles et ceux qui veulent un code clair, éprouvé, transmissible.  
Pour celles et ceux qui savent que la valeur ne se mesure pas au volume,  
mais à la justesse qui demeure.

---

# 5) Brief design — Logo “La Réponse”

## 5.1 Aperçu du projet

La Réponse est un collectif philosophique et créatif explorant l’équilibre entre question et vérité, émerveillement et clarté, réflexion et révélation.

Le logo doit capturer cette dualité : la fusion de l’interrogation et de l’affirmation, à travers l’essence symbolique de l’**interrobang** (‽), traité non comme un caractère typographique, mais comme un concept central.

---

## 5.2 Objectif

Concevoir un symbole visuel qui représente le noyau de La Réponse : une forme où le point d’interrogation et le point d’exclamation coexistent dans une synthèse abstraite, harmonieuse et poétique.

Ce symbole doit être :

- immédiatement reconnaissable comme un signe unique, unifié,
- capable de tenir seul comme monogramme ou emblème (sans texte),
- porteur de profondeur, de curiosité, et d’une révélation calme — pas de bruit, pas d’urgence.

---

## 5.3 Direction visuelle

### Focus conceptuel

Le logo incarne l’interrobang comme un **état métaphysique**, pas comme un caractère.

Le penser comme une **graine**, une **colonne**, ou un **pouls** : deux forces convergent.

Le symbole doit exprimer résonance, équilibre, et tension intentionnelle.

### Langage formel

- **Trait** : propre, continu, délibéré — des courbes organiques rencontrant des axes structurés.
- **Géométrie** : ancrée dans des proportions naturelles (ratio d’or ou espacement harmonique).
- **Contraste** : tension entre la courbe (enquête) et la verticalité (affirmation).
- **Symétrie** : légèrement imparfaite — plus vivante que mécanique.

### Ton émotionnel

- philosophique, pas corporate,
- calme, intelligent, intemporel,
- à l’aise autant dans un livre de philosophie que gravé sur un objet tech minimaliste.

---

## 5.4 Style et esthétique

| Élément | Direction |
|--------|-----------|
| Palette | Noir / indigo profond sur fond ivoire ou blanc cassé |
| Support | Vectoriel (line art), texture possible pour l’impression |
| Typo | Pas nécessaire dans le symbole. Le mot “La Réponse” peut être associé séparément (serif ou sans humaniste) |
| Négatif | Intégré à la forme : l’air et le silence définissent le glyphe |
| Références d’humeur | Ensō zen, logotypes Frutiger, calligraphie de Bruno Munari, géométries de Hilma af Klint, lumière de Soulages |

---

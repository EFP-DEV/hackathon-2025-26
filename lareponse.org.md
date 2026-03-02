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

### Contact (conversion)

Formulaire minimal (si possible) ou mailto propre. Micro-texte rassurant (ce qu’il faut fournir, délai de réponse). CTA final visible.

**Livrable attendu** : section contact efficace + validation basique + anti-spam simple si formulaire.

### Logo / identité (optionnel)

Si nécessaire, une section “Logo” reprenant le brief interrobang (‽) et des déclinaisons attendues (favicon, monochrome, petite taille).

**Livrable attendu** : page courte utilisable par un graphiste et par l’équipe UI.

## Contenu

# LaRéponse — Dossier (Hackathon) — Version GitHub

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

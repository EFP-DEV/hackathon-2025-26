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

## Contraintes de contenu (à respecter)

Le contenu fourni est hétérogène (FR + EN) et partiellement redondant. Le travail attendu est une **consolidation éditoriale** : supprimer les doublons, harmoniser la langue (ou organiser en FR/EN), et faire ressortir une structure nette. Le site ne doit pas être un “dump” de texte ; il doit guider la lecture.

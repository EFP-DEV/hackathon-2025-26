## Contexte du site actuel

Le hackathon porte sur Dogitech.be, site vitrine d’une entreprise locale (plomberie, électricité, petits travaux). Le cœur du projet n’est pas une plateforme complexe mais un outil de conversion et de confiance : rassurer, clarifier l’offre, et faciliter la prise de contact.

Le point clé transversal est une exigence mobile-first : la plupart des demandes viennent du smartphone, souvent dans un contexte de stress (panne, fuite, coupure). L’UX doit privilégier l’accès immédiat aux informations utiles et à l’action.

## Identité et positionnement (Nicolas Dogiment)

Dogitech, c’est Nicolas Dogiment : un travailleur “à l’ancienne”. Très compétent, fiable, honnête, orienté action et service. Il préfère la solution concrète au discours. Son style peut être un peu bourru, mais c’est du bon sens : direct, sans détour, sans bullshit. C’est son créneau et sa différence.

Promesse centrale : sympa, compétent, fiable — avec un ton franc et des preuves (résultats, transparence, conformité).

## URLs et structure cible (référence technique)

Le site n’est pas décrit comme déjà structuré. Pour le dossier hackathon, on propose une arborescence simple (à adapter) :

* Homepage (accroche + accès rapide urgence / services)
* Services (liste) + pages service (plomberie / électricité / petits travaux)
* Tarifs / transparence (ou section intégrée aux pages service)
* Réalisations / avant-après (preuves concrètes)
* Contact (formulaire + infos + zones couvertes)
* Mentions / RGPD (simple et conforme)

À compléter côté équipe au démarrage : URLs finales, et repérage des blocs communs (header, footer, CTA).

## Objectif général

Construire une vitrine “artisan local” très lisible sur mobile, qui transforme. DogiTech doit être perçu comme fiable, clair, propre, et conforme (sécurité, normes), avec une promesse réaliste : intervention soignée, prix juste, et devis transparent.

Cible en 3 jours : un site opérationnel avec un parcours court vers le contact, des pages services structurées, et des preuves (réalisations + avis si disponible).

## Cohérence globale (valable sur tout le site)

Priorité mobile-first : CTA “Appeler” et “Demander un devis” visibles et accessibles, lisibilité maximale, interactions tactiles simples.

Ton “direct mais respectueux” : microcopy courte, utile, parfois sèche, jamais agressive. On assume le franc-parler comme gage de sérieux.

Preuves > promesses : cas concrets, avant/après, “ce qu’on fait / ce qu’on ne fait pas”, transparence, conformité.

Impact structurel limité : gabarits simples et répétables, composants légers, contenu robuste (même si incomplet ou variable).

## Guidelines de rédaction (microcopy)

Phrases courtes, vocabulaire simple, pas de superlatifs, pas de marketing.

Exemples :

* “On regarde. On explique. On répare.”
* “Devis annoncé avant intervention.”
* “Si c’est urgent : appelez. Sinon : décrivez, on rappelle.”
* “Travail propre. Normes respectées.”

À éviter : “leader”, “innovation”, “sur-mesure”, “excellence”, “satisfaction garantie”.

## Homepage (accès direct, réassurance)

La homepage sert de hub mobile : comprendre en 5 secondes ce que fait DogiTech et quoi faire maintenant.

Exigences UX :

* Deux entrées principales : “Urgence / dépannage” et “Installation / rénovation”
* CTA visibles (appel + message)
* Blocs de réassurance : zones, délais réalistes, devis avant intervention, conformité/sécurité
* Accès rapide aux 3 familles de services + liens vers tarifs et réalisations

Livrable attendu : maquette mobile-first + hiérarchie des blocs + version implémentable simplement.

## Pages services (offre lisible + transparence)

Chaque service doit être une page claire et répétable (même gabarit) :

* Problèmes typiques (ex : fuite, disjoncteur, prise, robinet, etc.)
* Ce que DogiTech fait concrètement (étapes)
* Fourchette de prix indicative + ce qui est inclus
* Ce qui peut faire varier le prix (cas réels)
* CTA contact pré-rempli (service sélectionné)

Livrable attendu : gabarit “service” réutilisable + 3 pages remplies (plomberie, électricité, petits travaux).

## Réalisations / avant-après (preuves concrètes)

Objectif : prouver le “travail soigné” avec du concret.

Contraintes :

* Fonctionne même avec peu de contenu (3 à 6 cas)
* Mobile-first : cartes empilées ou carrousel simple
* Légendes utiles : contexte, durée, solution, ordre de grandeur du coût (si acceptable)

Livrable attendu : page réalisations + composant avant/après simple.

## Tarifs / transparence (cadre honnête)

Le site doit cadrer les attentes et éviter la “surprise”.

Contenus recommandés :

* Ce qui est inclus (déplacement, diagnostic, main d’œuvre, fournitures)
* Ce qui varie (urgence, accessibilité, vétusté, pièces, mise aux normes)
* “Ce qu’on ne fait pas” (cadre honnête : pas de bricolage dangereux, pas de promesses impossibles)

Livrable attendu : page (ou sections) de transparence tarifaire intégrables aux pages services.

## Contact (friction minimale + anti-spam simple)

Point de conversion principal.

Exigences :

* Formulaire court : nom, téléphone/email, type d’intervention, code postal, message
* Validation temps réel + erreurs explicites
* Option “urgence” (si cochée : conseils + incitation à appeler)
* Anti-spam léger (honeypot + délai minimal) sans CAPTCHA lourd

Livrable attendu : page contact + composant formulaire réutilisable + confirmation (message ou email selon périmètre).

## Outil “cheap / fast / good” (cadrage d’attentes)

Module interactif pour illustrer le triangle des contraintes projet :

* L’utilisateur choisit deux options (cheap / fast / good)
* La troisième est “sacrifiée” et une explication apparaît
* Exemples concrets liés au métier (dépannage urgent vs rénovation planifiée)

Livrable attendu : composant interactif simple (HTML/CSS/JS) intégrable homepage et/ou tarifs.

## Résumé opérationnel pour les étudiants

Ce dossier n’est pas une refonte “branding”. Il impose :

1. Mobile-first strict (urgence, lisibilité, CTA, contact).
2. Une identité assumée : Nicolas, franc, très compétent, fiable, orienté action.
3. Des chantiers à fort ROI en 3 jours :

* Homepage : compréhension immédiate + accès urgence/services + réassurance.
* Pages services : gabarit unique, contenu concret, transparence.
* Réalisations : preuves rapides, avant/après simple.
* Contact : formulaire court, validation, anti-spam léger, confirmation.
* Module “cheap/fast/good” : interaction simple pour cadrer les attentes.

Résultat attendu : un site vitrine cohérent, maintenable, mobile-first, avec un parcours de conversion évident et des gabarits réutilisables.

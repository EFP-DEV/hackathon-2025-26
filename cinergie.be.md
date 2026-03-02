# hackathon-2025-26 — Cinergie
## Contexte du site actuel

Le hackathon porte sur Cinergie.be, avec un site déjà en production et une charte graphique existante à respecter. L’équipe a une marge de proposition sur certaines pages (notamment la homepage), mais le cadre impose de limiter les répercussions structurelles sur les autres pages du site : on évite les refontes globales de gabarits ou de composants partagés.

Le point clé transversal est une exigence mobile-first : les choix UX/UI et les arbitrages de dev doivent être centrés sur l’usage mobile (lecture, navigation, repères, feedback), le desktop venant ensuite.

## URLs et structure actuelle (référence technique)

Les URLs exactes ne sont pas listées dans les notes actuelles. Pour le dossier hackathon, on se base sur les “zones” identifiées comme prioritaires dans le site existant :

* Homepage (page d’entrée principale)
* Agenda (liste d’événements)
* Page article “single” (lecture d’un article)
* Pages statiques : “Prix Cinergie” et “Notre histoire”
* Boutique + page panier/checkout + pages films (ajout au panier depuis la page film)

À compléter côté équipe au démarrage : URL de chaque page, et capture/repère du gabarit actuel (pour mesurer l’impact structurel des changements).

## Objectif général

Améliorer significativement l’expérience Cinergie sur mobile, sans déclencher une refonte structurelle qui casserait ou complexifierait le reste du site. Les chantiers ciblés sont ceux où le gain UX est élevé et où l’existant montre des limites claires : agenda (sans FullCalendar), page article (refonte complète), boutique/panier (feedback et repères), et deux pages statiques (structuration/design).

## Cohérence globale (valable sur tout le site)

Priorité mobile-first : chaque proposition doit être pensée pour un écran étroit et une interaction tactile.

Respect de la charte : pas de rupture visuelle, pas de “nouvelle identité”. Les améliorations doivent s’intégrer naturellement.

Impact structurel limité : éviter de réécrire des layouts qui servent partout. On privilégie des modifications localisées (gabarits spécifiques) plutôt qu’un changement de base qui toucherait toutes les pages.

Robustesse de contenu : prévoir des contraintes réelles (titres très variables, contenus hétérogènes, éléments manquants) sans casser la mise en page.

## Homepage (liberté de proposition, contrainte d’impact)

La homepage est ouverte à des propositions UX/UI, à condition de rester dans la charte et de limiter les répercussions sur les autres pages. L’enjeu est d’améliorer la clarté et l’efficacité sur mobile (hiérarchie, accès rapide aux contenus clés) sans imposer un refactor global.

Livrable attendu : maquette mobile-first + règles de mise en page + proposition implémentable de manière localisée.

## Agenda (abandon de FullCalendar, grille progressive)

Décision : on abandonne FullCalendar. Objectif : une solution “design grid” avec images.

Contraintes fonctionnelles et UX :

* La mise en page ne doit pas dépendre de titres “propres” : les titres sont extrêmement variables, donc il faut une stratégie de troncature/hauteurs stables.
* Au chargement, l’utilisateur voit tout de suite ce qui est pertinent “maintenant” (pas besoin de scroller pour trouver les prochains événements).
* Le scroll sert à avancer progressivement vers le futur.
* Navigation manuelle obligatoire : deux boutons “mois précédent / mois suivant”.
* Pas de navigation par année, et pas d’archives profondes : on reste sur une fenêtre environ -3 mois / +3 mois.

Livrable attendu : composant agenda en grille responsive (mobile-first) + comportement progressif + contrôles mois +/- + garde-fous sur la fenêtre temporelle.

## Page article “single” (refonte complète, mobile lecture)

La page article doit être repensée entièrement : le layout actuel est “écrit dans l’HTML” via des classes Bootstrap, ce qui rend les ajustements propres difficiles. L’approche demandée est de “tuer le design” existant et reconstruire un gabarit article dédié.

Exigence forte : un design particulièrement bon sur mobile (confort de lecture, hiérarchie, médias, rythme, blocs).

Livrable attendu : structure HTML sémantique + CSS (ou système de classes) moins dépendant de Bootstrap, avec une maquette mobile-first solide.

## Pages statiques

Deux pages statiques sont identifiées :

* “Prix Cinergie” : besoin de structuration (information architecture + présentation claire).
* “Notre histoire” : besoin de design (mise en forme, narration, rendu mobile qualitatif).

Livrables attendus : IA + maquettes mobile-first + implémentation simple via composants éditoriaux réutilisables (titres, sections, encadrés, blocs visuels).

## Boutique / panier / commande (repères + confirmation)

Problèmes UX identifiés :

* Ajout au panier possible depuis la page boutique et depuis la page film, mais le feedback actuel est faible.
* Le toast est facilement manquable.
* L’icône panier n’est visible que dans la boutique : manque de repère/accès dans le reste du parcours, donc expérience jugée “pas UX”.

Exigences attendues :

* Feedback d’ajout au panier clair et difficile à rater (sans être agressif).
* Repère panier plus visible et plus cohérent dans le parcours (au minimum sur les pages concernées, idéalement plus largement si l’impact structurel reste maîtrisé).
* Après commande : afficher un résumé de commande (confirmation) et envoyer un email de confirmation avec le même récapitulatif.

Livrables attendus : flux UX complet (ajout → panier → checkout → confirmation) + UI des états/feedback + page confirmation + envoi email.

## Résumé opérationnel pour les étudiants

Ce dossier n’est pas une demande de “refonte totale”. Il impose :

1. Une contrainte de stabilité (charte + impact structurel minimal).
2. Une priorité mobile-first stricte (lecture, navigation, repères, feedback).
3. Des chantiers ciblés à fort ROI UX :

* Agenda : grille avec images, progressive au scroll, navigation mois +/- et fenêtre -3/+3 mois, sans FullCalendar.
* Article single : refonte complète (sortir du layout Bootstrap inline) avec un design lecture mobile excellent.
* Boutique : rendre l’ajout au panier et l’accès au panier évidents, puis assurer confirmation + email après commande.
* Pages statiques : “Prix Cinergie” à structurer, “Notre histoire” à designer.

Le résultat attendu en 3 jours est une amélioration tangible du site sur mobile, livrée sous forme de gabarits/écrans implémentables et maintenables, sans provoquer de cascade de changements sur tout Cinergie.be.

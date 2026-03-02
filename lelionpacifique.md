# hackathon-2025-26 — le lion pacifique

## Contexte du site actuel

Le contenu disponible provient d’un article long (type “actualité / portrait”) et d’une présence officielle sur Instagram. L’enjeu du site “Le Lion Pacifique” est de transformer ce contenu en une galerie en ligne durable, lisible, et respectueuse : montrer l’art sans pousser à l’achat, raconter le parcours sans dramatisation ni romantisation, et donner des repères concrets (œuvres, expositions, demandes de projets).

Le point clé transversal est une exigence “œuvre d’abord” : l’interface doit laisser respirer les peintures (grands blancs, une œuvre à la fois quand possible) tout en restant mobile-first.

## URLs et structure actuelle (référence technique)

À ce stade, il n’existe pas d’URL de site. Références disponibles :

* Référence officielle : Instagram de l’artiste (Alpha / Lion Pacifique) : [https://www.instagram.com/alpha_lion_pacifique/](https://www.instagram.com/alpha_lion_pacifique/)
* Source éditoriale (contenu long) : article “Alpha Oumar Diallo…” (texte fourni dans les notes)

Pour le dossier hackathon, on se base sur des “zones” cibles à construire :

* Accueil (mise en avant d’une œuvre + accès galerie / demande)
* Galerie (liste des œuvres)
* Fiche œuvre (page détail)
* Parcours / Démarche (bio factuelle + repères)
* Actualités / Expositions (optionnel, basé sur articles)
* Demande de projet (commande personnalisée + upload)
* Contact

À compléter côté équipe au démarrage : nom de domaine, arborescence finale, et inventaire des contenus (photos HD, dimensions/techniques, textes par œuvre, expositions).

## Objectif général

Produire un site galerie mobile-first, sobre et crédible, qui :

1. Met l’œuvre au premier plan (consultation confortable, détails accessibles).
2. Donne un cadre factuel au parcours (repères, dates, lieux, sources), sans sur-récit.
3. Permet des demandes (fresque, portrait, atelier) via un formulaire clair avec photos de référence.

Le site doit fonctionner comme vitrine culturelle et point de contact, plus que comme e-commerce classique.

## Cohérence globale (valable sur tout le site)

Priorité mobile-first : navigation tactile, lecture fluide, images optimisées, repères clairs.

“Œuvre d’abord” : grands espaces blancs, hiérarchie visuelle simple, textes courts par défaut (avec option “lire plus”).

Palette issue des peintures : jaunes solaires, bleus profonds, rouges chaleureux, utilisée par touches (accents) sans nuire à la lisibilité.

Récit factuel, daté, attribué : si des éléments sensibles (asile, détention, etc.) sont mentionnés, ils doivent être présentés comme informations “selon la source X, à la date Y”, sans extrapolation.

Accessibilité : contrastes, navigation clavier, alt text descriptifs, focus visible, formulaires robustes.

## Accueil (mise en situation, entrée galerie)

L’accueil doit installer immédiatement le ton : une œuvre forte, un nom clair, et deux entrées principales.

Contenu attendu (issu des notes existantes) :

* Titre / baseline : “Alpha Oumar Diallo (Lion Pacifique)”
* Phrase courte : “Peintre, actif dans l’espace public à Bruxelles. Œuvres vibrantes, colorées, profondément humaines.”
* Accès direct :

  * “Voir les œuvres”
  * “Demande de projet” (fresque, portrait, atelier)

Option éditoriale (non obligatoire) : un bloc “Exposition en repère” (ex. CCM Molenbeek, dates) si l’équipe met en place une section “Actualités/Expos”.

## Galerie (grille responsive, respiration, tri léger)

Objectif : permettre de parcourir les œuvres sans surcharge.

Contraintes UX :

* Grille adaptative selon taille d’écran (1 colonne mobile → 2/3 colonnes desktop).
* Titres variables : prévoir troncature, hauteurs stables, et priorité à l’image.
* Accès rapide à une fiche œuvre (tap large).
* Filtres légers (optionnels si données disponibles) : série, technique, disponibilité.

Livrable attendu : composant galerie responsive + états (chargement / vide / erreur) + règles d’affichage (ratio image, marges, troncature).

## Fiche œuvre (détails, disponibilité, contact discret)

Chaque œuvre doit avoir une page dédiée, orientée “documentation + contemplation”.

Champs attendus (selon la demande initiale) :

* Images : 1 principale + secondaires (zoom/lightbox optionnel)
* Dimensions
* Technique
* Année (si connue)
* Histoire de création (courte par défaut, déroulable si long)
* Disponibilité (ex. “disponible”, “réservée”, “vendue”, “sur demande”)

CTA non agressif :

* “Demander cette œuvre” (ouvre une demande préremplie)
* “Commander un projet” (fresque/portrait/atelier)

Livrable attendu : gabarit fiche œuvre mobile-first + micro-IA des infos + style “carnet” (annotations légères non intrusives).

## Parcours / Démarche (contenu long conservé, mais hiérarchisé)

Le contenu fourni est très narratif. On le conserve, mais on le structure en couches pour éviter une page illisible sur mobile.

Couches recommandées :

1. Essentiel (court)

   * Origine : Guinée (Conakry)
   * Pratique : peinture, influence culturelle (référence “Picasso + culture africaine” dans le texte)
   * Présence dans l’espace public : Bruxelles (ex. Rue du Marché aux Poulets mentionnée)
   * Enseignement / ateliers enfants (élément central du pitch initial)

2. Repères (timeline courte, factuelle)

   * 2013 : caricature politique, répression (selon le texte)
   * Janvier 2014 : arrivée en Belgique (selon le texte)
   * 25 décembre 2023 → juin 2024 : période d’incarcération / libération (selon le texte)
   * Expositions citées : Mappa Mundo, Forum, Église du Béguinage, Debrouckère, etc. (selon le texte)

3. Texte long (intégral, attribué)

   * Reprise du texte complet, avec auteur et source clairement visibles, datation, et avertissement éditorial (“texte long, lecture 6–8 min”).

Livrable attendu : page “Parcours” structurée, lisible mobile, avec sommaire, ancres, et version courte/longue.

## Actualités / Expositions (optionnel, mais cohérent avec le contenu)

Si l’équipe implémente une section “Actualités”, le contenu fourni offre un exemple d’entrée :

* Exposition au Centre Communautaire Maritime (CCM), Molenbeek : 24 octobre → 17 novembre 2025
* Adresse : Rue Vandenboogaerde 93, 1080 Molenbeek-Saint-Jean
* Horaires mentionnés : lundi–vendredi, 9h–16h (gratuit)

Ce bloc doit rester informatif (quoi/où/quand) et renvoyer vers la page “Parcours” pour la lecture longue.

Livrable attendu : gabarit d’article/actualité simple + composant “cartouche expo” réutilisable.

## Demande de projet (commande personnalisée + upload)

Objectif : capter des demandes réelles sans complexifier.

Exigences fonctionnelles :

* Choix du type de demande : fresque / portrait / atelier / autre
* Description guidée : contexte, dimensions approximatives, lieu, délai, budget indicatif (optionnel)
* Upload de photos de référence
* Coordonnées : nom + email (téléphone optionnel)
* Confirmation claire après envoi

Contraintes de robustesse :

* Validation côté serveur
* Limites fichier (taille/type), renommage sécurisé, stockage non-exécutable
* Anti-CSRF

Livrable attendu : formulaire mobile-first + gestion upload + stockage (DB + fichiers) + page de confirmation.

## Résumé opérationnel pour les étudiants

Ce dossier ne demande pas un “site e-commerce agressif”. Il impose :

1. Une priorité “œuvre d’abord” (respiration, sobriété, une œuvre à la fois quand possible).
2. Un mobile-first strict (images, lecture, navigation, formulaires).
3. Un récit factuel (contenu long conservé mais structuré ; éléments sensibles attribués/daté).
4. Un socle fonctionnel utile en 3 jours :

* Accueil : œuvre forte + accès galerie + accès demande
* Galerie : grille responsive + tri léger si possible
* Fiche œuvre : détails + disponibilité + contact discret
* Parcours : version courte + repères + texte long attribué
* Demande de projet : formulaire + upload + confirmation

Le résultat attendu est un site présentable, maintenable, et crédible, qui respecte l’artiste et facilite la rencontre entre l’œuvre et le public.

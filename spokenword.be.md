# hackathon-2025-26 — spokenword.be (Dans! Dichter! Dans!)
## Contexte du site actuel

Le site est actuellement publié sur le domaine `https://www.spokenword.be/` et fonctionne sur WordPress (API visible via `wp-json`). ([Dans! Dichter! Dans! - ...][1]) Les contenus et libellés sont majoritairement en néerlandais (ex. “Over ons”, “Alle deelnemers”, “Gesprekken”), et la navigation n’est pas uniforme selon les pages, ce qui correspond au constat du client (“logo/newsletter/réseaux sociaux pas visibles partout”). ([Dans! Dichter! Dans! - ...][2])

Le site expose déjà des sections clés (participants, pages vidéos, interviews/“gesprekken”), mais certaines pages existent en double ou avec des slugs incohérents, par exemple `https://www.spokenword.be/over-ons/` et `https://www.spokenword.be/over-ons-2/`. ([Dans! Dichter! Dans! - ...][3])

## URLs et structure actuelle (référence technique)

La page d’accueil est `https://www.spokenword.be/`.
Les pages “contenu” déjà en place (et donc à conserver/adapter plutôt qu’inventer) incluent :

* “Alle deelnemers” (tous les participants) : `https://www.spokenword.be/deelnemers/`. ([Dans! Dichter! Dans! - ...][5])
* “Gesprekken” (interviews / conversations) : `https://www.spokenword.be/gesprekken/`, avec des pages enfants du type `https://www.spokenword.be/gesprekken/interview-…/`. ([Dans! Dichter! Dans! - ...][6])
* Pages vidéos : `https://www.spokenword.be/aftermovies/`, `https://www.spokenword.be/teasers/`, et “Testimonials” dans le menu “Filmpjes”. ([Dans! Dichter! Dans! - ...][2])

Le menu principal, selon plusieurs pages, suit un modèle “Home → Edities → Gesprekken → Alle deelnemers → Over ons → Open Calls → Filmpjes → Contact”, mais on observe aussi une variante où “Gesprekken” apparaît comme “Interviews” et où des sous-sections “Interlude” sont visibles (donc plusieurs gabarits de navigation coexistent). ([Dans! Dichter! Dans! - ...][2])

[1]: https://www.spokenword.be/wp-json/ "www.spokenword.be"
[2]: https://www.spokenword.be/aftermovies/ "Aftermovies - Dans! Dichter! Dans!"
[3]: https://www.spokenword.be/over-ons/?utm_source=chatgpt.com "Over ons"
[4]: https://www.spokenword.be/ "Dans! Dichter! Dans! - muzikaal spoken word platform"
[5]: https://www.spokenword.be/deelnemers/ "Alle deelnemers - Dans! Dichter! Dans!"
[6]: https://www.spokenword.be/gesprekken/?utm_source=chatgpt.com "Gesprekken met artiesten"
[7]: https://www.spokenword.be/over-ons-2/ "Over ons - Dans! Dichter! Dans!"


## Objectif général

Le client demande une mise à niveau globale de spokenword.be pour obtenir un site cohérent visuellement et plus facile à maintenir. Deux axes dominent : une identité graphique uniforme sur toutes les pages (éléments récurrents, typographies, proportions) et l’ajout/amélioration de pages de contenu, surtout autour des événements, des archives et des médias (vidéos, interviews, podcasts).

## Cohérence globale (valable sur tout le site)

Le logo, l’inscription à la newsletter et les liens vers les réseaux sociaux doivent être visibles sur chaque page. Actuellement ce n’est pas encore respecté partout, donc il faudra vérifier chaque gabarit.

Le client veut changer les couleurs du site. Cela implique de revoir la palette et de l’appliquer de manière homogène (fonds, textes, boutons, liens, zones de footer, etc.).

Les règles typographiques sont strictes : les titres doivent utiliser la “ddd-font”, sauf si certains caractères n’existent pas dans cette police (exception autorisée). Tout le reste du texte doit être en Sarabun. La hiérarchie de tailles doit être stable sur toutes les pages : un titre doit être environ 1,6 fois plus grand que le texte placé juste en dessous.

Le client souhaite aussi adapter manuellement les noms de pages dans les menus. Cela signifie qu’il faudra relire et corriger les libellés de navigation, et vérifier que les menus reflètent bien les intitulés attendus.

## Pages “Événements” (nouveau modèle)

Le client veut des pages dédiées aux événements, avec deux versions utilisables avant l’événement.

La première version est une page “pré-événement” sans line-up (pas encore d’artistes annoncés). Elle doit contenir un titre, un texte d’informations, un visuel principal (bannière, poster ou image carrée), et éventuellement deux boutons : un CTA vers un open call (optionnel et supprimable) et un CTA vers la billetterie (optionnel).

La deuxième version est une page “pré-événement” avec line-up. On garde titre, texte d’informations et visuel principal, mais on ajoute une section avec les images des performers et de courtes biographies. Le CTA billetterie reste possible (optionnel).

L’idée est de pouvoir publier une page tôt, puis l’enrichir au moment où la programmation est connue, sans changer toute la structure.

## Homepage (refonte selon 3 scénarios)

La homepage doit pouvoir changer selon qu’un événement approche ou non.

Si un événement arrive bientôt, la homepage doit pouvoir fonctionner comme une mise en avant de l’événement, en reprenant soit la version sans line-up (même logique que la page événement “pré-événement sans line-up”), soit la version avec line-up (même logique que la page événement “pré-événement avec line-up”).

S’il n’y a pas d’événement à venir, la homepage devient une page plus générale : un titre accroche, des images et/ou une vidéo, un bouton vers la page du dernier événement (pour garder une dynamique), et un bloc d’informations générales sur DDD.

## Footer (pied de page)

Le client envisage de modifier la présence du logo dans le footer : soit le retirer, soit le remplacer, soit l’ajouter. L’enjeu pour les étudiants est de rendre le footer flexible, sans casser l’équilibre graphique, et en gardant la cohérence avec la règle “logo + newsletter + réseaux sociaux visibles partout”.

## Page “Over ons” (À propos)

La page “Over ons” doit être mise à jour à la fois sur les personnes et sur les textes.

Le client veut pouvoir modifier l’équipe d’organisation : retirer un membre, remplacer un membre, ou ajouter un membre. La même logique s’applique à l’équipe de sélection.

Plusieurs textes doivent aussi être revus : la section “What do we do”, le texte explicatif sur l’équipe de sélection, et le texte sur les collaborations. Le résultat attendu est une page à jour, lisible sur mobile, avec une structure claire et homogène.

## Page “Past editions” (archives)

La page des éditions passées doit permettre d’ajouter des événements. Le client signale aussi que la structure et le layout pourraient être améliorés, donc il faudra rendre l’affichage plus propre et plus logique (ex : organisation par année, tuiles, sections répétables).

## Page “Alle deelnemers” (tous les participants)

Cette page doit permettre d’ajouter des noms. Elle doit aussi permettre d’ajouter des liens sur des noms déjà présents, ce qui implique que certains participants doivent pouvoir renvoyer vers un contenu associé (page, profil, média, etc.).

## Pages vidéos et médias

Plusieurs pages doivent être enrichies par ajout de vidéos.

La page “Aftermovies” doit permettre d’ajouter des films. La page “Teasers” doit permettre d’ajouter des films. La page “Testimonials” doit permettre d’ajouter des films.

Dans les trois cas, l’objectif est d’avoir une liste maintenable (ajouts simples) et un rendu propre (vignettes, titres, lecture confortable sur mobile).

## Page “Contact”

Le besoin est limité à une modification du texte. Même si c’est simple, il faut appliquer les règles globales : typographies, tailles, cohérence de mise en page.

## Page “Interview” (structure + ajouts réguliers)

Le client veut créer une page d’entrée qui regroupe des liens vers plusieurs types de contenus : anciens podcasts, “interlude”, interviews écrites, conseils de podcasts, et une playlist Spotify.

Ensuite, il doit être possible d’ajouter de nouveaux contenus au fil du temps : nouvelles interviews, nouveaux épisodes de podcast, et nouvelles recommandations de podcasts. L’enjeu est donc d’avoir une structure claire (rubriques) et une organisation facile à maintenir.

## Résumé opérationnel pour les étudiants

Ce cahier de demandes n’est pas seulement une liste “d’ajouts”. Il impose des gabarits réutilisables (événements, homepage conditionnelle, pages médias), une identité visuelle uniforme (éléments récurrents + typographies + proportions), et une logique de maintenance (ajouter/retirer du contenu sans casser la mise en page), avec une priorité implicite : un rendu mobile propre et cohérent sur tout le site.

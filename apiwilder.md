# hackathon-2025-26 — apiwilder

## Contexte du site actuel

ApiWilder est une ASBL qui porte un rucher collectif installé au bois du Wilder, sur d’anciens terrains potagers en lisière du bois, réaffectés à l’apiculture avec l’appui de Bruxelles-Environnement. Le projet existe depuis 2011, produit des essaims pour des apiculteurs isolés ainsi qu’un miel reconnu pour sa qualité, et mène un travail de sensibilisation lors d’événements communaux.

Le site à réaliser vise à soutenir financièrement le rucher et ses actions, en rendant le don simple, rassurant et motivant. L’enjeu central est la confiance : expliquer pourquoi la collecte existe, à quoi sert l’argent, où en est la collecte, et quel impact concret chaque contribution permet (matériel, ateliers, panneaux didactiques, actions de terrain). Le site doit aussi donner envie de rejoindre une dynamique locale autour des pollinisateurs (bénévolat, participation, contact).

## URLs et structure actuelle (référence technique)

L’URL n’est pas encore définie. Pour le dossier hackathon, on part d’une structure “page de dons + pages projets + transparence” :

Page d’accueil orientée don (pitch, jauge, paliers, CTA), page “Projets” (liste), page “Projet” (détail), page “Transparence” (à quoi sert l’argent + où en est la collecte + historique simplifié), page “À propos / le rucher”, page “S’impliquer / contact”.

## Positionnement et objectifs (côté utilisateur)

Le site doit convaincre rapidement un visiteur mobile qu’il s’agit d’un projet réel, local, utile, géré sérieusement, et que son don a un effet mesurable. L’interface doit réduire les frictions (comprendre en 10–20 secondes, trouver le bouton “Donner”, visualiser le progrès), tout en fournissant un second niveau de lecture pour les personnes qui veulent vérifier (montants, usage des fonds, dernières contributions, porteurs du projet).

## UX/UI (intentions et principes)

L’ambiance attendue est nature, artisanale et pédagogique : photos du rucher et du bois, portraits des bénévoles, textures douces (papier, bois), iconographie simple (abeille, fleurs, calendrier des actions). La mise en page doit être “Kickstarter-like” : une barre de progression visible en permanence sur la page de dons, des paliers de financement compréhensibles, et des cartes projets avec médias (photo/vidéo), objectifs clairs, et état d’avancement.

Le mobile-first est non négociable : hiérarchie très lisible, typographie confortable, blocs courts, CTA toujours accessible, feedback immédiat après action (don enregistré, total mis à jour, remerciement). Le contenu didactique doit rester accessible : expliquer le rôle des abeilles, l’année apicole, et les actions menées, sans noyer la page de dons.

## Contenu de référence (à intégrer / reformuler)

Le site doit pouvoir raconter : le rôle crucial des abeilles pour la pollinisation et notre alimentation, les menaces liées à nos modes de consommation, la réponse concrète du collectif (création de l’ASBL, rucher au bois du Wilder), les objectifs (initiation à une apiculture plus respectueuse, sensibilisation du grand public), et les actions (production d’essaims, miel, présence aux manifestations, panneaux d’information). Il doit aussi rendre explicite l’appel : “si vous désirez vous investir, contactez-nous”.

Contacts fournis : Houriet Khati (email et téléphone). Mention d’acteurs de soutien : Agenda 21 communal de Berchem et BLED asbl/vzw.

## Dev (périmètre réaliste hackathon)

Le cœur fonctionnel est un module de dons avec affichage du total récolté et une jauge de progression. Le site doit gérer des paliers (montant cible, intitulé, bénéfice concret) et des projets (liste + détail), chaque projet pouvant avoir une galerie photo/vidéo.

L’administration doit rester simple : soit un mini backoffice très limité, soit un fichier JSON administrable permettant de mettre à jour projets, paliers et montants (et éventuellement une liste d’entrées “dons” si on simule ou si on intègre un export). Côté public, un historique simplifié des derniers dons doit être affiché, avec anonymisation si nécessaire (ex. “Anonyme”, “M.”, “Mme”, “Donateur·rice”, montant et date).

Le dossier hackathon peut accepter une intégration de paiement “mock” (simulation) si l’intégration réelle est trop lourde ; dans ce cas, le focus reste sur la crédibilité UX (parcours, transparence, affichage dynamique, mise à jour du total via stockage simple). Si une intégration réelle est faisable, elle doit rester minimale et robuste (un seul montant libre + quelques montants rapides, confirmation, reçu/trace, protection anti-spam).

## Points d’attention (qualité et confiance)

La page de dons doit répondre clairement à trois questions : “Pourquoi récolter ?”, “À quoi sert l’argent ?”, “Où en est la collecte ?”. La transparence ne doit pas être une page cachée : elle doit être accessible depuis la page d’accueil et la page de dons. Les chiffres affichés (total, objectif, paliers) doivent provenir d’une source unique (JSON ou backoffice) pour éviter les incohérences.

## Données à prévoir (structure simple)

Projets : titre, objectif, description courte + longue, médias, montant cible, montant atteint (optionnel), statut, tags (matériel / sensibilisation / terrain).
Paliers : montant, intitulé, impact concret, état (atteint / prochain).
Dons : date, montant, nom affiché (ou “anonyme”), message optionnel (si on veut), identifiant interne.

## Informations pratiques

Nom : ASBL ApiWilder (rucher collectif au bois du Wilder).
URL : à définir.
Contact : Houriet Khati (email + téléphone fournis dans le brief).
Partenaire mentionné : BLED asbl/vzw (et soutien Agenda 21 communal de Berchem dans le texte).

# hackathon-2025-26 — bechill.be

## Contexte du site actuel

Be Chill est un salon esthétique / bien-être situé à Uccle (Chaussée d’Alsemberg 842, 1180). Aujourd’hui, la présence en ligne se fait essentiellement via Instagram et une page de réservation (Salonkee), avec des informations déjà riches (services, prix, horaires, avis vérifiés, accès, ambiance). Le besoin n’est pas de “refaire une marque”, mais de créer une page web mobile-first, rapide et rassurante, qui centralise l’essentiel, met en valeur l’expérience (calme, premium, chaleureux) et augmente la conversion vers la prise de rendez-vous.

Le site doit rester simple : une vitrine courte, claire, orientée action (“Réserver”), avec un parcours mobile direct et des repères pratiques immédiatement accessibles (accès, horaires, contact, itinéraire). L’objectif est d’éviter la surcharge (trop de texte, trop de widgets), tout en gardant assez de preuves de qualité (avis, photos, services phares) pour déclencher la réservation.

## URLs et structure actuelle (référence technique)

Le domaine n’existe pas encore pour le site vitrine. Les contenus de référence sont actuellement hébergés sur les plateformes suivantes (à utiliser comme source et comme leviers de conversion) : une page Salonkee (services, descriptions, prix, avis) et les réseaux sociaux (Instagram, Facebook, TikTok) pour l’ambiance et les contenus récurrents.

Côté “structure”, on part sur une landing page unique (one-page) qui renvoie vers Salonkee pour réserver. Le site vitrine doit pouvoir évoluer plus tard (pages dédiées par service, SEO local), mais la V1 du hackathon doit privilégier l’efficacité : une page, des sections courtes, des CTA visibles.

## Objectifs du hackathon (UX/UI + dev)

L’enjeu principal est la conversion sur mobile : rassurer en quelques secondes, montrer l’ambiance, donner les informations pratiques sans friction, puis pousser vers la réservation. Le design doit être “calme premium” (beaucoup d’air, typographie élégante, visuels plein cadre, palette douce), et la réalisation doit être légère (performances, images optimisées, peu de JS, chargement progressif).

Le livrable attendu est un site vitrine fonctionnel, crédible, et prêt à être branché sur une URL. Même si tout ne peut pas être “parfait” (SEO avancé, tracking, blog), le résultat doit être propre, cohérent, accessible, et utilisable immédiatement par une cliente sur smartphone.

## Contenus à intégrer (base fournie)

Le message principal (à reprendre tel quel ou légèrement lissé) : « Prenez soin de votre esprit en prenant soin de votre corps ». La description longue existe déjà : Be Chill comme espace dédié au massage et au bien-être profond, séances personnalisées, ambiance calme et élégante, extension beauté via soins/rituels capillaires (head spa).

Informations pratiques indispensables : adresse (Chaussée d’Alsemberg 842, Uccle 1180), téléphone (0492 10 05 95), indications d’accès (1er étage, premier escalier à droite), et “important information” (parking accessible, accueil avec secrétariat à l’entrée, boissons chaudes et collations).

Horaires à afficher clairement : lun-mar 09:30–18:00, mer 09:30–12:00, jeu-ven 09:30–18:00, sam 11:30–15:00, dim fermé, avec la note “Besoin d’adapter un horaire ? écrivez-moi”.

Services à mettre en avant (sans tout noyer) : massages, head spa, visage anti-âge, drainage & silhouette. Côté tarifs, on peut afficher des “à partir de” pour rassurer : massage sur mesure dès 90 €, pierres chaudes dès 85 €, dos/nuque/cuir chevelu 40 €, femme enceinte 75 €, gommage corps 50 €.

Preuve sociale : 15 avis vérifiés, note globale 4.9/5, et 3–5 extraits courts (sans en faire une page entière).

## UX/UI (parcours et sections recommandées)

Sur mobile, l’entrée doit être immédiate : un hero plein écran ou demi-écran avec une photo d’ambiance, une accroche courte, puis un bouton “Réserver” très visible. Le reste doit être scannable : sections courtes, titres lisibles, peu de texte par bloc, et une hiérarchie typographique régulière. L’intention est d’éviter une “page catalogue” et de construire une trajectoire : rassurer → donner envie → prouver → rendre simple → convertir.

Une structure efficace pour V1 : (1) Hero + CTA “Réserver”, (2) “Ce que vous trouvez ici” (bien-être profond, sur-mesure, ambiance), (3) Services phares (cartes courtes), (4) Tarifs indicatifs (4–6 lignes), (5) Avis (note + extraits), (6) Galerie (quelques images), (7) Infos pratiques (adresse, horaires, accès), (8) Contact (téléphone + mini formulaire). Sur toute la page, un CTA persistant (sticky) doit offrir “Réserver / Appeler / Itinéraire” pour ne jamais forcer l’utilisateur à remonter.

Instagram doit être présent mais discret : l’objectif est de donner un aperçu “vivant” sans ralentir le site. On privilégie une intégration légère (ex. 3–6 visuels récents) ou un simple lien “Voir sur Instagram”, plutôt qu’un widget lourd en iframe qui casse les performances.

## Dev (contraintes et choix techniques)

Mobile-first strict, CSS léger, et performance comme règle de base : images en formats modernes si possible (WebP/AVIF), tailles responsives, lazy-loading, et pas de dépendances lourdes. La page doit charger vite sur 4G et rester lisible sans JS (progressive enhancement).

La réservation se fait via Salonkee : au minimum, un lien propre et rassurant (“Réserver sur Salonkee”), et si l’embed est possible sans pénalité majeure, l’intégrer uniquement sur une section dédiée (pas en bloc “au-dessus de la ligne de flottaison”). Dans tous les cas, prévoir un fallback solide (lien direct) et éviter les intégrations qui dégradent l’accessibilité ou la vitesse.

Le contact : formulaire minimal (nom + téléphone/email + message), validation basique côté client, et anti-spam simple (honeypot + temporisation). Si aucun back-end n’est prévu pendant le hackathon, on peut soit basculer sur un mailto bien formaté, soit utiliser un endpoint léger (selon l’environnement du projet).

CTA persistants : barre fixe en bas sur mobile, avec trois actions maximum. “Appeler” doit déclencher `tel:`. “Itinéraire” doit pointer vers Google Maps (ou Apple Plans en fallback). “Réserver” vers Salonkee.

## Points d’attention (qualité et cohérence)

Cohérence éditoriale : harmoniser “Be Chill / Be chill”, accents (Chaussée d’Alsemberg), et uniformiser la tonalité (calme, premium, simple). Les textes très longs (ex. description détaillée d’un massage) peuvent être conservés mais placés en accordéon “En savoir plus”, pour garder la page respirante.

Accessibilité : contrastes suffisants malgré la palette douce, tailles de police confortables, boutons larges, textes alternatifs pour images, focus visible au clavier.

## Définition de “réussi” pour la V1

Une utilisatrice sur smartphone doit pouvoir : comprendre en 10 secondes ce qu’est Be Chill, voir les services principaux et une gamme de prix, être rassurée par les avis, trouver l’adresse et les horaires sans chercher, et réserver en 1–2 taps. Si ces points sont atteints avec une page rapide et propre, le hackathon est gagné.

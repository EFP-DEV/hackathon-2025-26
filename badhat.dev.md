## Contexte du projet

BADHAT (Bits As Decision. HTTP As Terminal.) est un micro-toolkit PHP orienté “request-lifecycle programming”. Ce n’est pas un framework : il fournit un noyau très réduit (environ 100 lignes de cœur) qui fait trois choses, sans ontologie imposée ni “magie” d’architecture : résoudre une URL en fichier, exécuter ce fichier, émettre une réponse HTTP. L’architecture n’est pas décrite par une configuration ou un conteneur : elle émerge du système de fichiers et de PHP lui-même.

La thèse est explicitement encodée dans le nom : les bits (bitmasks) pilotent les décisions, et HTTP est le terminal (le “dernier kilomètre” concret), pas une abstraction initiale. Le projet vise PHP ≥ 8.0 sur systèmes POSIX, sans dépendances, sans autoloader, sans DSL de configuration.

## Modules et périmètre (référence technique)

BADHAT tient en huit fichiers, chacun correspondant à une responsabilité clairement adressable :

* `map.php` : résolution URL → chemin → fichier, avec “seek” progressif
* `run.php` : include + invocation + gestion du buffer (output buffering) contrôlée par bitmasks
* `http.php` : staging/mutation des headers et émission contrôlée
* `trap.php` : installation handlers error/exception/shutdown + request IDs
* `pdo.php` : helper PDO minimal, sémantique d’échec explicite
* `auth.php` : login/logout à base de session, vérifications timing-safe
* `csrf.php` : génération/validation de tokens avec TTL
* `rfc.php` : validateurs RFC au niveau byte pour headers et chemins d’URI

Empreinte : 8 fichiers, aucun runtime externe, aucune dépendance, aucun “framework vocabulary”.

## Objectif du site

Le site n’est pas une page marketing. Il sert de documentation et de dossier de soumission, en reflétant exactement la philosophie du code : économie, traçabilité, absence d’effets cachés.

Trois publics sont servis, par ordre de priorité :

1. Évaluateurs (jury) : comprendre ce qu’est BADHAT, pourquoi il existe, et en quoi il diffère — en moins de 90 secondes, sans cloner un dépôt.
2. Praticiens (développeurs PHP) : accéder à une doc efficace, avec exemples exécutables, contraintes réelles, sans storytelling publicitaire.
3. Curieux (autres écosystèmes) : comprendre l’idée sans cours magistral ; philosophie transposable, implémentation PHP.

Non-objectifs : pas de témoignages, pas de compteurs, pas de “hero block” de landing SaaS, pas de matrice comparative, pas d’optimisation de conversion.

## Principes de conception (ce que le site doit “incarner”)

Le système de fichiers est le routeur. L’output buffering est le moteur de rendu. Les bitmasks sont le langage de configuration. PHP est le fichier de configuration. Les validations se font avec `if` (pas un framework). Toute transformation doit être traçable, chaque responsabilité doit avoir une adresse (un fichier, une page), chaque effet doit avoir une cause pointable.

## Contraintes UX (non négociables)

Information architecture : la structure doit rester plate, lisible, et prévisible. Toute information doit être atteignable en deux clics maximum. Pas de menus accordéons/collapsables : les destinations doivent être visibles (navigation = contenu). La documentation est découpée par module : une page par fichier `.php`. Pas de recherche au lancement : moins de 15 pages, Ctrl+F suffit. Les exemples de code se lisent de haut en bas : pas de tabs, pas de switchers, un parcours unique.

Expérience de lecture : limiter la largeur de ligne à 75 caractères pour éviter les erreurs de suivi visuel. Code en monospace, nettement séparé de la prose. Pas de thèmes de coloration syntaxique : une seule couleur pour le code, la structure doit parler d’elle-même. Chaque heading a un lien d’ancrage (deep-linking obligatoire). Aucune overlay modale : pas de cookie banner, newsletter popup, onboarding. Pas d’infinite scroll : chaque page est une unité complète avec début/fin.

Navigation et repères : les pages de doc ont une sidebar persistante (repérage constant), la page courante est toujours indiquée, et des breadcrumbs existent sur les pages de doc pour renforcer la hiérarchie sans surcharge cognitive. Pas de client-side routing : URLs réelles, back/forward, bookmarks et `curl` doivent fonctionner. Pas de spinners : si un spinner est “nécessaire”, la page est trop lourde.

## Contraintes UI (cohérence visuelle et anti-dérive)

Typographie : maximum deux polices (une monospace pour titres + code, une serif ou sans pour le corps). Corps en 16–18px, code en 14–15px. Pas de chargement depuis CDN : auto-hébergement ou polices système, pour éviter FOIT/CLS et dépendances tierces. Trois graisses maximum par famille.

Couleurs : maximum cinq couleurs au total (fond, texte, texte atténué, accent, fond de code). Le dark mode est obligatoire (dark-first acceptable). Pas de gradients. Accent utilisé parcimonieusement. Contraste WCAG AA ≥ 4.5:1 pour le texte.

Layout : largeur max de contenu 800px (doc = colonne lisible). Sidebar fixe 220–260px (présente sans dominer). Pas de grilles “marketing” (cards, icônes, blocs 3 colonnes). L’espace blanc sert de structure : espacement vertical généreux, pas de séparateurs décoratifs. Mobile : “content-first collapse” (sidebar devient menu supérieur, contenu plein écran, rien de caché derrière gestes).

Composants : pas de JS pour rendre le contenu (HTML complet côté build). JS uniquement pour confort (copie de code, toggle thème). Un seul style de blocs de code. Tables uniquement pour données, jamais pour mise en page. Pas de librairie d’icônes : SVG inline uniquement si nécessaire. Pas d’animations.

## Contraintes de développement (le site doit être BADHAT-compatible en philosophie)

Stack : site statique (générateur statique ou HTML pur). Build step autorisé, mais aucun runtime Node.js en production. Pas de framework CSS (pas de Tailwind/Bootstrap). Poids total par page < 100KB (assets inclus). Zéro requête externe (pas d’analytics, pas de fonts Google, pas de pixels). Site auto-contenu.

Pipeline de contenu : sources en Markdown, sortie en HTML (une transformation). La structure de la doc doit refléter le dépôt : `doc/map.md` → `/docs/map`. Pas de CMS : le contenu vit dans Git. Exemples extraits des tests : si un exemple ne s’exécute pas, il ne doit pas être publié. Une seule commande de build produit tout le site.

Performance & hébergement : pas de SSR à l’exécution (fichiers statiques servis par CDN ou serveur simple). `Cache-Control: immutable` sur assets avec noms versionnés. Aucun cookie (site de doc sans état). Lisible sans JavaScript. Déploiement “push main → live” en moins de 30 secondes.

## Inventaire des pages (lancement)

Chaque page a un but unique ; aucune page “de remplissage”.

* `/` : définition de BADHAT + philosophie en trois paragraphes + liens docs + dépôt
* `/docs` : index des modules (nom + phrase de rôle)
* `/docs/map` : `map.php` — `hook()`, `look()`, `seek()`, flags, exemples
* `/docs/run` : `run.php` — `loot()`, flags, contrat callable, pattern layout
* `/docs/http` : `http.php` — `headers()`, `out()`, `csp_nonce()`, référence flags
* `/docs/trap` : `trap.php` — installation handlers, format logs, flags
* `/docs/pdo` : `pdo.php` — `db()`, `qp()`, `trans()`, sémantique d’erreur
* `/docs/auth` : `auth.php` — `checkin()`, `checkout()`, notes sécurité
* `/docs/csrf` : `csrf.php` — lifecycle token, encodage, exemples
* `/docs/rfc` : `rfc.php` — `field_name()`, `field_value()`, `url_path()`
* `/quickstart` : init projet, subtree add, entry point, première route, premier rendu
* `/examples` : projets complets (blog, API, e-commerce, IoT) avec code réel
* `/license` : licence complète (courte)

## Direction visuelle

Ton “technical-editorial” : ni corporate, ni ludique. Références implicites : pages man Unix (dense, monospaced, sans waste), ratio data-ink de Tufte (chaque pixel doit porter du sens), éditeurs de dev (dark, structure visible), livres techniques (hiérarchie claire, marges, exemples qui tournent).

À éviter strictement : hero images, illustrations abstraites, photos stock, gradients/blobs, parallax, arrière-plans animés, effets “SaaS landing page” (glassmorphism/neumorphism/confetti).

## Critères de succès

Le site est considéré réussi si :

1. Un développeur comprend BADHAT, décide si c’est pertinent, et trouve la doc en moins de 60 secondes depuis la landing.
2. Un développeur passe de zéro à un cycle route→render via le quickstart, sans ressource externe.
3. Tous les exemples s’exécutent (zéro pseudo-code, zéro “…”).
4. Lighthouse : 100 en Performance et 100 en Accessibilité.
5. Le site reste intégralement lisible sans JavaScript.
6. Poids total du site (toutes pages cumulées) < 1MB.
7. Un juge comprend la proposition de valeur depuis la landing, sans connaître PHP.

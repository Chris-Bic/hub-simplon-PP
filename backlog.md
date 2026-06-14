# Backlog heavy-hub

## Contexte du projet

Le projet represente un portail membre avec home connectee, bibliotheque, detail contenu, dashboard, notifications et profil.

## Format attendu

Completer au minimum 3 user stories.
Remplacer chaque champ entre crochets par votre contenu.

## User story 1 - Compression

- Contexte: En tant que visiteur de l'annuaire Solydari, je veux que les pages se chargent plus rapidement, afin de de consommer moins de données et que ce soit rapide.
- Objectif: Réduire le poids des fichiers transférés de 3,5 Mo à moins de 2 Mo
- Bonne pratique d eco-conception ciblee: Activer la compression des fichiers côté serveur avant envoi au navigateur (RGESN 6.3)
- KPI associe: Poids de page mesuré via PageSpeed Insights avant/après activation
- Repo ou ecran concerne: Configuration serveur Infomaniak, pages annuaire et fiches entreprises
- Critere de reussite: Poids de page inférieur à 2 Mo constaté sur PageSpeed après activation
- Niveau de priorite: Haute

## User story 2 - Suppression librairies JS inutilisées

- Contexte: En tant que membre du réseau consultant l'annuaire, je veux que les pages de recherche s'affichent sans délai, afin de trouver rapidement un prestataire sans attendre.
- Objectif: Réduire le JavaScript inutilisé de 833 Ko à moins de 100 Ko
- Bonne pratique d eco-conception ciblee: Supprimer ou ne pas charger les librairies JS inutilisées sur les pages de l'annuaire (RGESN 6.5 + 6.1)
- KPI associe: Volume de JS inutilisé mesuré via PageSpeed Insights (actuellement environ 5Mo)
- Repo ou ecran concerne: Pages annuaire, filtres de recherche et fiches entreprises
- Critere de reussite: PageSpeed signale moins de 100 Ko de JS inutilisé sur les pages annuaire
- Niveau de priorite: Haute

## User story 3 - Lazy loading carte

- Contexte: En tant que visiteur consultant une fiche entreprise, je veux que la page s'affiche rapidement sans attendre le chargement de la carte, afin de trouver les informations du prestataire sans délai.
- Objectif: Réduire le temps de chargement initial de la fiche entreprise
- Bonne pratique d eco-conception ciblee:  Charger la carte Leaflet uniquement quand l'utilisateur la consulte - lazy loading (RGESN 6.5)
- KPI associe: Temps de chargement initial mesuré via PageSpeed avant/après
- Repo ou ecran concerne: Page fiche entreprise, composant carte interactive. Autre carte disponible sur la liste des poles.
- Critere de reussite: La carte ne se charge plus au premier affichage de la page. Déclenchement uniquement au scroll ou au clic
- Niveau de priorite: Moyenne

## User story 4 - Cache serveur

- Contexte : En tant que visiteur de l'annuaire Solydari, je veux que les pages se chargent instantanément, afin de ne pas attendre que le serveur recalcule une page dont le contenu n'a pas changé.
- Objectif : Réduire le nombre de requêtes de 230 à moins de 60
- Bonne pratique : Activer le cache serveur pour servir des pages statiques pré-générées (RGESN 7.1)
- KPI : Nombre de requêtes mesuré via EcoIndex avant/après activation
Repo ou écran concerné : Configuration LiteSpeed Cache, toutes les pages publiques du site
- Critère de réussite : EcoIndex passe d'une note F à une note D minimum
- Priorité : Haute

## User story 5 - Suppression doublons Analytics et cloisonnement JS

- Contexte : En tant que visiteur non connecté parcourant l'annuaire, je veux que la page ne charge pas de scripts inutiles à mon profil, afin de ne pas consommer de données pour des ressources qui ne me concernent pas.
- Objectif : Supprimer les 743 Ko de JavaScript inutilisé identifiés par PageSpeed Insights
- Bonne pratique : Supprimer les ressources dupliquées ou non utilisées selon le profil utilisateur (RGESN 6.5)
- KPI : Volume de JS inutilisé mesuré via PageSpeed avant/après
- Repo ou écran concerné : Toutes les pages publiques — scripts Analytics et plugin de gestion des transactions
- Critère de réussite : PageSpeed ne signale plus de doublon Analytics. Le plugin de transactions (Bulma + Tabulator) ne se charge plus sur les pages visiteurs non connectés
- Priorité : Haute

## Notes

- Vous pouvez ajouter d autres user stories si necessaire.
- Le niveau de detail attendu doit permettre une priorisation exploitable.

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

## Notes

- Vous pouvez ajouter d autres user stories si necessaire.
- Le niveau de detail attendu doit permettre une priorisation exploitable.

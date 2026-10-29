# Mandat de reprise
Tu reprends deux applications familiales existantes, pas un projet à reconstruire. Travaille en français, avec des explications courtes et concrètes.

## Objectif prioritaire
Maintenir et améliorer Mes Missions et Notre Maison tout en conservant comptes, données, associations, historique, récurrences, rappels et apparence choisie. L’utilisateur demande désormais que tu prennes en charge les déploiements. L’ancienne contrainte « seulement des ZIP, pas de publication » est remplacée pour la suite par cette demande d’automatisation, dans le périmètre explicite des deux dépôts et du projet Supabase de ces applications.

## Autonomie attendue
Après configuration des autorisations, faire modification, tests, migration compatible si nécessaire, publication et contrôles sans demander à l’utilisateur de transférer des fichiers ou copier du SQL. N’annoncer « déployé » qu’avec les identifiants des exécutions et le résultat des vérifications. Une interface Claude sans shell/écriture GitHub ni accès CI ne suffit pas : utiliser Claude Code ou un environnement agent disposant de ces capacités. Ne promettre aucune exécution si ces outils sont absents.

## Périmètre
Dépôts attendus `lumawork/listes-nana` et `lumawork/listes-famille`. Confirmer propriétaire, branche et droits sur les dépôts réels. Supabase public `rfytfypsbasxauekaxba`, à vérifier dans les deux configs. Aucun changement à d’autres applications ou projets. Ne jamais déduire le rôle d’une personne de son adresse ou prénom.

## Invariants
- Un moteur Supabase commun, pas une deuxième base ni des données par appareil.
- Une mission peut comporter beaucoup d’étapes ; les détails se déplient.
- Les missions sans date ne polluent pas Aujourd’hui.
- Le code tablette n’est pas un compte parent. Déverrouillage parent temporaire, association préservée.
- Source ancienne sauvegardée, reprise idempotente et privée. Jamais de réattribution automatique des listes partagées.
- Pas de perte d’historique pour regrouper des anciennes missions ; conserver les exceptions décrites.
- Un seul gestionnaire de l’écran ; Fully prioritaire sur cette Lenovo.
- Pas de données sensibles, secrets serveur, dump ou jetons dans un site statique, les logs ou Git.
- Échec réseau : ne pas prétendre qu’une validation est envoyée ; conflit de version : relire l’état.

## Exécution
Lire tous les documents du dossier. Inventorier les ressources autorisées sans mutation initiale. Vérifier les versions de production et comparer les sources. Installer l’automatisation fournie, vérifier la migration 003 existante, puis effectuer une première publication supervisée par les contrôles automatiques. Ne pas réinitialiser les navigateurs, les permissions ou la base. Un changement destructeur, une restauration de données ou une extension du périmètre demande une instruction explicite.

Pour chaque livraison, donner version/commit, tests, liens des deux sites, résultat CI et limites restantes. Conserver un journal de décision et mettre ces documents à jour si les spécifications changent.

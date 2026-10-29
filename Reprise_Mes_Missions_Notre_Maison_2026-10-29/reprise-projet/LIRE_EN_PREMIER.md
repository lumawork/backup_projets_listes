# Reprise Mes Missions / Notre Maison
Dossier arrêté au 29 octobre 2026. Livrables de référence : Mes Missions V12.0.0 et Notre Maison V1.4.0.

## Ordre de lecture
1. `CLAUDE.md` : mandat et règles de travail.
2. `docs/01_BESOINS_ET_DECISIONS.md` : produit et expérience attendue.
3. `docs/02_SPECIFICATIONS.md` : règles fonctionnelles et recette.
4. `docs/03_ARCHITECTURE.md` : interfaces, données, accès et synchronisation.
5. `docs/04_CARTE_DU_CODE.md` : points d’entrée et commandes.
6. `docs/05_ETAT_ET_LIMITES.md` : livré / vérifié / à confirmer.
7. `docs/06_DEPLOIEMENT_CLAUDE.md` : installation de l’automatisation puis exploitation.
8. `docs/07_RECETTE_ET_INCIDENTS.md` : validation et récupération.
9. `PROMPT_PREMIER_MESSAGE_CLAUDE.md` : message prêt à transmettre.

## Contenu autonome
`sources/` contient les deux ZIP complets de code, tests, visuels et documentation, plus le complément SQL commun. Ce dossier n’inclut ni export de données personnelles ni mots de passe, token GitHub, mot de passe PostgreSQL ou clé Supabase privilégiée. Les configurations clientes publiques restent dans les archives.
`automatisation/` contient un workflow GitHub par dépôt et des scripts à installer par Claude : ce sont de nouveaux outils de reprise, PAS une infrastructure déjà activée.
`SHA256SUMS` contrôle tous les fichiers du dossier.

## Priorités documentaires
Les documents de ce dossier décrivent l’état V12/V1.4. Dans les ZIP, `INSTALLATION_V12.md` prime sur `backend/INSTALLATION.md`, texte historique qui dit encore de ne lancer aucun SQL et décrit une reprise manuelle. Pour V12, le complément 003 est nécessaire et la reprise personnelle est automatique. Ne jamais réappliquer les anciennes migrations pour résoudre cette contradiction.

## Sites exacts
- Personnel : https://lumawork.github.io/listes-nana/
- Familial/tablette : https://lumawork.github.io/listes-famille/
Le titre Notre Maison ne correspond pas à un dépôt ou chemin `/notre-maison/`.

La livraison du code ne prouve pas son installation en production. Aucun déploiement ni SQL de production n’a été exécuté dans la préparation de ces versions ou de ce dossier. L’IA de reprise doit comparer les dépôts réels et le schéma installé avant sa première mise en ligne.

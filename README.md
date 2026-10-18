# Mon planner — version à héberger sur GitHub Pages

Ce dossier contient ton planner prêt à être mis en ligne (gratuitement) pour le tester sur ton téléphone.
Tout fonctionne dans **un seul fichier** (`index.html`). Les autres fichiers servent à l'installer comme une application et à l'utiliser **hors ligne**.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | le planner |
| `manifest.webmanifest` + `icons/` | nom, couleurs et icônes de l'application installée |
| `sw.js` | permet l'utilisation hors ligne (mise en cache) |
| `.nojekyll` | dit à GitHub de publier les fichiers tels quels |
| `THIRD_PARTY_NOTICES.md` | licences des composants libres (à garder) |

## Mise en ligne en 6 étapes (depuis un ordinateur ou le navigateur du téléphone)

1. **Décompresse** le fichier ZIP.
2. Sur [github.com](https://github.com), crée un compte (gratuit) puis **New repository** : donne-lui un nom court (par exemple `planner`), laisse **Public**, puis **Create repository**.
3. Dans le dépôt : **Add file › Upload files**. Glisse **tous** les fichiers décompressés **et le dossier `icons`** (le fichier `index.html` doit être à la racine, pas dans un sous-dossier). Clique sur **Commit changes**.
4. Va dans **Settings › Pages**. Sous *Build and deployment*, choisis **Deploy from a branch**, branche **main**, dossier **/(root)**, puis **Save**.
5. Attends 1 à 3 minutes. L'adresse apparaît en haut de la page : `https://TON-PSEUDO.github.io/NOM-DU-DEPOT/`
6. Ouvre cette adresse **dans Chrome sur ton téléphone**, puis menu **⋮ › Installer l'application** (ou **Ajouter à l'écran d'accueil**). Elle s'ouvre ensuite en plein écran, comme une vraie application, même sans connexion.

## Mettre à jour plus tard

Dans le dépôt, **Add file › Upload files**, envoie le nouveau `index.html` (et `sw.js` s'il est fourni) : GitHub remplace l'ancien. Ferme puis rouvre l'application **deux fois** pour qu'elle prenne la nouvelle version (à cause du cache hors ligne).

## À savoir

- **Tes données restent sur ton téléphone** (stockage du navigateur). Elles ne sont **pas** envoyées dans le dépôt GitHub : seul le code est public.
- Cette version est **séparée** de la version ouverte depuis ton compte Claude : les données ne se partagent pas automatiquement. Pour les transférer : dans l'ancienne version, **Réglages › Sauvegardes et e-mail › Télécharger le fichier**, puis dans la nouvelle **Importer un fichier**.
- Hors de Claude, ces fonctions ne sont **pas disponibles** : la sauvegarde en ligne dans ton compte Claude et la création d'exercices de langue par Claude (le défi « langue » du verrou de concentration). Le défi **échecs** (moteur Stockfish embarqué), les sauvegardes par fichier, le partage, les rappels, les sons et tout le reste fonctionnent.
- Les **notifications** et le **micro** demandent l'accès HTTPS, que GitHub Pages fournit.
- Le bouton **« M'offrir un café »** ouvre ta page Ko-fi dans un nouvel onglet.
- Pour effacer toutes les données du téléphone : paramètres du navigateur › données du site › effacer.

## Licences

Le planner embarque le moteur d'échecs libre **Stockfish.js (GPLv3)** : en publiant ce code dans un dépôt public, tu respectes cette licence. Garde le fichier `THIRD_PARTY_NOTICES.md`.

## Nouveautés de cette version

- **Écran d'accueil / profil** au premier lancement (prénom, nom, anniversaire, sexe, e-mail). Modifiable ensuite : ⚙ Réglages › « Mon profil ».
- **Barre de navigation fixe en bas** : Agenda, À faire, Suivis, Energy, Focus, Projets, Habit.
- **Menu déroulant (☰)** : Planning, Réglages, « Noter l’application », « Parler de l’application à un ami », « Nous contacter », « Politique de confidentialité » et « M’offrir un café ». Les 7 espaces sont déjà dans la barre du bas, ils ne sont plus répétés dans ce menu, et ces 4 actions ne sont plus dans les Réglages.
- **Verrou de concentration supprimé.**
- **Restauration** : bouton « Vérifier et restaurer mes données » (retrouve la sauvegarde gardée sur ce téléphone pour cet e-mail), ou glisser-déposer / importer un fichier `.json` de sauvegarde.
- **manifest.json** ajouté (pour PWABuilder).

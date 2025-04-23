# Template Dev Container: Monorepo Stack (Nx + Node 22 + TS + GCP + Pulumi)

Ce dépôt sert de template de base pour démarrer rapidement de nouveaux projets en utilisant une stack technologique moderne et cohérente, encapsulée dans un environnement de développement conteneurisé (Dev Container).

L'objectif est de fournir un environnement prêt à l'emploi avec les outils essentiels pré-configurés pour un développement efficace au sein d'un monorepo géré par Nx.

## Stack Technologique Cible

Ce Dev Container est configuré pour supporter les technologies suivantes :

- **Monorepo:** Nx (via l'extension Nx Console)
- **Runtime:** Node.js v22
- **Langage:** TypeScript
- **Cloud:** Google Cloud Platform (GCP)
- **Infrastructure as Code:** Pulumi
- **Gestionnaire de paquets:** `pnpm` (préinstallé dans le conteneur)

## Fonctionnalités du Dev Container

- **Image de Base:** `mcr.microsoft.com/devcontainers/typescript-node:22`
- **Outils CLI Inclus:**
  - Docker (via montage du socket Docker de l'hôte - `docker-in-docker` feature)
  - GitHub CLI (`gh`)
  - Pulumi CLI (`pulumi`)
  - Google Cloud CLI (`gcloud`)

## Configuration VS Code

L'environnement est pré-configuré pour VS Code avec :

- **Extensions Essentielles:**
  - Linting & Formatting: ESLint, Prettier
  - Frameworks & Outils: Nx Console, Tailwind CSS IntelliSense, GraphQL
  - Cloud & Infra: Pulumi, Google Cloud Code, Docker
  - Git: GitLens, Git Graph
  - Utilitaires: Code Runner, Task Explorer, PNPM, TODO Highlight, DotEnv
  - Thème: Material Theme + Icons
  - AI Assistants: Claude AI (Gemini est désactivé)
  - Autres: Postman
- **Paramètres Clés:**
  - **Formatteur par défaut:** Prettier (`esbenp.prettier-vscode`)
  - **Formatage à la sauvegarde:** Activé (`editor.formatOnSave: true`)
  - **Thème:** Material Theme Darker High Contrast (UI) & Material Theme Icons Darker (Icônes)

## Ports Transférés

Les ports suivants sont automatiquement transférés de l'intérieur du conteneur vers votre machine locale :

- `3000`: Port souvent utilisé par des applications frontend (ex: Next.js)
- `3001`: Port potentiel pour une API ou un service backend (ex: NestJS)

## Comment Utiliser ce Template

1.  **Créer un nouveau dépôt:** Cliquez sur le bouton "Use this template" sur la page GitHub de ce dépôt.
2.  **Cloner votre nouveau dépôt:** Clonez le dépôt que vous venez de créer sur votre machine locale.
    ```bash
    git clone <url-de-votre-nouveau-repo>
    cd <nom-de-votre-nouveau-repo>
    ```
3.  **Ouvrir dans VS Code:** Ouvrez le dossier cloné avec Visual Studio Code.
4.  **Rouvrir dans le Conteneur:** VS Code devrait détecter le fichier `.devcontainer/devcontainer.json` et vous proposer de "Reopen in Container" (Rouvrir dans le conteneur). Cliquez sur ce bouton.
5.  **Attendre la construction:** La première fois, le conteneur sera construit (cela peut prendre quelques minutes). Les fois suivantes, le démarrage sera beaucoup plus rapide.
6.  **Commencer à développer:** Une fois le conteneur démarré et VS Code connecté, votre environnement de développement est prêt !

## Prochaines Étapes (Après Démarrage du Conteneur)

1.  **Initialiser votre projet Nx (ou autre):** Ce template fournit l'environnement, mais pas encore le code source. Vous devrez initialiser votre workspace Nx ou copier votre projet existant ici.
    ```bash
    # Exemple pour créer un nouveau workspace Nx avec pnpm
    pnpm create nx-workspace@latest my-org
    ```
2.  **Installer les dépendances:** Une fois votre `package.json` en place :
    ```bash
    pnpm install
    ```
3.  **Coder !**

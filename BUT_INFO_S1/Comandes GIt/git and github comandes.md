### 1. Connexion et gestion GitHub (`gh`)

| Action                         | Commande                              | Description                                         |
| ------------------------------ | ------------------------------------- | --------------------------------------------------- |
| **Se connecter à GitHub**      | `gh auth login`                       | Lance l'authentification interactive via navigateur |
| **Vérifier sa connexion**      | `gh auth status`                      | Affiche le compte connecté et les droits actifs     |
| **Lister ses dépôts en ligne** | `gh repo list`                        | Affiche tes 30 derniers dépôts publics et privés    |
| **Cloner un dépôt GitHub**     | `gh repo clone auteur/projet`         | Télécharge un dépôt directement sur ton PC          |
| **Créer un dépôt en ligne**    | `gh repo create nom-projet --private` | Crée un nouveau dépôt privé sur ton GitHub          |

### 2. Démarrer ou récupérer un projet

| Action                           | Commande                                                                         | Description                                         |
| -------------------------------- | -------------------------------------------------------------------------------- | --------------------------------------------------- |
| **Configurer son identité**      | `git config --global user.name "Nom"`                                            | Définit ton nom pour tes commits (à faire une fois) |
| **Configurer son e-mail**        | `git config --global user.email "mail@ex.com"`                                   | Définit ton e-mail GitHub pour tes commits          |
| **Cloner via URL**               | `git clone [https://github.com/user/repo.git](https://github.com/user/repo.git)` | Récupère un dépôt existant dans un nouveau dossier  |
| **Initialiser un dépôt local**   | `git init`                                                                       | Transforme le dossier actuel en projet Git          |
| **Lier un dépôt local à GitHub** | `git remote add origin <URL>`                                                    | Connecte ton dossier local à un dépôt GitHub vide   |

### 3. Le cycle quotidien (Coder, Sauvegarder, Envoyer)

À chaque session de travail, suis cet ordre exact :

1. **Récupérer les nouveautés de l'équipe** avant de commencer à coder :
    
    Bash
    
    ```
    git pull
    ```
    
2. **Vérifier l'état des fichiers** (modifiés, ajoutés, supprimés) :
    
    Bash
    
    ```
    git status
    ```
    
3. **Préparer les fichiers** pour la sauvegarde :
    
    Bash
    
    ```
    git add .                 # Ajoute tous les fichiers modifiés
    git add nom-du-fichier    # Ajoute uniquement un fichier précis
    ```
    
4. **Enregistrer une version (commit)** avec un message clair :
    
    Bash
    
    ```
    git commit -m "Ajout de la page de connexion"
    ```
    
5. **Envoyer sur GitHub** :
    
    Bash
    
    ```
    git push
    ```
    

### 4. Gérer les branches (Travail en équipe)

| Action                               | Commande                        | Description                                               |
| ------------------------------------ | ------------------------------- | --------------------------------------------------------- |
| **Savoir sur quelle branche on est** | `git branch --show-current`     | Affiche uniquement le nom de ta branche active            |
| **Lister toutes les branches**       | `git branch -a`                 | Montre les branches locales et celles sur GitHub          |
| **Mettre à jour la liste distante**  | `git fetch --all`               | Récupère les nouvelles branches créées par les autres     |
| **Changer de branche**               | `git checkout nom-branche`      | Bascule sur une branche existante (locale ou distante)    |
| **Créer et ouvrir une branche**      | `git checkout -b ma-branche`    | Crée une nouvelle branche et te place dessus              |
| **Pousser une nouvelle branche**     | `git push -u origin ma-branche` | Publie ta branche locale sur GitHub (1re fois uniquement) |
| **Fusionner une branche**            | `git merge autre-branche`       | Intègre le code d'une branche dans celle où tu te trouves |
| **Supprimer une branche locale**     | `git branch -d nom-branche`     | Supprime une branche locale déjà fusionnée                |

### 5. Historique et annulation d'erreurs

| Situation                           | Commande                          | Effet                                                        |
| ----------------------------------- | --------------------------------- | ------------------------------------------------------------ |
| **Voir l'historique des commits**   | `git log --oneline`               | Affiche la liste condensée des versions enregistrées         |
| **Annuler les modifs d'un fichier** | `git checkout -- nom-fichier`     | Remet le fichier tel qu'il était au dernier commit           |
| **Retirer un fichier du `git add`** | `git reset HEAD nom-fichier`      | Annule la mise en attente sans perdre ton code               |
| **Corriger le dernier message**     | `git commit --amend -m "Nouveau"` | Modifie le message du tout dernier commit                    |
| **Mettre son code de côté**         | `git stash`                       | Sauvegarde temporairement tes modifs pour changer de branche |
| **Récupérer le code mis de côté**   | `git stash pop`                   | Réapplique les modifications mises de côté avec `stash`      |
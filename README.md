# Setup-windows-10

Voici une version complète et intégrée du guide pour la configuration de l'environnement de développement sous Windows :

### Configuration de l'Environnement de Développement pour Windows

#### Prérequis

1. **Git Bash** : Téléchargez et installez Git Bash depuis [ce lien](https://git-scm.com/downloads).

2. **Node.js** : Installez Node.js depuis [le site officiel](https://nodejs.org/).

3. **Yarn** : Installez Yarn via Git Bash :
   ```bash
   npm install --global yarn
   ```

4. **Visual Studio Code** : Téléchargez et installez Visual Studio Code depuis [ce site](https://code.visualstudio.com/). Ajoutez l'extension "Remote - WSL".

5. **WSL (Windows Subsystem for Linux)** : Activez WSL avec les commandes suivantes dans PowerShell en tant qu'administrateur :
   ```bash
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
   ```

6. **Installation d'Ubuntu sur WSL** : Installez Ubuntu via le Microsoft Store.

7. **Terminal Windows** : Installez Windows Terminal depuis le [Microsoft Store](https://www.microsoft.com/store/productId/9N0DX20HK701).

8. **Zsh, Git, et outils de ligne de commande** : Dans Ubuntu, installez Zsh, Git et divers outils :
   ```bash
   sudo apt update
   sudo apt install -y curl git imagemagick jq unzip vim zsh tree
   ```

9. **Oh-my-zsh** : Installez Oh My Zsh :
   ```bash
   sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```

10. **GitHub CLI** : Installez GitHub CLI :
    ```bash
    curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
    sudo apt update
    sudo apt install -y gh
    ```

11. **Navigateur par défaut sous Ubuntu** : Configurez un navigateur par défaut avec `sudo update-alternatives --config x-www-browser`.

12. **Authentification GitHub** : Authentifiez-vous sur GitHub avec :
    ```bash
    gh auth login -s 'user:email' -w
    ```

#### Vérification de l'installation

Vérifiez chaque installation avec les commandes appropriées pour Git, Node.js, Yarn, et Rails. Assurez-vous que tous les outils répondent avec les versions attendues.

Cette documentation complète vous aidera à préparer et vérifier un environnement de développement robuste sous Windows.

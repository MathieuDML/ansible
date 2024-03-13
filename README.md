# 👋 Ansible

# 🚀 Ajout d'un Workflow GitHub 

1. Dans votre dépôt GitHub, cliquez sur l'onglet "Actions".
2. Cliquez sur "New workflow".
3. Vous pouvez choisir de partir d'un workflow prédéfini ou créer le vôtre en cliquant sur "set up a workflow yourself".
4. Nommez votre fichier de workflow (par exemple, main.yml) et ajoutez le contenu de votre workflow. Un workflow typique pourrait ressembler à ceci :

```yaml
name: Mon premier workflow

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Exécute une commande
      run: echo "Hello, world!"
```

5. Cliquez sur "Start commit".

6. Entrez un message de commit et une description, puis cliquez sur "Commit new file".

Votre workflow sera exécuté chaque fois que l'événement spécifié se produit (dans cet exemple, à chaque push sur le dépôt).

# 🏃‍♂️ Configuration d'un Runner GitHub

1. Connectez-vous à votre compte GitHub et accédez à votre dépôt.
2. Cliquez sur "Settings" dans le menu en haut de la page.
3. Cliquez sur "Actions" dans le menu de gauche.
4. Sous "Self-hosted runners", cliquez sur "Add runner".
5. Sélectionnez le système d'exploitation et l'architecture de votre machine, puis suivez les instructions pour installer le runner.

# 🤫 Ajout d'un Secret au Dépôt

1. Dans les paramètres de votre dépôt, cliquez sur "Secrets" dans le menu de gauche.
2. Cliquez sur "New repository secret".
3. Donnez un nom à votre secret. Par exemple, vous pouvez le nommer SUDO_PASSWORD.
4. Entrez la valeur de votre secret. Dans ce cas, il s'agit de votre mot de passe sudo.
5. Cliquez sur "Add secret" pour sauvegarder le secret.

Maintenant, vous pouvez utiliser ce secret dans votre fichier de workflow GitHub Actions en utilisant la syntaxe suivante : ${{ secrets.SUDO_PASSWORD }}.
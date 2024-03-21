# Déploiement du Site Web

Ce dépôt contient un workflow GitHub Actions pour automatiser le déploiement d'un site web via FTP.

## Configuration

### Déclencheurs

Le déploiement est déclenché automatiquement lorsqu'un push est effectué sur la branche `main`. Vous pouvez également déclencher manuellement le déploiement en utilisant l'option "Run workflow" dans l'interface des workflows GitHub.

### Secrets

Assurez-vous de configurer les secrets suivants dans les paramètres secrets de votre dépôt :

- `FTP_SERVER`: Adresse du serveur FTP pour le déploiement.
- `FTP_USERNAME`: Nom d'utilisateur FTP.
- `FTP_PASSWORD`: Mot de passe FTP.

## Déploiement Automatisé

Le déploiement est automatisé à l'aide de GitHub Actions. Voici les étapes principales du processus de déploiement :

1. **Checkout Repository**: Cette étape récupère le contenu du dépôt GitHub pour être prêt à être déployé.

2. **Deploy Website**: Cette étape déploie le site web en utilisant l'action `simple-ftp-deploy-action`. Elle transfère les fichiers du répertoire local spécifié vers le serveur FTP, en excluant les fichiers correspondant aux motifs spécifiés.

## Comment Utiliser

Pour utiliser ce workflow dans votre propre projet, suivez ces étapes :

1. Créez un fichier similaire `main.yml` dans le répertoire `.github/workflows` de votre dépôt.
2. Configurez les secrets `FTP_SERVER`, `FTP_USERNAME` et `FTP_PASSWORD` dans les paramètres secrets de votre dépôt.
3. Personnalisez le chemin du répertoire local à déployer et le répertoire cible sur le serveur FTP dans le fichier YAML du workflow si nécessaire.

## Auteur

Ce workflow GitHub Actions a été créé par [A2B78](https://github.com/A2B78/ftp-site-deploy.git).

## Licence

Ce projet est sous licence [MIT](LICENSE).

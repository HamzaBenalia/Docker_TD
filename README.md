![Logo Docker Facebook](images/docker-facebook.png)

# Guide d'utilisation - Docker

Ce guide explique les étapes pour créer des images Docker, créer des tags et publier ces images sur un registre Docker.

## Création d'images Docker

Pour créer une image Docker à partir d'un Dockerfile, suivez ces étapes :

1. Assurez-vous d'avoir un Dockerfile dans votre répertoire contenant les instructions pour construire votre image Docker.
2. Ouvrez un terminal et accédez au répertoire où se trouve votre Dockerfile.
3. Utilisez la commande `docker build` pour construire votre image. Par exemple :

    ```bash
    docker build -t mon_image:latest .
    ```

   Cette commande construit une image nommée "mon_image" avec le tag "latest" à partir du Dockerfile actuel (`.` représente le répertoire actuel).

## Création de tags

Une fois que vous avez construit votre image Docker, vous pouvez lui attribuer des tags pour identifier différentes versions ou des états spécifiques. Voici comment :

1. Utilisez la commande `docker tag` avec l'ID de l'image et le nouveau tag que vous souhaitez lui attribuer. Par exemple :

    ```bash
    docker tag mon_image:latest mon_image:v1.0
    ```

   Cette commande crée un nouveau tag "v1.0" pour l'image "mon_image:latest".

## Publication des images Docker

Après avoir créé vos images Docker et attribué des tags, vous pouvez les publier sur un registre Docker pour les partager avec d'autres utilisateurs. Suivez ces étapes :

1. Connectez-vous à votre registre Docker à l'aide de la commande `docker login`. Vous devrez fournir vos identifiants Docker Hub (ou d'autres registres Docker) :

    ```bash
    docker login
    ```

2. Utilisez la commande `docker push` pour publier vos images sur le registre. Par exemple :

    ```bash
    docker push mon_utilisateur/mon_image:v1.0
    ```

   Assurez-vous de remplacer "mon_utilisateur" par votre nom d'utilisateur sur Docker Hub et "mon_image:v1.0" par le nom de votre image et le tag que vous souhaitez publier.

Ces étapes devraient vous aider à créer des images Docker, à leur attribuer des tags et à les publier sur un registre Docker pour les partager avec d'autres utilisateurs.

---


### URLs des images Docker

- BFF : [hamza3991/bffapp](https://hub.docker.com/repository/docker/hamza3991/bffapp/general)
- Front : [hamza3991/frontapp](https://hub.docker.com/repository/docker/hamza3991/frontapp/general)


🐳 Bon développement en Docker !

# Docker compose

## Services

Ce docker compose fourni 4 services :
1. `db`, contenant une image mysql et un volume pour conserver les données à l'exctinction des containers. L'environnement du container contient aussi les variables de base mysql telles que la base de données et le mot de passe.
2. `phpmyadmin`, contenant une image phpmyadmin, déployée sur le port `8080:80`. Le container contient aussi les variables d'environnement nécessaires à se connecter à la db.
3. `apache`, contenant une image build d'un Dockerfile situé dans `./www/php`, déployé sur le port `80:80` et utilisant un volume local. Le Dockerfile charge un fichier de configuration au lancement.
4. `php`, contenant une image php en version 7.4-fdm, déployé sur le port `9000:9000` et utilisant un volume local.

Enfin le docker compose déclare le volume de la base de données utilisé.
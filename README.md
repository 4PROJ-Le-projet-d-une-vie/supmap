# Supmap

| Nom              | Spécialité                    |
|------------------|-------------------------------|
| Bihel Lucas      | Systèmes et Réseaux           |
| Bosquet Ewen     | Développement Cloud et Modile |
| Cheruel Baptiste | Développement Cloud et Modile |
| Durand Mathéo    | Systèmes et Réseaux           |

Organisation Github : https://github.com/4PROJ-Le-projet-d-une-vie

## Présentation

SupMap est une application mobile de navigation en temps réel dédiée aux trajets en France. 
Elle informe les conducteurs sur le trafic, les incidents routiers et propose des itinéraires optimisés. 
Les utilisateurs peuvent aussi signaler des événements et contribuer à la fiabilité des informations.

## Organisation

Le projet est séparé en plusieurs sous-projets. Chaque sous projet est un repository git.
L'ensemble des services et applicatifs intègrent une Github Action permettant de fabriquer une image de l'applicatif.

| Service           | Description                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| supmap-gateway    | Gateway permettant d'exposer et centraler l'ensemble des endpoint HTTP des services                           |
| supmap-users      | Service incluant l'ensemble des fonctionnalités de gestion des utilisateurs et d'authentification (Stateless) |
| supmap-gis        | Service incluant les fonctionnalités de routing et de géocoding (Stateless)                                   |
| supmap-incidents  | Service incluant la gestion en direct des incidents et des intéractions avec ces incidents (Stateless)        |
| supmap-navigation | Service de gestion de navigation en temps réel                                                                |
| supmap-front      | Application mobile implémentant les fonctionnalités proposées par les services                                |
| supmap-webapp     | Application Web permettant de consulter les incidents et de créer un itinéraire personnalisé                  |
| supmap-devops     | Centralisation du déploiement et de la configuration du projet                                                |

Le repository `supmap-devops` est le point central du projet, car il centralise l'ensemble des configurations.

## Documentation

Chaque sous-projet inclut sa propre documentation. Nous avons converti au format PDF l'entièreté de ces documentations.

| Service           | Documentation PDF | Documentation MD                                                      |
|-------------------|-------------------|-----------------------------------------------------------------------|
| supmap-gateway    | []()              | [README.md](./supmap-gateway/README.md)                               |
| supmap-users      | []()              | [README.md](./supmap-users/README.md)                                 |
| supmap-gis        | []()              | [README.md](./supmap-gis/README.md)                                   |
| supmap-incidents  | []()              | [README.md](./supmap-incidents/README.md)                             |
| supmap-navigation | []()              | [README.md](./supmap-navigation/README.md)                            |
| supmap-front      | []()              | [TechnicalDocumentation.md](./supmap-front/TechnicalDocumentation.md) |
| supmap-webapp     | []()              | [README.md](./supmap-webapp/README.md)                                |
| supmap-devops     | []()              | [README.md](./supmap-devops/README.md)                                |

> NB: Les fichiers au format PDF contient quelques soucis de format. En cas de soucis, référencez-vous au fichier Markdown associé ou consultez ce même fichier sur Github.

La documentation d'infrastructure finale du projet est disponible dans le fichier [network_documentation.md](./network_documentation.md)

La documentation utilisateur est disponible dans le fichier [users_documentation.pdf](./users_documentation.pdf)
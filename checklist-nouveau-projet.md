# Checklist d'init de projet Steamulo

- Ajouter un [.editorconfig](http://editorconfig.org/) pour éviter les IDE à 2 ou 4 caractères de tabulations
(charset UTF-8 PARTOUT).
- Selon le projet, créer / éditer le .gitignore pour ajouter "./idea".
- Créer un alias mail avec toutes les personnes du projet.
- Jenkins
    - Créer une tâche de build MR (appelée par Gitlab lors du 'Merge Request Event').
    - Créer une tâche de livraison (appelée par Gitlab lors du 'Tag Push Event').
    - Créer une tâche Sonar, lancée toutes les nuits, qui poussera le résultat de l'analyse vers Sonar.
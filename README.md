# TP2

# Quelles étapes (steps) sont réalisées par cette action ?

- Déclenchement de l'action : l'action se déclenche sur les évenements de push ou de pull_request sur la branche main.
- Permissions : l'action a une permission de lecture (read) sur le contenu du dépôt
- Job "build" : le job est effectué sur la dernière version de ubuntu, celui-ci va ensuite configurer l'environnement python, installer les dépendances, executer flake8 pour identifier les erreurs de syntaxe python, puis finalement va executer les tests unitaires avec pytest.

# Une étape est définie au minimum par 2 éléments, lesquels sont-ils et à quoi servent-ils ?

Les éléments "uses" et "run". "uses" spécifie une action réutilisable à executer, "run" est utilisé pour executer des commandes ou script directement dans le runner.

# La première étape contient le mot-clé ‘with’, a quoi sert-il ?

Le mot-clé "with" permets de passer des paramètres ou arguments supplémentaires à une action "uses".
Dans notre exemple, "with" est utilisé pour précisier la version de python pour le "uses" "uses: actions/setup-python@v3".


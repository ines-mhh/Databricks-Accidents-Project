# Projet d'Examen - Accidents de la Route

## Présentation du Projet
Le projet vise à créer et héberger un modèle prédictif pour évaluer les accidents de la route. Les données utilisées proviennent du travail d'Ilyes Talbi, qui a été présenté dans les premières sessions. 

## Sources des Données
Les données pour ce projet ont été fournies par Ilyes Talbi. Pour plus d'informations, veuillez consulter les sources mentionnées dans le travail d'Ilyes Talbi [ici](https://larevueia.fr/xgboost-vs-random-forest-predire-la-gravite-dun-accident-de-la-route/).

## Éléments du Repository
- **Code source**: Les scripts et notebooks utilisés pour prétraiter les données, construire et évaluer les modèles.
- **README.md**: Ce fichier contenant la documentation du projet.
- **Azure Configuration**: Les configurations et scripts pour créer le groupe de ressources, l'instance Azure Databricks, et le cluster.
- **Databricks Notebooks**: Les notebooks utilisés pour importer les données, construire les modèles, et tester l'API.
- **Modèles Enregistrés**: Les meilleurs modèles sélectionnés après l'évaluation.

## Modèle Retenu et Performances
Trois modèles ont été construits et évalués :
1. **KNeighborsClassifier**
    - Paramètre optimisé : `n_neighbors`
    - Performances : Précision, F1-score
    
2. **DecisionTreeClassifier**
    - Paramètres optimisés : `max_depth`, `min_samples_leaf`
    - Performances : Précision, F1-score
    
3. **RandomForestClassifier**
    - Paramètres optimisés : `n_estimators`, `max_depth`, `min_samples_leaf`
    - Performances : Précision, F1-score

Le meilleur modèle de chaque méthode a été enregistré dans Databricks sous le nom "BestModel".

## Endpoint du Modèle
Le modèle est hébergé sur Databricks. Vous pouvez accéder à l'endpoint du modèle à [lien de l'endpoint].

## Documentation de l'API
Un token a été créé pour consommer l'API du modèle, avec un délai d'expiration fixé à 30 jours. Vous pouvez utiliser le notebook "Test API" dans le dossier Shared du workspace de Databricks pour tester le modèle avec des exemples d'accidents.

---
N'oubliez pas de remplacer "[lien de l'endpoint]" par le lien réel de votre endpoint. Cette documentation devrait servir de guide pour quiconque souhaite comprendre et utiliser votre projet.

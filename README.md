# Examen Inès MEHAH - Accidents de la Route 

## Présentation du Projet
Le projet vise à créer et héberger un modèle prédictif pour évaluer les accidents de la route. 

## Sources des Données
Les données utilisées proviennent du travail d'Ilyes Talbi, qui a été présenté dans les premières sessions à retrouver [ici](https://larevueia.fr/xgboost-vs-random-forest-predire-la-gravite-dun-accident-de-la-route/).

## Éléments du Repository
- **README.md**: Ce fichier contenant la documentation du projet (présentation du projet, les sources des données, etc.).
- **Databricks Notebooks**: Les notebooks utilisés pour importer les données, construire les modèles (Notebook : "Modelisation"), et tester l'API (Notebook : "Test API").
- **Modèle retenu**: Le meilleur modèle sélectionné après l'évaluation ainsi que ses performances.

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

Les modèles ont été évalués sur leurs performances. Les résultats sont les suivants :

1. **KNeighborsClassifier :**
   - Accuracy : 0.58
   - F1-score : 0.56

2. **DecisionTreeClassifier :**
    - Accuracy : 0.61
    - F1-score : 0.59

3. **RandomForestClassifier :**
   - Accuracy : 0.64
   - F1-score : 0.62

Le modèle RandomForestClassifier avec une accuracy de 0.64 et un F1-score de 0.62 a été identifié comme le meilleur modèle.

## Endpoint du Modèle
Le modèle est hébergé sur Databricks. Vous pouvez accéder à l'endpoint du modèle à [lien de l'endpoint](https://adb-5635851618340357.17.azuredatabricks.net/serving-endpoints/mehahines/invocations).

## Documentation de l'API
Un token a été créé pour consommer l'API du modèle, avec un délai d'expiration fixé à 30 jours. Vous pouvez utiliser le notebook "Test API" dans le dossier Shared du workspace de Databricks pour tester le modèle avec des exemples d'accidents.


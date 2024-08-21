# Application de recommandation d'articles  

## Objectif du Projet  

Ce projet a pour but de développer une application de recommandation d'articles.  
Il correspond au livrable n°2 du projet "Réalisez une application de recommandation de contenu".  

Les données utilisées pour ce projet sont en opensource sur kaggle et disponible en suivant le lien : https://www.kaggle.com/datasets/gspmoreira/news-portal-user-interactions-by-globocom#clicks_sample.csv.  

## Structure du Projet  

Les fichiers et modèles utilisés pour cette application ont été créé en utilisant le fichier EDA.ipynb présent dans ce dossier.    
Ils ont ensuite été stocké sur Azure Blob Storage pour être utilisé dans l'azure function.  

L'azure function est déployée sur azure à l'adresse https://apprecopq.azurewebsites.net.  

La fonction est composée de 2 HttpTriggers :  

- HttpTrigger1 qui récupère les Ids utilisateur est disponible à l'adresse : https://apprecopq.azurewebsites.net/api/HttpTrigger1?code=Fy258_J-hAV1mjbnLRhWumDbtiQoBrG245qhqqK-btzaAzFuobqI_w%3D%3D  

- HttpTrigger2 qui effectue les prédection et renvoie les recommandations d'article est disponible à l'adresse : https://apprecopq.azurewebsites.net/api/HttpTrigger2?code=Fy258_J-hAV1mjbnLRhWumDbtiQoBrG245qhqqK-btzaAzFuobqI_w%3D%3D  



## Utilisation  

Ce repo a été configuré pour être déployé directement sur le portail azure.  
Pour créer votre propre application de recommandation à partir des fichiers :   

- Déposer les fichier HttpTrigger1, HttpTrigger2 et le fichier requirements directement dans un repo github.  
- Créer une Azure function sur le portail azure (l'hébergement basique suffit à faire tourner l'application).  
- Une fois l'azure function créée, connecter simplement le repo github en déploiement continu.  
- Mettre à jour les liens dans l'application streamlit (livrable 1 du projet) afin de récupérer les Ids et les recommandations.  


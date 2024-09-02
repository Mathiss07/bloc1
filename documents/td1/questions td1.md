# 1 - Méthodes GET et POST
## GET 
- Avec la méthode GET, les données à envoyer au serveur sont écrites directement dans l’URL.
- Toutes les informations saisies par l’utilisateur (les paramètres dits URL) sont transmises aussi librement que l’URL elle-même.
- Visibilité : Visible pour l’utilisateur dans le champ d’adresse
- Marque-page et historique de navigation : Les paramètres de l’URL sont stockés en même temps que l’URL.
- Cache et fichier log du serveur : Les paramètres de l’URL sont stockés sans chiffrement
- Comportement lors de l’actualisation du navigateur / Bouton « précédent » :Les paramètres de l’URL ne sont pas envoyés à nouveau.
- Type de données : Caractères ASCII uniquement.
- Longueur des données : Limitée - longueur maximale de l’URL à 2 048 caractères.
## POST
- La méthode POST écrit les paramètres URL dans la requête HTTP pour le serveur. Les paramètres ne sont donc pas visibles pour les utilisateurs et la portée des requêtes POST est illimitée.
- Visibilité : Invisible pour l’utilisateur
- Marque-page et historique de navigation : L’URL est enregistrée sans paramètres URL.
- Cache et fichier log du serveur : Les paramètres de l’URL ne sont pas enregistrés automatiquement.
- Comportement lors de l’actualisation du navigateur / Bouton « précédent » : Le navigateur avertit que les données du formulaire doivent être renvoyées.
- Type de données : Caractères ASCII mais également données binaires.
- Longueur des données : Illimitée.


# 2 - Comparaison méthodes
| GET |POST|
|---|---|
| Visibilité : Visible pour l'utilisateur dans le champ d'adresse | Visibilité : Invisible pour l’utilisateur |
| Marque-page et historique de navigation : Les paramètres de l’URL sont stockés en même temps que l’URL. | Marque-page et historique de navigation : L’URL est enregistrée sans paramètres URL. |
| Cache et fichier log du serveur : Les paramètres de l’URL sont stockés sans chiffrement |Cache et fichier log du serveur : Les paramètres de l’URL ne sont pas enregistrés automatiquement. |
| Comportement lors de l’actualisation du navigateur / Bouton « précédent » :Les paramètres de l’URL ne sont pas envoyés à nouveau. | Cache et fichier log du serveur : Les paramètres de l’URL ne sont pas enregistrés automatiquement. | 
| Type de données : Caractères ASCII uniquement. | Type de données : Caractères ASCII mais également données binaires. |
| Longueur des données : Limitée - longueur maximale de l’URL à 2 048 caractères.| Longueur des données : Illimitée. |

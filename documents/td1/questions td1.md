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

# 3 -Extensible
- Comme il est extensible, il est utilisé non seulement pour transmettre des documents hypertextes HTTP, mais aussi des images ou des vidéos, ou encore pour envoyer des données ou du contenu à des serveurs, comme dans le cas des formulaires. La méthode HTTP est à la base de tout échange de données sur le Web.

- Le fait que HTTP soit qualifié de protocole sans état signifie qu'à chaque requête, le serveur ne conserve aucune information sur les interactions précédentes avec le client. En d'autres termes, chaque requête HTTP est indépendante, et le serveur ne se "souvient" pas de ce qui s'est passé auparavant.

# 4 -Sans état

Le fait que HTTP soit qualifié de protocole sans état signifie qu'à chaque requête, le serveur ne conserve aucune information sur les interactions précédentes avec le client. En d'autres termes, chaque requête HTTP est indépendante, et le serveur ne se "souvient" pas de ce qui s'est passé auparavant.

Conséquences pour la navigation Web :

* Gestion de sessions : Pour maintenir une continuité entre les interactions, comme rester connecté à un site, des mécanismes comme les cookies, les sessions ou les tokens sont nécessaires. Ces outils permettent de "mémoriser" l'état entre les requêtes, malgré le caractère sans état de HTTP.

* Sécurité améliorée : L'absence de stockage d'informations entre les requêtes réduit la surface d'attaque pour les pirates. Cependant, cela nécessite une gestion prudente des mécanismes comme les cookies pour éviter les vulnérabilités.

* Scalabilité : Le caractère sans état de HTTP facilite la scalabilité des applications web. Comme le serveur n'a pas besoin de stocker l'état de chaque utilisateur, il peut traiter un grand nombre de requêtes simultanément sans surcharge liée à la gestion d'états multiples.



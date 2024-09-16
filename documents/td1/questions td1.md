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

# 5 -URL

https://github.com/Mathiss07/bloc1/edit/main/documents/td1/questions%20td1.md

Une URL commence par le protocole https:// ensuite vient le nom de domaine par exemple https://github.com , le ".com" est le TLD pour Top-Level Domain puis vient le chemin d'accès ici /Mathiss07/bloc1/edit/main/documents/td1/questions%20td1/ et pour finir avec l'extension ".md"

# 6 -Codes Status

Les codes de statut HTTP se décomposent en 5 grandes familles :

* Un code 1xx indique une réponse provisoire (non implémenté avec HTTP/1.0) ;

* Un code 2xx (200, 201, 202, 204) indique que la requête a été traitée avec succès ;

* Un code 3xx(300, 301, 302, 304) indique que la requête doit être redirigée ;

* Un code 4xx (400, 401, 403, 404) indique une erreur côté client ;

* Un code 5xx (500, 501, 502, 503) indique une erreur côté serveur.

# 7 -Négociation de contenu

La négociation de contenu en HTTP est un processus par lequel un serveur web détermine la meilleure représentation d'une ressource à renvoyer en fonction des préférences exprimées par le client (navigateur web). Ce mécanisme permet de répondre aux divers besoins et capacités des clients, comme la langue, le format ou l'encodage des données.

# 10 –Headers

| En-tête            | Description                                                                 | Exemple d'utilisation                                           |
|--------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| **Host**           | Indique le nom de domaine du serveur (et éventuellement le numéro de port). | `Host: www.exemple.com`                                          |
| **User-Agent**     | Identifie le client (navigateur, application) qui envoie la requête.         | `User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)`         |
| **Accept**         | Spécifie les types de contenu que le client peut traiter.                   | `Accept: text/html, application/json`                           |
| **Accept-Language**| Indique les langues préférées du client pour le contenu de la réponse.      | `Accept-Language: fr-FR, en-US`                                 |
| **Accept-Encoding**| Indique les encodages de contenu que le client peut décompresser.           | `Accept-Encoding: gzip, deflate`                                |
| **Content-Type**   | Indique le type de média du corps de la requête, lorsque le client envoie des données au serveur. | `Content-Type: application/json`             |
| **Authorization**  | Contient les informations d'authentification pour accéder à une ressource protégée. | `Authorization: Basic YWxhZGRpbjpvcGVuc2VzYW1l`        |
| **Referer**        | Indique l'URL de la page précédente à partir de laquelle la requête a été envoyée. | `Referer: https://www.google.com`                       |
| **Cookie**         | Envoie les cookies du client au serveur pour l'identification de la session ou d'autres informations d'état. | `Cookie: sessionId=abc123; theme=dark`             |
| **Cache-Control**  | Indique les directives de gestion du cache pour la requête.                 | `Cache-Control: no-cache`                                      |

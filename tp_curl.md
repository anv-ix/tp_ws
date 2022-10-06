# TP curl - comprendre les requêtes et les réponses HTTP

Pour les questions suivantes, vous devez utiliser l'url suivante : https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe

Pour tous les appels vous devez ajouter un header pour identifier votre appel parmis ceux des autres étudiants : x-student : VOTRE_NOM

## Faire un appel curl : copier la commande exécutée et indiquer la requête et la réponse
LA REQUETE : 
	curl https://webhook.site/d4ec90aa-8173-48dd-8414-6fb832ea2a26 -H "x-student:Anis"

## Quel est la version du protocole utilisé par le serveur ?
LA REQUETE :
	curl -I  https://webhook.site/d4ec90aa-8173-48dd-8414-6fb832ea2a26
LA VERSION est http/1.1 :
HTTP/1.1 200 OK
Server: nginx
Content-Type: text/plain; charset=UTF-8
Vary: Accept-Encoding
X-Request-Id: 27a53a54-fb83-45f6-9c4e-5146bce81f71
X-Token-Id: d4ec90aa-8173-48dd-8414-6fb832ea2a26
Cache-Control: no-cache, private
Date: Thu, 22 Sep 2022 12:29:26 GMT

## Quels sont les headers que l'on envoie dans la requête ? Quels sont leur sens ?
LA REQUETE : 
	curl -v  https://webhook.site/d4ec90aa-8173-48dd-8414-6fb832ea2a26 -H "x-student:Anis"

LES HEADERS : 
> Host: webhook.site		: Spécifie le nom de domaine
> User-Agent: curl/7.81.0	: Permet d'identifier le nom de l'application, le systeme d'exploitation, la version, la langue,...etc
> Accept: */*	:permet de specifier quel est le type de contenue que le client peut comprende et il est exprimé avec la norme MIME( qui est une norme qui définit la nature est le format d'un document )
> x-student:Anis

## Quelles informations pouvez-vous trouver à propos du certificat SSL ?
les informations à propos du SSL sont :
	le type du tls utilisépour se connecter
	certificat SSL

## Quel est le code de la réponse ? Que signifie-t-il ?
Le code de la réponse est : 200 et cela signifie que la requete est parfaite.

## Quels headers recevez vous dans la response ? Quels sont leur sens ?
Server: nginx : renvoie le nom du serveur
Content-Type : renvoie le type des données retournées
Transfer-Encoding : spécifie la forme de codage utilisée pour transférer en toute sécurité le corps de la charge utile à l'utilisateur
Vary : Il est utilisé par le serveur pour indiquer quels en-têtes sont utilisés pour représenter une resource dans un algorithme
X-Request-Id : c'est un identifiant que le client crée de façon aléatoire et que le serveur utilise ensuite dans chaque instruction du journal qu'il crée.
X-Token-Id :
Cache-Control : des instructions pour controler la mise en cache dans les navigateurs, et caches partagées. 
Date:
## Faire un appel curl en envoyant du texte brut : copier la commande exécutée et indiquer la requête et la réponse
curl https://webhook.site/d4ec90aa-8173-48dd-8414-6fb832ea2a26 -H "x-student: Anis" -H "Content-Type: text/plain" -v -X POST --data "Texte"

reponse :
* Connected to webhook.site (46.4.105.116) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
*  CAfile: /etc/ssl/certs/ca-certificates.crt
*  CApath: /etc/ssl/certs
* TLSv1.0 (OUT), TLS header, Certificate Status (22):
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.2 (IN), TLS header, Certificate Status (22):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS header, Finished (20):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Finished (20):
* TLSv1.2 (OUT), TLS header, Finished (20):
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.3 (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
* ALPN, server did not agree to a protocol
* Server certificate:
*  subject: CN=webhook.site
*  start date: Jul 31 23:09:19 2022 GMT
*  expire date: Oct 29 23:09:18 2022 GMT
*  subjectAltName: host "webhook.site" matched cert's "webhook.site"
*  issuer: C=US; O=Let's Encrypt; CN=R3
*  SSL certificate verify ok.
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
> POST /37f00faa-5d4f-4572-97a8-2db3c5b785c5 HTTP/1.1
> Host: webhook.site
> User-Agent: curl/7.81.0
> Accept: */*
> x-student: Anis
> content-Type: text/plain
> Content-Length: 6
> 
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* old SSL session ID is stale, removing
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Server: nginx
< Content-Type: text/plain; charset=UTF-8
< Transfer-Encoding: chunked
< Vary: Accept-Encoding
< X-Request-Id: 5b44b245-3524-4662-954f-533f60a01097
< X-Token-Id: 37f00faa-5d4f-4572-97a8-2db3c5b785c5
< Cache-Control: no-cache, private
< Date: Thu, 06 Oct 2022 13:05:20 GMT
< 
* Connection #0 to host webhook.site left intact


## Faire un appel curl en envoyant du JSON (avec les bons headers) : copier la commande exécutée et indiquer la requête et la réponse
curl https://webhook.site/37f00faa-5d4f-4572-97a8-2db3c5b785c5 -H "x-student: Anis" -H "Content-Type: application/json" -v -X POST -d '{"login":"abcdefg1","password":"1234567a"}'

*   Trying 46.4.105.116:443...
* Connected to webhook.site (46.4.105.116) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
*  CAfile: /etc/ssl/certs/ca-certificates.crt
*  CApath: /etc/ssl/certs
* TLSv1.0 (OUT), TLS header, Certificate Status (22):
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.2 (IN), TLS header, Certificate Status (22):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS header, Finished (20):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Finished (20):
* TLSv1.2 (OUT), TLS header, Finished (20):
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.3 (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
* ALPN, server did not agree to a protocol
* Server certificate:
*  subject: CN=webhook.site
*  start date: Jul 31 23:09:19 2022 GMT
*  expire date: Oct 29 23:09:18 2022 GMT
*  subjectAltName: host "webhook.site" matched cert's "webhook.site"
*  issuer: C=US; O=Let's Encrypt; CN=R3
*  SSL certificate verify ok.
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
> POST /37f00faa-5d4f-4572-97a8-2db3c5b785c5 HTTP/1.1
> Host: webhook.site
> User-Agent: curl/7.81.0
> Accept: */*
> x-student: Anis
> Content-Type: application/json
> Content-Length: 42
> 
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* old SSL session ID is stale, removing
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Server: nginx
< Content-Type: text/plain; charset=UTF-8
< Transfer-Encoding: chunked
< Vary: Accept-Encoding
< X-Request-Id: c3da8ed0-31f0-46a6-846c-cef4c31f5def
< X-Token-Id: 37f00faa-5d4f-4572-97a8-2db3c5b785c5
< Cache-Control: no-cache, private
< Date: Thu, 06 Oct 2022 13:07:57 GMT
< 
* Connection #0 to host webhook.site left intact


## Faire une appel curl en envoyant une basic authentication en utilisant 2 méthodes différentes : copier les commandes exécutées et indiquer la requête et la réponse à chaque fois 


## Exécuter la commande suivante avec la méthode GET puis indiquer la réponse : curl https://demo.api-platform.com/books/07dd4786-aaa7-4d08-a467-076b76f1d1b6 


## Exécuter la commande suivante avec la méthode PATCH  puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1


## Quel est le code HTTP reçu ? Quel est sa signification ?


## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1


## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/9999


## Quel est le code HTTP ? Que signifie-t-il ?


## Exécuter la requête suivante et copier la réponse : curl https://google.fr


## Quel est le code HTTP reçu ? Pouvez-vous expliquer cette réponse ?


## Comment éviter cette réponse ? Trouvez 2 solutions différentes et détaillez les.

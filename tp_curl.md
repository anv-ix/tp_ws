# TP curl - comprendre les requêtes et les réponses HTTP

Pour les questions suivantes, vous devez utiliser l'url suivante : https://webhook.site/d4ec90aa-8173-48dd-8414-6fb832ea2a26

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


## Faire un appel curl en envoyant du texte brut : copier la commande exécutée et indiquer la requête et la réponse


## Faire un appel curl en envoyant du JSON (avec les bons headers) : copier la commande exécutée et indiquer la requête et la réponse


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

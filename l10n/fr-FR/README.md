# Comment configurer le serveur SMTP ?

Par défaut, APITable ne configure pas le serveur SMTP, ce qui signifie que vous ne pouvez pas inviter des utilisateurs car il nécessite la fonctionnalité d'envoi de courriels.

Il est nécessaire de modifier la configuration `.env` à l'aide de l'email et de redémarrer le serveur backend.

```conf
MAIL_ENABLED=true
MAIL_HOST=smtp.xxx.com
MAIL_PASSWORD=your_email_password
MAIL_PORT=465
MAIL_SSL_ENABLE=true
MAIL_TYPE=smtp
MAIL_USERNAME=your_email
```

J'ajoute quelque chose : `
xxa=xsd
kdsfds=lok`

De plus, certaines boîtes aux lettres doivent être activées en arrière-plan pour utiliser smtp. Pour plus de détails, vous pouvez rechercher le tutoriel Smtp de la boîte aux lettres xxx.


## Problème de performance sous macOS M1 docker run?

## Où est la documentation de l'API?

Vous pouvez accéder à la documentation de l'API en lançant un serveur local :

1. L'adresse de la documentation du serveur Backend est : <http://localhost:8081/api/v1/doc.html>

2. L'adresse de documentation du serveur de la salle est : <http://localhost:3333/nest/v1/docs>

Si vous êtes intéressé par les interfaces API du service cloud, vous pouvez également accéder directement à la documentation de l'API en ligne sur <https://developers.apitable.com/api/introduction>.

## Comment définir la limitation de la quantité de widget dans le tableau de bord ? (30 par défaut)

Ceci peut être réalisé en définissant le paramètre `DSB_WIDGET_MAX_COUNT` dans le fichier `.env`.

## Puis-je augmenter la limite de taux de demande de l'IPA? (5 par défaut)

Dans le fichier `.env.default` de `room-server`, il y a deux paramètres qui peuvent ajuster la fréquence de la requête :

1. Vous pouvez définir `LIMIT_POINTS` et `LIMIT_DURATION` pour indiquer le nombre de requêtes qui peuvent être faites dans une période de temps unitaire. Lorsque LIMIT_POINTS est le nombre de fois et que LIMIT_DURATION est la durée, mesurée en secondes.

2. Vous pouvez définir le paramètre `LIMIT_WHITE_LIST` pour définir une fréquence de requête séparée pour des utilisateurs spécifiques. Sa valeur est une chaîne JSON, et sa structure peut se référer à `Map<string, IBaseRateLimiter>`.

## Comment augmenter le nombre d'enregistrements insérés par appel API ? (10 par défaut)

Ceci peut être réalisé en définissant le paramètre `API_MAX_MODIFY_RECORD_COUNTS` dans le fichier `.env.default` du `room-server`.


## Comment mettre à jour vers la version la plus récente ?


## Comment changer le port 80 par défaut ?

Les propriétés de configuration dans le fichier `.env` peuvent également être remplacées en les spécifiant vars env `NGINX_HTTP_PORT`

Par exemple. Il serait défini comme NGINX_HTTP_PORT=8080

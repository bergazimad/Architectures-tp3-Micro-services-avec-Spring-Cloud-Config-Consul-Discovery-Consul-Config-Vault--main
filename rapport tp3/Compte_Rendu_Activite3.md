![Image associée](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.001.jpeg)**Ecole Normale Supérieure de l’Enseignement Technique Mohammedia**

**Université Hassan II de Casablanca**

ﺍ ﻟﻤﺪﺭﺳﺔﺍﻟﻌﻠﻴﺎﻸﺳﺎﺗﺬﺓﺍﻟﺘﻌﻠﻴﻢﺍﻟﺘﻘﻨﻲالمحمدية ﺟﺎﻣﻌﺔﺍﻟﺤﺴﻦﺍﻟﺜﺎﻧﻲﺑﺎﻟﺪﺍﺭﺍﻟﺒﻴﻀﺎﺀ






# **Architectures Micro services avec (Spring Cloud Config, Consul Discovery, Consul Config,Vault)**


![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.002.jpeg)











**Travail à faire**

Création d’une application de e-commerce basée sur les micro services:

Consul Discovery Spring Cloud Config Spring Cloud Gateway Customer-service Inventory Service Order Service

Consul Config (Billing Service) Vault (Billing Service) Frontend Web avec Angular

17
![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.003.png)
# **PARTIE 1 : Configuration des microservices**

1. ![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.004.png)**Démarrer le service Consul Discovery.**
1. **Activer le service de configuration des microservices:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.005.jpeg)

1. **Création d’un dossier contient les fichiers de configuration des ms :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.006.png)


1. **Configuration partagée par les microservices :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.007.png)

1. **Exemple de configuration (Customer-service) :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.008.jpeg)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.009.png)![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.010.png)

1. **Configuration de service de configuration crée :**

On va stocker la configuration de l'ensemble de microservices dans (repository git en local), Quand le service de configuration démarre va chercher dans le repository où se trouve la configuration de l'ensemble de microservices.

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.011.png)

1. **Démarrer le service de configuration :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.012.png)


# **PARTIE 2 : Création de Gateway**

1. **Configuration automatique de Gateway :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.013.jpeg)

1. **Configuration automatique de Gateway :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.014.jpeg)


# **PARTIE 3 : Création de customer-service**

1. **Structure du projet:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.015.png)

1. **Configuration de service :**

Le service customer-service va chercher sa configuration dans le service de configuration config-service qui a le port 8888

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.016.png)

1. **Entité de Customer:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.017.png)

1. **Repository de customer-service:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.018.png)

1. **Récupérer la configuration de customer-service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.019.jpeg)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.020.png)

1. **Tester le customer-service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.021.png)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.022.jpeg)


# **PARTIE 4 : Création de inventory-service**

1. **Configuration de service :**

Le service inventory-service va chercher sa configuration dans le service de configuration config- service qui a le port 8888

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.023.png)

1. **Entité de Product :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.024.png)

1. **Projection de inventory -service:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.025.jpeg)

1. **Tester le inventory -service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.026.jpeg)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.027.jpeg)

# **PARTIE 5 : Création de order-service**

1. **Structure du projet :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.028.png)

1. **Configuration de service :**

Le service order-service va chercher sa configuration dans le service de configuration config-service qui a le port 8888

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.029.png)

Sa configuration dans le répertoire de configuration :

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.030.jpeg)

1. **Entité de Order:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.031.jpeg)

1. **Entité ProductItem:**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.032.jpeg)

1. **Les modules utilisés dans order-service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.033.png)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.034.jpeg)

1. **Communiquer le order-service avec customer-service avec OpenFeign :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.035.jpeg)

1. **Récupérer le customer et la liste des produits d’order :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.036.jpeg)

1. **Tester le order-service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.037.png)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.038.jpeg)

# **PARTIE 6 : Création de billing-service**

1. **Dépendances :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.039.png)

1. **Structure de billing-service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.040.png)

1. **Configuration de billing-service :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.041.png)

1. **Partager le secret avec Vault :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.042.png)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.043.png)

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.044.png)

Les paramètres de configuration dans Consul Config

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.045.jpeg)

Contrôleur de test des secrets :

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.046.jpeg)![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.047.jpeg)


Dans cette situation le microservice billing-service le seul qui a le secret, il veut le partager avec les autres microservices mais il ne fait pas confiance, c’est pour cela, il va le donner à Vault, c’est comme ça il est sûr que seules les microservices qui ont droit d’accès à Vault qui peuvent le voir comme ça on partage les secrets.

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.048.jpeg)![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.049.png)


# **PARTIE 7 : Frontend avec Angular**

1. ![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.050.png)**Liste des produits :**

1. ![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.051.png)**Liste des customer :**
1. **Liste des order de customer 1 :**

![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.052.png)

1. ![](Aspose.Words.b83d2707-2baa-4c9c-8e47-47279270064b.053.png)**Détails de order 5 :**

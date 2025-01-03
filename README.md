<h1>Activite 3</h1>

<h3> Ordre de l'execution</h3>
<p>
Dicovery, config, customer, inventory, gateway,billing

ensuite : cd ecom-web-app
puis : ng serve
</p>

<h1>Backend Architecture - Spring Boot Microservices</h1>
    <p>Notre application est basée sur Spring Boot, qui utilise des microservices pour gérer les différentes fonctionnalités. L'architecture comprend plusieurs services, chacun ayant un rôle spécifique dans le système global.</p>

<h2>1. Architecture du Projet </h2>

<img src="images/img.png">

<p>L'architecture de l'application backend est composée des services suivants :</p>
    
<ul>
        <li>
            <h3>1.1. customer-service</h3>
            <p>
                Le service <strong>customer-service</strong> gère toutes les opérations liées aux clients. 
                Il permet de créer, lire, mettre à jour et supprimer les informations des clients. 
                Ce service expose des endpoints RESTful qui sont utilisés par d'autres services pour interagir avec les données des clients.
            </p>
        </li>
        <li>
            <h3>1.2. inventory-service</h3>
            <p>
                Le service <strong>inventory-service</strong> est responsable de la gestion de l'inventaire des produits. 
                Il suit les quantités de stock disponibles, met à jour les informations sur les produits, et traite les demandes des utilisateurs concernant les articles en stock.
            </p>
        </li>
        <li>
            <h3>1.3. gateway-service</h3>
            <p>
                Le service <strong>gateway-service</strong> agit comme un point d'entrée pour toutes les demandes externes. 
                Il fonctionne comme un API Gateway qui redirige les requêtes HTTP vers les services appropriés en interne, 
                en offrant également des fonctionnalités telles que la gestion des autorisations et des rôles, ainsi que le routage des requêtes.
            </p>
        </li>
        <li>
            <h3>1.4. discovery-service</h3>
            <p>
                Le service <strong>discovery-service</strong> est basé sur Eureka, une solution de découverte de services. 
                Il permet à chaque microservice de se déclarer automatiquement et de s'enregistrer dans le registre de services Eureka. 
                Il facilite la communication entre les services sans que les URL de chaque service soient codées en dur.
            </p>
        </li>
        <li>
            <h3>1.5. billing-service</h3>
            <p>
                Le service <strong>billing-service</strong> gère les factures des clients. 
                Il permet de générer des factures pour les clients en fonction de leurs achats et de suivre les paiements associés. 
                Ce service expose des endpoints pour récupérer les factures et effectuer des paiements.
            </p>
        </li>
        <li>
            <h3>1.6. config-service</h3>
            <p>
                Le service <strong>config-service</strong> est utilisé pour centraliser et gérer la configuration de tous les microservices. 
                Il permet de stocker les paramètres de configuration dans un dépôt Git ou un autre système de gestion de configuration, 
                et de les distribuer dynamiquement aux services au démarrage.
            </p>
        </li>
</ul>



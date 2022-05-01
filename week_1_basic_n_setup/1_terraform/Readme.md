# Initiation à Terraform et GCP (Google Cloud Platform)

**Pré-requis :** 
- Installer [Terraform](https://www.terraform.io/)
- Avoir un compte Google Cloud Platform
- Installer [GCP SDK](https://cloud.google.com/sdk/docs/install-sdk)

## Terraform


Terraform est un outil qui permet de générer des infrastructures à partir d'un code. C'est ce que l'on appelle un IaC (Infrastructure As a Code). Terraform utilise une méthode déclarative, c'est-à-dire qu'il va contenir les informations nécessaires à la création de notre infrastructure Cloud sous forme de déclaration. Il est possible de l'utiliser avec les trois principaux cloud provider que sont AWS, Azure et GCP. Dans l'exemple suivant, on va l'utiliser avec GCP. Si on veut l'utiliser avec un autre cloud provider, la structure sera identique. Il suffira juste de changer quelques informations. Pour cela, il ne faut pas hésiter à consulter la documentation pour avoir les informations nécessaires. 

Pour construire l'infrastructure dont on a besoin, on va créer des fichiers de configurations : `main.tf` et `variables.tf`. Dans le fichier `main.tf`, on va retrouver les informations des services que l'on souhaite créer en fonction de notre cloud provider. Ici, on va créer un Data Lake (**Google Storage Bucket**) et un Data Warehouse (**Google BigQuery**). Le fichier `variables.tf` va contenir les informations nécessaires à la configuration des différents produits utilisés. 

### Le cycle de vie de Terraform

On va avoir 3 (4 étapes) dans le cycle de vie d'une infrastructure avec Terraform. 

![lifecycle terraform](images/cycle_terraform.png)

#### 1) terraform init

La commande `init` permet de créer un répertoire de travail qui va contenir les informations nécessaires à Terraform. C'est l'équivalent de commande `init` que l'on retrouve dans d'autres outils comme `git init`.

#### 2) terraform plan

La commande `plan` permet de créer le plan d'exécution. Il va se baser sur les informations contenues dans les fichiers de configuration `main.tf` et `variables.tf`.

#### 3) terraform apply

Lors de l'utilisation de la commande `apply`, le plan d'exécution crée au préalable va être mis en place. L'infrastructure va se construire (et se modifier) en se basant sur les informations présentes dans les fichiers de configuration. Si la commande `plan` n'a pas été réalisé avant le plan d'exécution est automatiquement construit. Cette opération prend quelques secondes à être réalisé. 

#### 4) terraform destroy

Enfin lorsque l'on n'a plus besoin de l'infrastructure crée dans le cloud, on va la détruire à l'aide de la commande `destroy`. La destruction d'une infrastructure sur le cloud est recommandée pour éviter la génération de frais supplémentaires lorsqu'on ne l'utilise pas et que sa sauvegarde n'est pas nécessaire. 

## Google Cloud Platform

![GCP_services](images/gcp_services.png)


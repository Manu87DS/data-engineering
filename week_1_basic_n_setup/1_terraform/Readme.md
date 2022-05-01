# Initiation à Terraform et GCP (Google Cloud Platform)

**Pré-requis :** 
- Installer [Terraform](https://www.terraform.io/)
- Avoir un compte Google Cloud Platform
- Installer [GCP SDK](https://cloud.google.com/sdk/docs/install-sdk)

## Terraform


Terraform est un outil qui permet de générer des infrastructures à partir d'un code. C'est ce que l'on appelle un IaC (Infrastructure As a Code). Terraform utilise une méthode déclarative, c'est-à-dire qu'il va contenir les informations nécessaires à la création de notre infrastructure Cloud sous forme de déclaration. Il est possible de l'utiliser avec les trois principaux cloud provider que sont AWS, Azure et GCP. Dans l'exemple suivant, on va l'utiliser avec GCP. Si on veut l'utiliser avec un autre cloud provider, la structure sera identique. Il suffira juste de changer quelques informations. Pour cela, il ne faut pas hésiter à consulter la documentation pour avoir les informations nécessaires. 

Pour construire l'infrastructure dont on a besoin, on va créer des fichiers de configurations : `main.tf` et `variables.tf`. Dans le fichier `main.tf`, on va retrouver les informations des services que l'on souhaite créer en fonction de notre cloud provider. Ici, on va créer un Data Lake (**Google Storage Bucket**) et un Data Warehouse (**Google BigQuery**).

### Le cycle de vie de Terraform

[Cycle_Terraform](/images/cycle_terraform.png)

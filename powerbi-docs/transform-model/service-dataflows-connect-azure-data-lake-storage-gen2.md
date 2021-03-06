---
title: Découvrez comment connecter Azure Data Lake Storage Gen 2 à Power BI pour le stockage de flux de données
description: Utilisez vos propres données pour les flux de données à l’aide d’Azure Data Lake Storage Gen2
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 01/22/2020
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: e24888d4be0a527bd7af6a28fd28795b516b2020
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83309265"
---
# <a name="connect-azure-data-lake-storage-gen2-for-dataflow-storage"></a>Connecter Azure Data Lake Storage Gen2 pour le stockage de dataflows

Vous pouvez configurer des espaces de travail Power BI pour stocker des flux de données dans le compte Azure Data Lake Storage Gen2 de votre organisation. Cet article décrit les étapes générales nécessaires pour ce faire et fournit des conseils et meilleures pratiques tout au long du processus. Il existe quelques avantages à la configuration des espaces de travail pour stocker les définitions de flux de données et les fichiers de données dans votre Data Lake, notamment :

* Azure Data Lake Storage Gen2 fournit un support de stockage des données extrêmement scalable
* Les fichiers de définition et les données de flux de données peuvent être exploités par les développeurs de votre service informatique pour tirer parti d’Azure Data et des services d’intelligence artificielle (AI) comme illustré dans les [exemples GitHub d’Azure Data Services](https://aka.ms/cdmadstutorial)
* Permet aux développeurs de votre organisation d’intégrer les données de flux de données dans les applications internes et les solutions métier, à l’aide des ressources de développeur pour les flux de données et Azure

Pour utiliser Azure Data Lake Storage Gen2 pour les flux de données, vous avez besoin des éléments suivants :

* **Locataire Power BI** : au moins un compte de votre locataire Azure Active Directory (AAD) doit avoir souscrit à Power BI
* **Un compte d’administrateur général** : ce compte est nécessaire pour la connexion et la configuration de Power BI afin de stocker la définition de flux de données, et les données, dans votre compte Azure Data Lake Storage Gen2
* **Un abonnement Azure** : vous avez besoin d’un abonnement Azure pour utiliser Azure Data Lake Storage Gen2
* **Groupe de ressources** : utilisez un groupe de ressources que vous possédez déjà ou créez-en un
* **Un compte de stockage Azure avec la fonctionnalité Data Lake Storage Gen2 activée** 

> [!TIP]
> Si vous n’avez pas d’abonnement Azure, créez un [compte gratuit](https://azure.microsoft.com/free/) avant de commencer.

> [!WARNING]
> Une fois l’emplacement de stockage de flux de données configuré, il n’est pas modifiable. Consultez la section [considérations et limitations](#considerations-and-limitations) près de la fin de cet article pour connaître les autres éléments importants à prendre en compte.

## <a name="prepare-your-azure-data-lake-storage-gen2-for-power-bi"></a>Préparation de votre Azure Data Lake Storage Gen2 pour Power BI

Avant de pouvoir configurer Power BI avec un compte Azure Data Lake Storage Gen2, vous devez créer et configurer un compte de stockage. Jetons un œil à la configuration requise pour Power BI :

1. Vous devez être le propriétaire du compte de stockage ADLS. La qualité de propriétaire doit être affectée au niveau de la ressource, et non héritée du niveau de l’abonnement.
2. Le compte de stockage doit être créé dans le même locataire AAD que votre locataire Power BI.
3. Le compte de stockage doit être créé dans la même région que votre locataire Power BI. Pour savoir où se trouve votre locataire Power BI, consultez [Où est situé mon locataire Power BI ?](../admin/service-admin-where-is-my-tenant-located.md).
4. Le compte de stockage doit avoir la fonctionnalité *Espace de noms hiérarchique* activée.

Les sections suivantes vous guident à travers les étapes nécessaires à la configuration de votre compte Azure Data Lake Storage Gen2.

### <a name="create-the-storage-account"></a>Créer le compte de stockage

Suivez les étapes de l’article [Créer un compte de stockage Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-quickstart-create-account).

1. Assurez-vous de sélectionner le même emplacement que celui de votre locataire Power BI et définissez votre stockage en tant que **StorageV2 (usage général v2)**
2. Veillez à activer la fonctionnalité d’espace de noms hiérarchique
3. Il est recommandé de définir le paramètre de réplication **Stockage géoredondant avec accès en lecture (RA-GRS)**

### <a name="grant-permissions-to-power-bi-services"></a>Accorder des autorisations aux services Power BI

Ensuite, vous devez accorder au service Power BI les rôles Lecteur et Accès aux données sur le compte de stockage que vous avez créé. Comme ce sont deux rôles intégrés, les étapes sont simples. 

Suivez les étapes indiquées dans [Affecter un rôle RBAC intégré](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac#assign-a-built-in-rbac-role).

Dans la fenêtre **Ajouter une attribution de rôle**, sélectionnez le rôle **Lecteur et accès aux données**. Puis, utilisez Rechercher pour localiser l’application **Service Power BI**.
Répétez les mêmes étapes pour le rôle **Propriétaire des données Blob du stockage** et attribuez le rôle aux applications **Service Power BI** et **Power BI Premium**.

> [!NOTE]
> Accordez au moins 30 minutes pour que l’autorisation se propage à Power BI à partir du portail. Chaque fois que vous modifiez des autorisations dans le portail, prévoyez 30 minutes pour que ces autorisations soient reflétées dans Power BI. 

## <a name="connect-your-azure-data-lake-storage-gen2-to-power-bi"></a>Connexion de votre Azure Data Lake Storage Gen2 à Power BI

Une fois que vous avez configuré votre compte Azure Data Lake Storage Gen2 dans le portail Azure, vous le connectez à Power BI dans le **Portail d’administration Power BI**. Vous gérez également le stockage de flux de données Power BI dans la section des paramètres **Stockage de flux de données** du portail d’administration de Power BI. Pour obtenir des conseils sur le lancement et l’utilisation de base, consultez [Guide pratique pour accéder au portail d’administration](../admin/service-admin-portal.md).

Vous connectez votre compte **Azure Data Lake Storage Gen2** en procédant comme suit :

1. Accédez à l’onglet **Paramètres du flux de données** du **Portail d’administration de Power BI**

    ![Portail d’administration Power BI](media/service-dataflows-connect-azure-data-lake-storage-gen2/dataflows-connect-08b.png) 

2. Sélectionnez le bouton **Connecter votre Azure Data Lake Storage Gen2**. La fenêtre suivante s’affiche.

    ![Azure Data Lake Storage Gen2](media/service-dataflows-connect-azure-data-lake-storage-gen2/dataflows-connect-adlsg2_09.jpg) 

3. Fournissez **l’ID d’abonnement** du compte de stockage.
4. Fournissez le **nom du groupe de ressources** dans lequel le compte de stockage a été créé.
5. Fournissez le **nom du compte de stockage**.
6. Sélectionnez **Se connecter**.

Une fois ces étapes terminées, votre compte Azure Data Lake Storage Gen2 est connecté à Power BI. 

> [!NOTE]
> Pour configurer une connexion à Azure Data Lake Storage Gen2 dans le portail d’administration Power BI, vous devez avoir les autorisations d’administrateur général. Toutefois, les administrateurs généraux ne peuvent pas connecter un stockage externe dans le portail d’administration.  

Ensuite, vous devez permettre aux personnes de votre organisation de configurer leurs espaces de travail, ce qui leur permet d’utiliser ce compte de stockage pour le stockage des données et de la définition de flux de données. Nous allons le faire dans la section suivante. 


## <a name="allow-admins-to-assign-workspaces"></a>Autoriser les administrateurs à attribuer des espaces de travail

Par défaut, les fichiers de données et de la définition de flux de données sont stockés dans le stockage fourni par Power BI. Pour accéder aux fichiers de flux de données dans votre propre compte de stockage, les administrateurs de l’espace de travail doivent tout d’abord configurer l’espace de travail pour autoriser l’affectation et le stockage de flux de données dans le nouveau compte de stockage. Avant que l’administrateur d’un espace de travail puisse configurer les paramètres de stockage de flux de données, l’administrateur doit disposer d’autorisations d’attribution de stockage dans le **portail d’administration Power BI**.

Pour accorder des autorisations d’attribution de stockage, accédez à l’onglet **Paramètres de flux de données** dans le **portail d’administration Power BI**. Il existe un bouton radio pour *Autoriser les administrateurs d'espace de travail à attribuer des espaces de travail à ce compte de stockage* qui doit être défini sur **Autoriser**. Une fois ce curseur activé, sélectionnez le bouton **Appliquer** pour que la modification prenne effet. 

![Autoriser les administrateurs à attribuer des espaces de travail](media/service-dataflows-connect-azure-data-lake-storage-gen2/dataflows-connect-adlsg2_10.jpg) 

Voilà. Les administrateurs d’espace de travail Power BI peuvent désormais attribuer des flux de travail au système de fichiers que vous avez créé.


## <a name="considerations-and-limitations"></a>Considérations et limitations

Il s’agit d’une fonctionnalité en préversion, et son comportement peut changer lors de sa mise en production. Voici quelques considérations et limitations à prendre en compte lorsque vous utilisez votre stockage de flux de données :

* Une fois qu’un emplacement de stockage de flux de données est configuré, il ne peut pas être modifié.
* Seuls les propriétaires d’un flux de données stocké dans le stockage Azure Data Lake Storage Gen2 peuvent accéder à ses données par défaut. Pour autoriser d’autres personnes à accéder au flux de données stocké dans Azure, vous devez les ajouter au dossier CDM du flux de données 
* La création de flux de données avec des entités liées est uniquement possible lorsqu’elles sont stockées dans le même compte de stockage
* Les sources de données locales, dans les capacités Power BI partagées, ne sont pas prises en charge dans le flux de données stocké dans le Data Lake de votre organisation
* Les captures instantanées ne sont pas supprimées automatiquement sur ADLS Gen 2. Si vous souhaitez libérer de l’espace, vous pouvez créer une fonction Azure pour nettoyer périodiquement les anciennes captures instantanées.

Il existe également quelques problèmes connus, comme décrit dans cette section.

Les clients de Power BI Desktop ne peuvent pas accéder aux flux de données stockés dans un **compte de stockage Azure Data Lake Storage** , sauf s’ils propriétaires du flux de données ou ont été autorisés dans le dossier CDM dans le Data Lake. Le scénario est le suivant :

1. Anna a créé un espace de travail et l’a configuré pour stocker les dataflows dans le lac de données de l’organisation. 
2. Ben, qui est également membre de l’espace de travail créé par Anna, aimerait tirer parti de Power BI Desktop et du connecteur de flux de données pour obtenir des données à partir du flux de données créé par Anna.
3. Ben reçoit une erreur similaire, car il n’a pas été autorisé à accéder au dossier CDM du flux de données dans le Data Lake.

Questions et réponses courantes :

**Question :** Que se passe-t-il si j’avais précédemment créé des flux de données dans un espace de travail et que je souhaite modifier leur emplacement de stockage ?

**Réponse :** Vous ne pouvez pas modifier l’emplacement de stockage d’un flux de données après sa création. 

**Question :** Quand puis-je modifier l’emplacement de stockage de flux de données d’un espace de travail ?

**Réponse :** La modification de l’emplacement de stockage de flux de données d’un espace de travail est uniquement autorisée si l’espace de travail ne contient aucun flux de données.


## <a name="next-steps"></a>Étapes suivantes

Cet article fournit des conseils sur la façon de se connecter à un Azure Data Lake Gen2 pour le stockage de flux de données. Pour plus d’informations, consultez les articles suivants :

Pour plus d’informations sur les flux de données, le format CDM et Azure Data Lake Storage Gen2, voir les articles suivants :

* [Flux de données et intégration à Azure Data Lake (préversion)](service-dataflows-azure-data-lake-integration.md)
* [Configurer les paramètres de flux de données d’espace de travail (préversion)](service-dataflows-configure-workspace-storage-settings.md)
* [Ajouter un dossier CDM à Power BI comme en tant que flux de données (préversion)](service-dataflows-add-cdm-folder.md)

Pour plus d’informations générales sur les flux de données, consultez les articles suivants :

* [Créer et utiliser des flux de données dans Power BI](service-dataflows-create-use.md)
* [Utilisation d’entités calculées sur Power BI Premium](service-dataflows-computed-entities-premium.md)
* [Utilisation de flux de données avec des sources de données locales](service-dataflows-on-premises-gateways.md)
* [Ressources du développeur pour les flux de données Power BI](service-dataflows-developer-resources.md)

Pour plus d’informations sur le stockage Azure, voir les articles suivants :
* [Guide de sécurité sur le Stockage Azure](https://docs.microsoft.com/azure/storage/common/storage-security-guide)

Pour plus d’informations sur le modèle Common Data Model, vous pouvez lire son article de présentation :
* [Vue d’ensemble du modèle CMD (Common Data Model) ](https://docs.microsoft.com/powerapps/common-data-model/overview)
* [Dossiers CDM](https://go.microsoft.com/fwlink/?linkid=2045304)
* [Définition du fichier model CDM](https://go.microsoft.com/fwlink/?linkid=2045521)

Vous pouvez aussi [poser des questions à la Communauté Power BI](https://community.powerbi.com/).

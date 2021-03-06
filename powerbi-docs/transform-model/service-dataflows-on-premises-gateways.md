---
title: Utilisation de flux de données avec des sources de données locales
description: Guide pratique pour utiliser des données locales dans des flux de données
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 01/08/2020
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: 1008cf34cd09d8039107794e10dcef845ec35110
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83322421"
---
# <a name="using-dataflows-with-on-premises-data-sources"></a>Utilisation de flux de données avec des sources de données locales

Les **flux de données** vous permettent de créer une collection de données à partir de diverses sources, de nettoyer les données, de les transformer, puis de les charger dans le stockage Power BI. Lors de la création de flux de données, vous pouvez utiliser des sources de données locales. Cet article expose la condition associée à la création de flux de données et la façon dont votre **passerelle d’entreprise** doit être configurée pour activer ces connexions.

![Flux de données et passerelles](media/service-dataflows-onpremises-gateways/onpremises-gateways_01.png)

## <a name="configuring-an-enterprise-gateway-for-use-with-dataflows"></a>Configuration d’une passerelle d’entreprise pour une utilisation avec des flux de données

Pour créer un dataflow en utilisant une passerelle, l’utilisateur doit être l’administrateur d’Enterprise Gateway, ou l’administrateur doit avoir partagé la source de données qu’il envisage d’utiliser avec l’utilisateur. 


> [!NOTE]
> Les flux de données sont uniquement pris en charge avec des passerelles d’entreprise.

## <a name="using-an-on-premises-data-source-in-a-dataflow"></a>Utilisation d’une source de données locale dans un flux de données

Lorsque vous créez un flux de données, sélectionnez une source de données locale dans la liste des sources de données, comme indiqué dans l’image suivante.

![Choisir une source de données locale](media/service-dataflows-onpremises-gateways/onpremises-gateways_02a.png)

Après avoir effectué votre sélection, vous êtes invité à fournir les détails de la connexion de la passerelle d’entreprise qui servira à accéder aux données locales. Vous devez sélectionner la passerelle elle-même et fournir des informations d’identification pour la passerelle sélectionnée.

![Fournir les détails de la connexion](media/service-dataflows-onpremises-gateways/onpremises-gateways_03.png)

## <a name="monitoring-your-gateway"></a>Surveillance de votre passerelle

Vous pouvez surveiller un flux de données sur votre passerelle d’entreprise de la même façon que vous surveillez un jeu de données sur des passerelles.

Dans l’écran des paramètres du flux de données de Power BI, vous pouvez surveiller l’état de la passerelle d’un flux de données et affecter une passerelle au flux de données, comme illustré dans l’image suivante.

![Surveillance de la passerelle](media/service-dataflows-onpremises-gateways/onpremises-gateways_01.png)

## <a name="changing-a-gateway"></a>Modification d’une passerelle

Vous pouvez modifier la passerelle d’entreprise utilisée pour un flux de données de deux manières :

1. **À partir de l’outil de création** : vous pouvez modifier la passerelle affectée à toutes vos requêtes à l’aide de l’outil de création de flux de données.

    > [!NOTE]
    > Le flux de données tentera de trouver ou de créer les sources de données requises à l’aide de la nouvelle passerelle. S’il échoue, vous ne pourrez pas modifier la passerelle tant que tous les flux de données nécessaires ne sont pas disponibles à partir de la passerelle sélectionnée.

2. **À partir de l’écran des paramètres** : vous pouvez modifier la passerelle affectée à l’aide de l’écran des paramètres du flux de données dans le service Power BI.

Pour en savoir plus sur les passerelles d’entreprise, consultez [Passerelle de données locale](../connect-data/service-gateway-onprem.md).

## <a name="considerations-and-limitations"></a>Considérations et limitations

Il existe quelques limitations connues concernant l’utilisation de passerelles d’entreprise et de flux de données :

* Chaque flux de données ne peut utiliser qu’une seule passerelle. Par conséquent, toutes les requêtes doivent être configurées à l’aide de la même passerelle.
* La modification de la passerelle impacte l’intégralité du flux de données.
* Si plusieurs passerelles sont nécessaires, la meilleure solution consiste à créer plusieurs flux de données (un pour chaque passerelle) et à utiliser les fonctionnalités de calcul ou de référence d’entité pour unifier les données.
* Les flux de données sont uniquement pris en charge avec des passerelles d’entreprise. Les passerelles personnelles ne pourront pas être sélectionnées dans les listes déroulantes et les écrans de paramètres.


## <a name="next-steps"></a>Étapes suivantes

Cet article fournit des informations sur l’utilisation d’une source de données locale pour des flux de données et explique comment utiliser et configurer des passerelles pour accéder à ces données. Les articles suivants peuvent également vous être utiles

* [Préparation des données en libre-service avec des flux de données](service-dataflows-overview.md)
* [Créer et utiliser des flux de données dans Power BI](service-dataflows-create-use.md)
* [Utilisation d’entités calculées sur Power BI Premium](service-dataflows-computed-entities-premium.md)
* [Ressources du développeur pour les flux de données Power BI](service-dataflows-developer-resources.md)

Pour plus d’informations sur Power Query et l’actualisation planifiée, vous pouvez consulter ces articles :
* [Présentation des requêtes dans Power BI Desktop](desktop-query-overview.md)
* [Configuration d’une actualisation planifiée](../connect-data/refresh-scheduled-refresh.md)

Pour plus d’informations sur le modèle Common Data Model, vous pouvez lire son article de présentation :
* [Vue d’ensemble du modèle CMD (Common Data Model) ](https://docs.microsoft.com/powerapps/common-data-model/overview)

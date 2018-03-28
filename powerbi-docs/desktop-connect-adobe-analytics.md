---
title: "Se connecter à Adobe Analytics dans Power BI Desktop (préversion)"
description: "Découvrez comment vous connecter facilement à Adobe Analytics dans Power BI Desktop pour utiliser les données sous-jacentes"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/09/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: efd6d066e2f98f86248730917c2f4aa0c8a39983
ms.sourcegitcommit: 4217430c3419046c3a90819c34f133ec7905b6e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2018
---
# <a name="connect-to-adobe-analytics-in-power-bi-desktop-preview"></a>Se connecter à Adobe Analytics dans Power BI Desktop (préversion)
Dans **Power BI Desktop**, vous pouvez vous connecter à **Adobe Analytics** et utiliser les données sous-jacentes comme n’importe quelle autre source de données dans Power BI Desktop. 

![Obtenir des données d’Adobe Analytics](media/desktop-connect-adobe-analytics/connect-adobe-analytics_01.png)

## <a name="enable-the-adobe-analytics-connector-preview"></a>Activer la préversion du connecteur Adobe Analytics 
Le connecteur **Adobe Analytics** est actuellement disponible en préversion. Vous devez donc activer cette fonctionnalité en préversion pour que le connecteur s’affiche dans la fenêtre **Obtenir des données**. Pour activer la préversion du connecteur, sélectionnez **Fichier > Options et paramètres > Options > Fonctionnalités en préversion** dans Power BI Desktop, puis cochez la case à côté de **Signets**. 

![Activer la préversion du connecteur Adobe Analytics dans Options](media/desktop-connect-adobe-analytics/connect-adobe-analytics_02.png)

Vous devrez redémarrer **Power BI Desktop** après avoir activé la préversion du connecteur Adobe Analytics.

## <a name="connect-to-adobe-analytics-data"></a>Se connecter aux données Adobe Analytics
Pour vous connecter aux données **Adobe Analytics**, sélectionnez **Obtenir des données** dans le ruban **Accueil** de Power BI Desktop. Sélectionnez **Services en ligne** dans les catégories à gauche pour afficher le **connecteur Adobe Analytics**.

![Obtenir des données d’Adobe Analytics](media/desktop-connect-adobe-analytics/connect-adobe-analytics_01.png)

Dans la fenêtre **Adobe Analytics** qui s’affiche, sélectionnez le bouton **Se connecter**, puis entrez vos informations d’identification pour vous connecter à votre compte Adobe Analytics. La fenêtre de connexion Adobe s’affiche, comme ci-dessous.

![Se connecter à Adobe Analytics](media/desktop-connect-adobe-analytics/connect-adobe-analytics_03.png)

Lorsque vous y êtes invité, indiquez votre nom d’utilisateur et votre mot de passe. Une fois que la connexion est établie, vous pouvez prévisualiser et sélectionner différentes dimensions et mesures dans la boîte de dialogue **Navigateur** de Power BI pour créer une sortie tabulaire. Vous pouvez également spécifier les paramètres d’entrée nécessaires pour les éléments sélectionnés. 

![Sélectionner des données à l’aide du navigateur](media/desktop-connect-adobe-analytics/connect-adobe-analytics_04.png)

Vous pouvez **charger** la table sélectionnée, ce qui permet d’afficher la table entière dans **Power BI Desktop**, ou **modifier** la requête, ce qui permet d’ouvrir l’**éditeur de requête**. Vous pouvez ainsi filtrer et affiner l’ensemble de données que vous souhaitez utiliser, puis charger ce jeu de données affiné dans **Power BI Desktop**.

![Charger ou modifier des données dans le navigateur](media/desktop-connect-adobe-analytics/connect-adobe-analytics_05.png)


## <a name="next-steps"></a>Étapes suivantes
Vous pouvez connecter toutes sortes de données à l’aide de Power BI Desktop. Pour plus d’informations sur les sources de données, consultez les ressources suivantes :

* [Prise en main de Power BI Desktop](desktop-getting-started.md)
* [Sources de données dans Power BI Desktop](desktop-data-sources.md)
* [Mettre en forme et combiner des données dans Power BI Desktop](desktop-shape-and-combine-data.md)
* [Se connecter à des classeurs Excel dans Power BI Desktop](desktop-connect-excel.md)   
* [Entrer des données directement dans Power BI Desktop](desktop-enter-data-directly-into-desktop.md)   

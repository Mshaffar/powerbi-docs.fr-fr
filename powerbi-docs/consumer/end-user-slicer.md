---
title: Utilisation de segments dans le service Power BI
description: Un segment Power BI constitue un autre moyen de réduire la partie du jeu de données affichée dans les autres visualisations d’un rapport.
author: v-thepet
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 04/06/2020
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: a4bd02e21d6985dfe3684f9f209e7f43a45c6271
ms.sourcegitcommit: 2cb249fc855e369eed1518924fbf026d5ee07eb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2020
ms.locfileid: "83812907"
---
# <a name="slicers-in-the-power-bi-service"></a>Segments dans le service Power BI

[!INCLUDE[consumer-appliesto-ynnn](../includes/consumer-appliesto-yynn.md)]

![comparaison de deux sélections différentes sur un segment horizontal](media/end-user-slicer/power-bi-slider.png)

Un segment est un type de visuel qui filtre les autres visuels sur une page de rapport. Vous découvrirez de nombreux types de segments lors de l’utilisation des rapports Power BI. L’image ci-dessus montre le même segment, mais avec des sélections différentes. Notez que chaque sélection filtre les autres visuels de la page.  


## <a name="how-to-use-slicers"></a>Comment utiliser des segments ?
Lors de la création de rapports, les *concepteurs* ajoutent des segments pour aider à raconter une histoire et vous fournir des outils afin d’explorer vos données.

### <a name="numeric-range-slicer"></a>Sélecteur de plages numériques
 Le segment de plages numériques, ci-dessus, vous permet d’explorer le total des ventes par géographie, unités en stock et date de commande. Utilisez les poignées pour sélectionner une plage. 

![poignées d’un segment de plages](media/end-user-slicer/power-bi-handles.png)

### <a name="basic-vertical-checkbox-slicer"></a>Segment de case à cocher vertical de base

Dans un segment de case à cocher de base, cochez une ou plusieurs cases pour voir l’impact sur les autres visuels de la page. Pour en cocher plusieurs, utilisez Ctrl-Sélection. Parfois, le *concepteur* de rapports configure le segment pour vous autoriser à sélectionner une seule valeur à la fois. 

![segment vertical de base](media/end-user-slicer/power-bi-basic.png)

### <a name="image-and-shape-slicers"></a>Segments d’image et de forme
Quand les options du segment sont des images ou des formes, vous devez procéder comme avec des cases à cocher. Vous pouvez choisir une ou plusieurs images ou formes pour appliquer le segment aux autres visuels de la page. 

![segment d’image](media/end-user-slicer/power-bi-image.png)    

![segment horizontal](media/end-user-slicer/power-bi-horizontal.png)    

![segment de forme](media/end-user-slicer/power-bi-boxes.png)

### <a name="hierarchy-slicer"></a>Segment de hiérarchie

Dans un segment avec une hiérarchie, utilisez les chevrons pour développer et réduire la hiérarchie. L’en-tête est mis à jour pour afficher vos sélections.

![segment de hiérarchie](media/end-user-slicer/power-bi-hierarchy.png)

### <a name="relative-time-slicer"></a>Segment de temps relatif
Avec les nouveaux scénarios d’actualisation rapide, la capacité à filtrer sur une plus petite fenêtre de temps peut être très utile.
À l’aide du segment de temps relatif, vous pouvez appliquer des filtres basés sur le temps à toutes les données de date ou d’heure de votre rapport. Vous pouvez par exemple utiliser le segment de temps relatif pour montrer uniquement le nombre de vues de vidéos au cours des deux derniers jours, heures ou même minutes. 

![segment de temps relatif](media/end-user-slicer/power-bi-relative-time.png)

## <a name="deactivate-a-slicer"></a>Désactiver un segment
Pour désactiver un segment, sélectionnez l’icône de gomme.

![icône de gomme](media/end-user-slicer/power-bi-eraser.png)

## <a name="next-steps"></a>Étapes suivantes
Pour plus d’informations, consultez les articles suivants :

[Types de visualisation dans Power BI](end-user-visualizations.md)


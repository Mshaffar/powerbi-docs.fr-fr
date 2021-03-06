---
title: Supprimer un tableau de bord, un rapport, un classeur, un jeu de données ou un espace de travail
description: Découvrir comment supprimer pratiquement tout élément de Power BI
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 09/11/2018
ms.author: maggies
LocalizationGroup: Common tasks
ms.openlocfilehash: 3fdb969888d023ca9683c2460086f2fb8157c3c3
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83304550"
---
# <a name="delete-almost-anything-in-power-bi-service"></a>Supprimer pratiquement tout élément dans le service Power BI
Cet article explique comment supprimer un tableau de bord, un rapport, un classeur, un jeu de données, une application, une visualisation ou un espace de travail dans le service Power BI.

## <a name="delete-a-dashboard"></a>Supprimer un tableau de bord
Vous pouvez supprimer des tableaux de bord. La suppression du tableau de bord n’entraîne pas celle du jeu de données sous-jacent ou des rapports éventuellement associés à ce tableau de bord.

* Si vous êtes le propriétaire du tableau de bord, vous pouvez le supprimer. Si vous avez partagé le tableau de bord avec des collègues, sa suppression de votre espace de travail Power BI a pour effet de l’effacer également de leur espace de travail Power BI.
* Si on a partagé un tableau de bord avec vous et que vous ne voulez plus le voir, vous pouvez l’effacer.  Le fait d’effacer un tableau de bord n’a pas pour effet de l’effacer de l’espace de travail Power BI de quiconque.
* Si un tableau de bord fait partie d’un [pack de contenu d’organisation](../collaborate-share/service-organizational-content-pack-disconnect.md), le seul moyen de le supprimer est de supprimer le jeu de données associé.

### <a name="to-delete-a-dashboard"></a>Pour supprimer un tableau de bord
1. Dans votre espace de travail, sélectionnez l’onglet **Tableaux de bord**.
2. Recherchez le tableau de bord à supprimer et sélectionnez l’icône Supprimer ![icône supprimer](media/service-delete/power-bi-delete-icon.png).

    ![vidéo](media/service-delete/power-bi-delete-dash.gif)

## <a name="delete-a-report"></a>Supprimer un rapport
La suppression d’un rapport ne doit pas être une source d’inquiétudes : cette opération ne supprime pas le jeu de données sur lequel est basé le rapport.  De même, les visualisations que vous avez épinglées à partir du rapport sont aussi préservées : elles restent sur le tableau de bord tant que vous ne les supprimez pas individuellement.

### <a name="to-delete-a-report"></a>Pour supprimer un rapport :
1. Dans votre espace de travail, sélectionnez l’onglet **Rapports**.
2. Recherchez le rapport à supprimer et sélectionnez l’icône Supprimer   ![icône supprimer](media/service-delete/power-bi-delete-icon.png).   

    ![onglet Rapports d’un espace de travail](media/service-delete/power-bi-delete-reportnew.png)
3. Confirmez la suppression.

   ![boîte de dialogue Supprimer le rapport](media/service-delete/power-bi-delete-report.png)

   > [!NOTE]
   > si le rapport fait partie d’un [pack de contenu](../collaborate-share/service-organizational-content-pack-introduction.md), vous ne pourrez pas le supprimer en employant cette méthode.  Voir [Suppression de votre connexion à un pack de contenu d’organisation](../collaborate-share/service-organizational-content-pack-disconnect.md).
   >
   >

## <a name="delete-a-workbook"></a>Supprimer un classeur
Vous pouvez supprimer des classeurs. Toutefois, la suppression d’un classeur a également pour effet de supprimer l’ensemble des rapports et vignettes de tableau de bord contenant des données de ce classeur.

Si le classeur est stocké sur OneDrive Entreprise, sa suppression de Power BI n’a pas pour effet de le supprimer de OneDrive.

### <a name="to-delete-a-workbook"></a>Pour supprimer un classeur
1. Dans votre espace de travail, sélectionnez l’onglet **Classeurs**.
2. Recherchez le classeur à supprimer et sélectionnez l’icône Supprimer ![icône supprimer](media/service-delete/power-bi-delete-report2.png) .

    ![onglet Classeurs](media/service-delete/power-bi-delete-workbooknew.png)
3. Confirmez la suppression.

   ![boîte de dialogue Supprimer le classeur](media/service-delete/power-bi-delete-confirm.png)

## <a name="delete-a-dataset"></a>Supprimer un jeu de données
Vous pouvez supprimer des jeux de données. Toutefois, la suppression d’un jeu de données a également pour effet de supprimer l’ensemble des rapports et vignettes de tableau de bord contenant des données de ce jeu de données.

Si un jeu de données fait partie d’un ou plusieurs [packs de contenu d’organisation](../collaborate-share/service-organizational-content-pack-disconnect.md), la seule manière de le supprimer est de le retirer des packs de contenu dans lesquels il est utilisé, d’attendre la fin du traitement de l’opération, puis de réessayer de le supprimer.

### <a name="to-delete-a-dataset"></a>Pour supprimer un jeu de données
1. Dans votre espace de travail, sélectionnez l’onglet **Jeux de données**.
2. Localisez le jeu de données à supprimer, puis sélectionnez **Plus d’options** (…).  

    ![onglet Jeux de données](media/service-delete/power-bi-delete-datasetnew.png)
3. Dans la liste déroulante, sélectionnez **Supprimer**.

   ![menu des points de suspension](media/service-delete/power-bi-delete-datasetnew2.png)
4. Confirmez la suppression.

   ![boîte de dialogue Supprimer le tableau de bord](media/service-delete/power-bi-delete-dataset-confirm.png)

## <a name="delete-a-workspace"></a>Supprimer un espace de travail
> [!WARNING]
> Quand vous créez un espace de travail, vous créez un groupe Office 365. Quand vous supprimez un espace de travail, vous supprimez ce groupe Office 365. Cela signifie que le groupe est également supprimé des autres produits Office 365 comme SharePoint et Microsoft Teams.
>
>

En tant que créateur de l’espace de travail, vous pouvez le supprimer. Lorsque vous le supprimez, l’application associée est également supprimée pour tous les membres du groupe et supprimée de votre AppSource si vous l’aviez publiée pour toute l’organisation. Supprimer un espace de travail n’est pas quitter un espace de travail.

### <a name="to-delete-a-workspace---if-you-are-an-admin"></a>Pour supprimer un espace de travail - si vous êtes administrateur
1. Dans le volet de navigation, sélectionnez **Espaces de travail**.

2. Sélectionnez **Plus d’options** (...) à droite de l’espace de travail à supprimer, puis choisissez **Modifier l’espace de travail**.

    ![espaces de travail](media/service-delete/power-bi-delete-workspace.png)

3. Dans la fenêtre **Modifier l’espace de travail**, sélectionnez **Supprimer l’espace de travail** > **Supprimer**.

    ![supprimer l’espace de travail](media/service-delete/power-bi-delete-workspace2.png)

### <a name="to-remove-a-workspace-from-your-list"></a>Pour supprimer un espace de travail de votre liste
Si vous ne voulez plus être membre d’un espace de travail, vous pouvez le ***quitter*** : il est alors supprimé de votre liste. Lorsque vous quittez un espace de travail, celui-ci reste en place pour tous ses autres membres.  

> [!IMPORTANT]
> Si vous êtes l’unique administrateur de l’espace de travail, Power BI ne vous autorise pas à quitter celui-ci.
>
>

1. Démarrez dans l’espace de travail que vous voulez supprimer.

2. Dans le coin supérieur droit, sélectionnez **Plus d’options** (…), puis choisissez **Quitter l’espace de travail** > **Quitter**.

      ![quitter l’espace de travail](media/service-delete/power-bi-leave-workspace.png)

   > [!NOTE]
   > Les options qui apparaissent dans la liste déroulante varient selon que vous êtes administrateur ou membre de cet espace de travail.
   >
   >

## <a name="delete-or-remove-an-app"></a>Supprimer ou retirer une application
Vous pouvez facilement supprimer des applications de la page de votre liste d’applications. En revanche, seul un administrateur d’une application peut supprimer celle-ci définitivement.

### <a name="remove-an-app-from-your-app-list-page"></a>Supprimer une application de la page de votre liste d’applications
La suppression d’une application de la page de votre liste d’applications n’a pas pour effet de supprimer l’application pour les autres membres.

1. Dans le volet de navigation, sélectionnez **Applications** pour ouvrir la page de la liste d’applications.
2. Pointez sur l’application à supprimer, puis sélectionnez l’icône Supprimer ![](media/service-delete/power-bi-delete-report2.png).

   ![sélectionner Applications](media/service-delete/power-bi-delete-app.png)

   Si vous supprimez accidentellement une application, vous disposez de plusieurs options pour la récupérer.  Vous pouvez demander au créateur de l’application de la renvoyer, rechercher l’e-mail d’origine contenant le lien vers l’application, consulter votre [centre de notifications](../consumer/end-user-notification-center.md) pour voir si la notification relative à cette application y figure toujours, ou vérifier l’[AppSource de votre organisation](../consumer/end-user-apps.md).

## <a name="considerations-and-troubleshooting"></a>Considérations et résolution des problèmes
Cet article a expliqué comment supprimer les principaux blocs de construction principaux du service Power BI. Mais il existe d’autres éléments que vous pouvez supprimer dans Power BI.  

* [Supprimer votre tableau de bord par défaut](../consumer/end-user-featured.md)
* [Retirer un tableau de bord des favoris](../consumer/end-user-favorite.md)
* [Supprimer une page de rapport](service-delete.md)
* [Supprimer une vignette de tableau de bord](service-dashboard-edit-tile.md)
* [Supprimer une visualisation de rapport](service-delete.md)

D’autres questions ? [Posez vos questions à la communauté Power BI](https://community.powerbi.com/)

---
title: Portail d’administration Power BI
description: Le portail d’administration permet de gérer les clients Power BI de votre organisation. Il comprend notamment des métriques d’utilisation, un accès au Centre d’administration Microsoft 365 et des paramètres.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 04/27/2020
ms.author: kfollis
ms.custom: seodec18
LocalizationGroup: Administration
ms.openlocfilehash: b08184e92730bd3a42a91424883d07cecec82549
ms.sourcegitcommit: a72567f26c1653c25f7730fab6210cd011343707
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83564469"
---
# <a name="administering-power-bi-in-the-admin-portal"></a>Administration de Power BI dans le portail d’administration

Le portail d’administration vous permet de gérer un *client* Power BI pour votre organisation. Le portail comprend notamment des métriques d’utilisation, un accès au Centre d’administration Microsoft 365 et des paramètres.

Le portail d’administration est accessible dans son intégralité à tous les utilisateurs qui sont administrateurs généraux ou qui se sont vus attribuer le rôle d’administrateur de service Power BI. Si vous n’appartenez pas à l’un de ces rôles, seuls les **Paramètres de capacité** s’affichent sur le portail. Pour plus d’informations sur le rôle d’administrateur de Service Power BI, voir [Présentation du rôle d’administrateur Power BI](service-admin-role.md).

## <a name="how-to-get-to-the-admin-portal"></a>Accès au portail d’administration

Pour obtenir l’accès au portail d’administration Power BI, votre compte doit être un compte **d’Administrateur général** dans Microsoft 365 ou Azure Active Directory (Azure AD), ou le rôle d’Administrateur de service Power BI doit lui avoir été assigné. Pour plus d’informations sur le rôle d’administrateur de Service Power BI, voir [Présentation du rôle d’administrateur Power BI](service-admin-role.md). Pour accéder au portail d’administration Power BI, procédez comme suit.

1. Sélectionnez l’icône des paramètres représentant une roue dentée, située en haut à droite de l’écran Power BI.

1. Sélectionnez **Portail d’administration**.

    ![Paramètres du portail d’administration](media/service-admin-portal/powerbi-admin-settings.png)

Le portail compte neuf onglets. Le reste de cet article fournit des informations sur chacun de ces onglets.

![Navigation dans le portail d’administration](media/service-admin-portal/powerbi-admin-landing-page.png)

* [Métriques d’utilisation](#usage-metrics)
* [Utilisateurs](#users)
* [Journaux d’audit](#audit-logs)
* [Paramètres du locataire](#tenant-settings)
* [Paramètres de capacité](#capacity-settings)
* [Codes incorporés](#embed-codes)
* [Visuels de l’organisation](#organizational-visuals)
* [Stockage de dataflows (préversion)](#dataflowStorage)
* [Espaces de travail](#workspaces)
* [Marque personnalisée](#custom-branding)

## <a name="usage-metrics"></a>Métriques d'utilisation

Les **Métriques d’utilisation** vous permettent de superviser l’utilisation de Power BI dans votre organisation. Il permet également de voir les utilisateurs et les groupes de votre organisation qui sont les plus actifs dans Power BI. 

> [!NOTE]
> La première fois que vous accédez au tableau de bord ou si vous y accédez de nouveau après une longue période, un écran de chargement s’affiche probablement pendant le chargement du tableau de bord.

Une fois le tableau de bord chargé, vous voyez deux sections de vignettes. La première section comprend des données d’utilisation pour chacun des utilisateurs ; la deuxième comporte des informations similaires pour les groupes de votre organisation.

Voici le détail de ce que vous pouvez voir dans chaque vignette :

* Le nombre de tableaux de bord, de rapports et de jeux de données de l’espace de travail utilisateur.
  
    ![Nombre de tableaux de bord, de rapports et de jeux de données](media/service-admin-portal/powerbi-admin-usage-metrics-number-tiles.png)

* Le tableau de bord le plus utilisé par nombre d’utilisateurs autorisés à y accéder. Par exemple, si vous disposez d’un tableau de bord que vous avez partagé avec 3 utilisateurs et que vous l’avez aussi ajouté à un pack de contenu auquel sont connectés deux autres utilisateurs, le nombre d’utilisateurs s’élève à 6 (1 + 3 + 2).
  
    ![Tableaux de bord les plus utilisés](media/service-admin-portal/powerbi-admin-usage-metrics-top-dashboards.png)

* Le contenu auquel est connecté le plus grand nombre d’utilisateurs. Il peut s’agir de tout ce que les utilisateurs peuvent obtenir via le processus Obtenir des données, autrement dit, des packs de contenu SaaS, des packs de contenu d’organisation, des fichiers ou des bases de données.
  
    ![Packages les plus utilisés](media/service-admin-portal/powerbi-admin-usage-metrics-top-connections.png)

* Vue des utilisateurs les plus actifs, en fonction du nombre de tableaux de bord qu’ils possèdent, à la fois ceux qu’ils ont créés eux-mêmes et ceux qui ont été partagés avec eux.
  
    ![Utilisateurs les plus actifs - tableaux de bord](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-dashboards.png)

* Vue des utilisateurs les plus actifs, en fonction du nombre de rapports qu’ils possèdent.
  
    ![Utilisateurs les plus actifs - rapports](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-reports.png)

La deuxième section affiche le même type d’informations, mais pour les groupes. Vous pouvez ainsi voir quels sont les groupes les plus actifs dans votre organisation et le type de contenu qu’ils utilisent.

Ces informations vous procurent des insights tangibles sur la façon dont les employés de votre organisation utilisent Power BI et vous permettent d’identifier les utilisateurs et les groupes les plus actifs.

## <a name="control-usage-metrics"></a>Contrôler les métriques d’utilisation

Les rapports de métriques d’utilisation sont une fonctionnalité qu’un administrateur Power BI ou Microsoft 365 peut activer ou désactiver. Les administrateurs ont un contrôle granulaire sur l’accès des utilisateurs aux métriques d’utilisation. Ils sont **Activés** par défaut pour tous les utilisateurs de l’organisation.

Les administrateurs peuvent aussi déterminer si les créateurs de contenu peuvent voir les données par utilisateur dans les métriques d’utilisation. 

Pour plus d’informations sur les rapports eux-mêmes, consultez [Superviser les métriques d’utilisation de tableaux de bord et de rapports Power BI](../collaborate-share/service-usage-metrics.md).

### <a name="usage-metrics-for-content-creators"></a>Métriques d'utilisation pour les créateurs de contenu

1. Dans le portail d’administration, sélectionnez **Paramètres du client** > **Métriques d’utilisation pour les créateurs de contenu**.

    ![Métriques d’utilisation dans les paramètres du locataire sur le portail d’administration](media/service-admin-portal/power-bi-admin-usage-metrics.png)

1. Activez (ou désactivez) les métriques d’utilisation > **Appliquer**.

    ![métriques d’utilisation activées](../collaborate-share/media/service-usage-metrics/power-bi-tenant-settings-updated.png)


### <a name="per-user-data-in-usage-metrics"></a>Données par utilisateur dans les métriques d’utilisation

Par défaut, les données par utilisateur sont activées pour les métriques d’utilisation et les informations des comptes des consommateurs des contenus sont incluses dans le rapport des métriques. Si vous ne souhaitez pas inclure ces informations pour tout ou partie des utilisateurs, désactivez la fonctionnalité pour des groupes de sécurité spécifiés ou pour l’ensemble de l’organisation. Les informations de compte figurent alors dans le rapport sous l’intitulé *Sans nom*.

![Données d’utilisation par utilisateur](media/service-admin-portal/power-bi-admin-per-user-usage-data.png)

### <a name="delete-all-existing-usage-metrics-content"></a>Supprimer tous le contenu des métriques d’utilisation existantes

Lors de la désactivation des métriques d’utilisation pour leur organisation toute entière, les administrateurs peuvent également choisir une ou plusieurs options pour :

- **Supprimer tout le contenu des métriques d’utilisation** pour supprimer toutes les vignettes de rapports et de tableaux de bord existantes générées à l’aide de rapports et de jeux de données des métriques d’utilisation. Cette option supprime tout accès aux données de métriques d’utilisation pour tous les utilisateurs au sein de l’organisation qui peuvent déjà les utiliser. 
- **Supprimer toutes les données existantes par utilisateur dans le contenu des métriques d’utilisation actuelles** : Cette option supprime tout accès aux données par utilisateur pour tous les utilisateurs de l’organisation qui les utilisent peut-être déjà. 

Soyez prudent, car la suppression du contenu de métriques existantes d’utilisation et par utilisateur est irréversible.

## <a name="users"></a>Utilisateurs

Les utilisateurs, les groupes et les administrateurs Power BI sont gérés dans le Centre d’administration Microsoft 365. L’onglet **Utilisateurs** contient un lien qui donne accès au Centre d’administration pour votre client.

![Accéder au Centre d’administration Microsoft 365](media/service-admin-portal/powerbi-admin-manage-users.png)

## <a name="audit-logs"></a>Journaux d'audit

Les journaux d’audit Power BI sont gérés dans le Centre de sécurité et de conformité Office 365. L’onglet **Journaux d’audit** contient un lien qui donne accès au Centre de sécurité et de conformité pour votre client. [En savoir plus](service-admin-auditing.md)

Pour utiliser les journaux d’audit, vérifiez que le paramètre [**Créer des journaux d’audit pour l’audit et la conformité des activités internes**](#create-audit-logs-for-internal-activity-auditing-and-compliance) est activé.

## <a name="tenant-settings"></a>Paramètres du locataire

L’onglet **Paramètres du client** permet un contrôle affiné sur les fonctionnalités mises à la disposition de votre organisation. Si vous avez des inquiétudes à propos de vos données sensibles, il se peut que certaines de nos fonctionnalités ne soient pas adaptées à votre organisation. Vous pouvez aussi choisir de mettre à disposition une fonctionnalité déterminée à un groupe précis.

L’image suivante présente plusieurs paramètres de l’onglet **Paramètres du client**.

![Paramètres du locataire](media/service-admin-portal/powerbi-admin-tenant-settings.png)

> [!NOTE]
> Jusqu’à 10 minutes peuvent être nécessaires à la prise en compte de la modification d’un paramètre pour tous les utilisateurs de votre client.

Les paramètres peuvent avoir trois états :

* **Désactivé pour toute l’organisation** : Personne dans votre organisation ne peut utiliser cette fonctionnalité.

    ![Paramètre Désactivé pour tous](media/service-admin-portal/powerbi-admin-tenant-settings-disabled.png)

* **Activé pour toute l’organisation** : Tout le monde dans votre organisation peut utiliser cette fonctionnalité.

    ![Paramètre Activé pour tous](media/service-admin-portal/powerbi-admin-tenant-settings-enabled.png)

* **Activé pour une partie de l’organisation** : Un sous-ensemble spécifique d’utilisateurs ou de groupes de votre organisation peut utiliser la fonctionnalité en question.

    Vous pouvez activer la fonctionnalité pour toute votre organisation à l’exception d’un groupe spécifique d’utilisateurs.

    ![Paramètre Activé pour un sous-ensemble](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except.png)

    Vous pouvez aussi activer la fonctionnalité uniquement pour un groupe d’utilisateurs spécifique, mais aussi la désactiver pour un autre groupe d’utilisateurs. Cette approche permet de faire en sorte que certains utilisateurs n’ont pas accès à la fonctionnalité, même s’ils se trouvent dans le groupe autorisé.

    ![Paramètre d’activation sélective](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except2.png)

Les sections suivantes fournissent une vue d’ensemble des différents types de paramètres de locataire.

## <a name="help-and-support-settings"></a>Paramètres d’aide et de support

### <a name="publish-get-help-information"></a>Publier des informations « Obtenir de l’aide »

Les utilisateurs dans l’organisation peuvent accéder à l’aide interne et aux ressources de support dans le menu d’aide de Power BI. Plus précisément, ces paramètres changent le comportement des éléments du menu Apprendre, Communauté et Obtenir de l’aide.

De plus, en spécifiant une URL pour les demandes de licences, vous personnalisez l’URL cible du bouton **Mettre à niveau le compte**. Les utilisateurs qui n’ont pas de licence Power BI Pro voient ce bouton dans la boîte de dialogue **Mettre à niveau vers Power BI Pro** ainsi que dans la page **Gérer le stockage personnel**. Par ailleurs, Power BI ne présente plus le bouton **Essayez gratuitement la version Pro** dans cette boîte de dialogue ni dans cette page du stockage. Ainsi, Power BI guidera les utilisateurs de manière fiable tout au long des processus définis dans votre organisation par le biais de votre solution de gestion des licences.

![Paramètre d’activation sélective](media/service-admin-portal/powerbi-admin-tenant-settings-gethelp.png)

### <a name="receive-email-notifications-for-service-outages-or-incidents"></a>Recevoir des notifications par e-mail pour les pannes ou incidents du service

Les groupes de sécurité à extension messagerie reçoivent des notifications par e-mail si ce locataire est affecté par une panne ou un incident du service. En savoir plus sur les [notifications d’interruption de service](service-interruption-notifications.md).

## <a name="workspace-settings"></a>Paramètres de l’espace de travail

Dans **Paramètres du locataire**, le portail d’administration comporte deux sections pour le contrôle des espaces de travail :

- Créez les nouvelles expériences d'espace de travail.
- Utilisez des jeux de données entre des espaces de travail.

### <a name="create-the-new-workspaces"></a>Créer de nouveaux espaces de travail

Les espaces de travail sont des emplacements où les utilisateurs peuvent collaborer sur des tableaux de bord, des rapports et d’autres contenus. Les administrateurs utilisent le paramètre **Créer des espaces de travail (nouvelle expérience d’espace de travail)** pour indiquer quels utilisateurs de l’organisation peuvent créer des espaces de travail. Les administrateurs peuvent autoriser tout le monde ou personne dans une organisation à créer des espaces de travail avec la nouvelle expérience d’espace de travail. Il peuvent également limiter la création aux membres de groupes de sécurité spécifiques. En savoir plus sur les [espaces de travail](../collaborate-share/service-new-workspaces.md)

:::image type="content" source="media/service-admin-portal/power-bi-admin-workspace-settings.png" alt-text="Créer les nouvelles expériences d'espace de travail":::

Pour les espaces de travail classiques basés sur les groupes Microsoft 365, l’administration continue à s’effectuer dans le portail d’administration Microsoft 365 et Azure Active Directory.

> [!NOTE]
> Par défaut, le paramètre **Créer des espaces de travail (nouvelle expérience d’espace de travail)** est défini pour autoriser uniquement les utilisateurs pouvant créer des groupes Microsoft 365 à créer les nouveaux espaces de travail Power BI. Veillez à définir une valeur dans le portail d’administration Power BI pour garantir que les utilisateurs appropriés peuvent les créer.

**Liste des espaces de travail**

Le portail d’administration comporte une autre section de paramètres sur les espaces de travail dans votre locataire. Dans cette section, vous pouvez trier et filtrer la liste des espaces de travail et afficher les détails de chaque espace de travail. Pour plus d’informations, consultez [Espaces de travail](#workspaces), plus loin dans cet article.

**Publier des packs de contenu et des applications**

Dans le portail d’administration, vous contrôlez également les utilisateurs qui disposent des autorisations nécessaires pour distribuer des applications à l’organisation. Consultez la section [Publier des packs de contenu et des applications pour toute l’organisation](#publish-content-packs-and-apps-to-the-entire-organization) de cet article pour plus de détails.

### <a name="use-datasets-across-workspaces"></a>Utiliser des jeux de données entre des espaces de travail

Les administrateurs peuvent contrôler les utilisateurs de l’organisation qui peuvent utiliser des jeux de données dans les espaces de travail. Quand ce paramètre est activé, les utilisateurs ont toujours besoin de l’autorisation de build requise pour un jeu de données spécifique.

:::image type="content" source="media/service-admin-portal/power-bi-admin-datasets-workspaces.png" alt-text="Utiliser des jeux de données entre des espaces de travail":::

Pour en savoir plus, consultez [Introduction aux jeux de données entre plusieurs espaces de travail](../connect-data/service-datasets-across-workspaces.md).


## <a name="export-and-sharing-settings"></a>Paramètres d'exportation et de partage

### <a name="share-content-with-external-users"></a>Partager le contenu avec des utilisateurs externes

Les utilisateurs de l’organisation peuvent partager des tableaux de bord, des rapports et des applications avec des utilisateurs externes à l’organisation. Découvrez plus en détail le [partage externe](../collaborate-share/service-share-dashboards.md#share-a-dashboard-or-report-outside-your-organization).

![Paramètre Utilisateurs externes](media/service-admin-portal/powerbi-admin-sharing-external-02.png)

L’image suivante présente le message qui s’affiche quand vous faites un partage avec un utilisateur externe.

![Partager avec un utilisateur externe](media/service-admin-portal/powerbi-admin-sharing-external.png)  

> [!IMPORTANT]
> Cette option détermine si les utilisateurs de Power BI peuvent inviter des utilisateurs externes à devenir des utilisateurs invités d’Azure Active Directory B2B (Azure AD B2B) dans votre organisation par le biais de Power BI. Lorsque cette option est activée, les utilisateurs qui ont le rôle d’Inviteur d’invités dans Azure AD peuvent ajouter des adresses e-mail externes lors du partage de rapports, de tableaux de bord et d’applications Power BI. Le destinataire externe est invité à rejoindre votre organisation en tant qu’utilisateur invité d’Azure AD B2B. Important : lorsque vous désactivez ce paramètre, les utilisateurs externes qui sont déjà des utilisateurs invités d’Azure AD B2B dans votre organisation continuent à apparaître dans les interfaces utilisateur de sélection de personnes dans Power BI et peuvent avoir accès à des éléments, des espaces de travail et des applications.

### <a name="publish-to-web"></a>Publier sur le web

En tant qu’administrateur d’un locataire Power BI, le paramètre **Publier sur le web** vous propose des options pour lesquelles les utilisateurs peuvent créer des codes incorporés pour publier des rapports sur le web. Cette fonctionnalité rend le rapport et ses données accessibles à n’importe qui sur le web. Découvrez plus d’informations sur la [publication sur le web](../collaborate-share/service-publish-to-web.md).

> [!NOTE]
> Seul les administrateurs Power BI peuvent autoriser la création de codes incorporés « Publier sur le web ». Les organisations peuvent avoir des codes incorporés existants. Consultez la section [Codes incorporés](service-admin-portal.md#embed-codes) du portail d’administration pour passer en revue les rapports actuellement publiés.

L’image suivante montre le menu **Plus d’options (...)** pour un rapport quand le paramètre **Publier sur le web** est activé.

![Publier sur le web dans le menu Plus d’options](media/service-admin-portal/power-bi-more-options-publish-web.png)

Le paramètre **Publier sur le web** du portail d’administration fournit des options pour lesquelles les utilisateurs peuvent créer des codes incorporés.

![Paramètre Publier sur le web](media/service-admin-portal/powerbi-admin-publish-to-web-setting.png)

Les administrateurs peuvent définir **Publier sur le web** sur **Activé** et **Choisir le mode de fonctionnement des codes incorporés** sur **Autoriser seulement les codes incorporés existants**. Dans ce cas, les utilisateurs peuvent créer des codes incorporés, mais ils doivent contacter l’administrateur Power BI pour les y autoriser.

![Invite Publier sur le web](../collaborate-share/media/service-publish-to-web/publish_to_web_admin_prompt.png)

Les options présentées aux utilisateurs dans l’interface utilisateur varient en fonction de la nature du paramètre **Publier sur le web**.

|Caractéristique |Activée pour toute l’organisation |Désactivée pour toute l’organisation |Groupes de sécurité spécifiques   |
|---------|---------|---------|---------|
|**Publier sur le web** sous le menu **Plus d’options (...)** d’un rapport|Activée pour tous|Non visible pour tous|Visible uniquement par les utilisateurs ou groupes autorisés.|
|**Gérer les codes d’incorporation** sous **Paramètres**|Activée pour tous|Activée pour tous|Activée pour tous<br><br>Option * **Supprimer** uniquement pour les utilisateurs ou groupes autorisés.<br>* **Obtenir les codes** activé pour tous.|
|**Codes d’incorporation** au sein du portail d’administration|L’état reflète l’une des options suivantes :<br>* Actif<br>* Non pris en charge<br>* Bloqué|L’état affiche **Désactivé**|L’état reflète l’une des options suivantes :<br>* Actif<br>* Non pris en charge<br>* Bloqué<br><br>Si un utilisateur n’est pas autorisé en fonction du paramètre de locataire, l’état indique **Enfreint**.|
|Rapports publiés existants|Tout activé|Tout désactivé|Les rapports continuent à être restitués pour tous.|

### <a name="export-data"></a>Exporter des données

Les utilisateurs de l’organisation peuvent exporter des données à partir d’une vignette ou d’une visualisation. Cela contrôle l’analyse dans Excel, l’exportation au format .csv, les téléchargements de jeux de données (.pbix) et les fonctionnalités de connexion directe du service Power BI. Découvrez-en plus sur l’[exportation de données à partir d’une vignette ou d’un visuel](../visuals/power-bi-visualization-export-data.md).

>[!NOTE]
> Avant l’introduction du paramètre Exporter vers Excel, ce paramètre contrôlait également l’exportation des données vers des fichiers Excel. Pour plus d’informations, consultez la [remarque sous Exporter vers Excel](#export-to-excel).

![Paramètre Exporter des données](media/service-admin-portal/powerbi-admin-portal-export-data-setting.png)

L’image suivante présente l’option d’exportation de données à partir d’une vignette.

![Exporter des données à partir d’une vignette](media/service-admin-portal/powerbi-admin-export-data.png)

> [!NOTE]
> La désactivation du paramètre **Exporter des données** empêche également les utilisateurs d’utiliser la fonctionnalité [Analyser dans Excel](../collaborate-share/service-analyze-in-excel.md) ainsi que la connexion active du service Power BI.

### <a name="export-to-excel"></a>Exporter vers Excel

Les utilisateurs de l’organisation peuvent exporter les données à partir d’une visualisation dans un fichier Excel.

![Paramètre Exporter vers Excel](media/service-admin-portal/powerbi-admin-portal-export-to-excel-setting.png)

>[!IMPORTANT]
> Avant l’introduction du paramètre Exporter vers Excel, l’exportation vers un fichier Excel était contrôlée par le paramètre Exportation des données. Ainsi, sur les locataires qui existaient avant l’introduction du paramètre Exporter vers Excel, la première fois que les administrateurs de locataires regardent le paramètre Exporter vers Excel, ils voient la présence de *modifications non appliquées*. Ils doivent appliquer ces modifications pour que le nouveau paramètre prenne effet. Dans le cas contraire, l’exportation vers un fichier Excel continue d’être contrôlée par le paramètre Exporter des données.

### <a name="export-reports-as-powerpoint-presentations-or-pdf-documents"></a>Exporter les rapports comme présentations PowerPoint ou documents PDF

Les utilisateurs de l’organisation peuvent exporter des rapports Power BI sous forme de fichiers PowerPoint ou de documents PDF. [En savoir plus](../consumer/end-user-powerpoint.md)

L’image suivante présente le menu **Fichier** qui s’affiche pour un rapport quand le paramètre **Exporter les rapports comme présentations PowerPoint ou documents PDF** est activé.

![Exporter les rapports comme présentations PowerPoint](media/service-admin-portal/powerbi-admin-powerpoint.png)

### <a name="print-dashboards-and-reports"></a>Imprimer des tableaux de bord et des rapports

Les utilisateurs de l’organisation peuvent imprimer des tableaux de bord et des rapports. [En savoir plus](../consumer/end-user-print.md)

L’image suivante présente l’option d’impression d’un tableau de bord.

![Imprimer le tableau de bord](media/service-admin-portal/powerbi-admin-print-dashboard.png)

L’image suivante présente le menu **Fichier** qui s’affiche pour un rapport quand le paramètre **Imprimer des tableaux de bord et des rapports** est activé.

![Imprimer le rapport](media/service-admin-portal/powerbi-admin-print-report.png)

### <a name="allow-external-guest-users-to-edit-and-manage-content-in-the-organization"></a>Autoriser les utilisateurs invités externes à modifier et à gérer le contenu de l’organisation

Les utilisateurs invités Azure AD B2B peuvent modifier et gérer le contenu de l’organisation. [En savoir plus](service-admin-azure-ad-b2b.md)

L’image suivante présente l’option permettant d’autoriser les utilisateurs invités externes à modifier et à gérer le contenu de l’organisation.

![Autoriser les utilisateurs invités externes à modifier et à gérer le contenu de l’organisation](media/service-admin-portal/powerbi-admin-tenant-settings-b2b-guest-edit-manage.png)

Dans le portail d’administration, vous contrôlez également les utilisateurs qui disposent des autorisations nécessaires pour inviter des utilisateurs externes à l’organisation. Pour plus d’informations, consultez [Partager du contenu avec des utilisateurs externes](#export-and-sharing-settings) dans cet article.

### <a name="email-subscriptions"></a>Abonnements par e-mail
Les utilisateurs de l'organisation peuvent créer des abonnements par courrier. En savoir plus sur les [abonnements](../collaborate-share/service-publish-to-web.md).

![Activer les abonnements par courrier](media/service-admin-portal/power-bi-manage-email-subscriptions.png)

### <a name="featured-content"></a>Contenu proposé

Autorisez certains ou tous les auteurs de rapports de votre organisation à présenter leur contenu dans la section À la une de la page d’accueil Power BI. Les nouveaux utilisateurs verront le contenu proposé en haut de leur page d’accueil Power BI. Le contenu proposé descend dans la page d’accueil à mesure que les utilisateurs ajoutent des éléments **favoris**, **fréquents** et **récents**. 

Nous vous recommandons de commencer avec un ensemble réduit d’approbateurs. Permettre à l’ensemble de l’organisation de présenter du contenu dans la page d’accueil peut compliquer le suivi de tout le contenu promu. 

Une fois que vous avez activé le contenu proposé, vous pouvez également le gérer dans le portail d’administration. Consultez [Gérer le contenu proposé](#manage-featured-content) dans cet article pour en savoir plus sur le contrôle du contenu proposé dans votre domaine.

## <a name="content-pack-and-app-settings"></a>Paramètres des applications et des packs de contenu

### <a name="publish-content-packs-and-apps-to-the-entire-organization"></a>Publier des packs de contenu et des applications pour toute l’organisation

Les administrateurs utilisent ce paramètre pour décider si les utilisateurs peuvent publier des packs de contenu et des applications pour toute l’organisation, plutôt que pour des groupes spécifiques uniquement. En savoir plus sur la [publication d’applications](../collaborate-share/service-create-distribute-apps.md).

L’image suivante montre l’option **Toute mon organisation** lors de la création d’un pack de contenu.

![Publier un pack de contenu vers l’organisation](media/service-admin-portal/powerbi-admin-publish-entire-org.png)

### <a name="create-template-apps-and-organizational-content-packs"></a>Créer des modèles d’applications et des packs de contenu d’organisation

Les utilisateurs peuvent créer des modèles d’applications et des packs de contenu d’organisation qui utilisent des jeux de données basés sur une même source de données dans Power BI Desktop. En savoir plus sur les [applications modèles](../connect-data/service-template-apps-create.md).

### <a name="push-apps-to-end-users"></a>Effectuer une transmission de type push des applications pour les utilisateurs finaux

Les auteurs de rapports peuvent partager directement des applications avec les utilisateurs finaux sans installation à partir d’[AppSource](https://appsource.microsoft.com). En savoir plus sur l’[installation automatique d’applications pour les utilisateurs finaux](../collaborate-share/service-create-distribute-apps.md#automatically-install-apps-for-end-users).

## <a name="integration-settings"></a>Paramètres d’intégration

### <a name="use-analyze-in-excel-with-on-premises-datasets"></a>Utiliser Analyser dans Excel avec des jeux de données locaux

Les utilisateurs de l’organisation peuvent utiliser Excel pour afficher et interagir avec des jeux de données Power BI locaux. [En savoir plus](../collaborate-share/service-analyze-in-excel.md)

> [!NOTE]
> La désactivation du paramètre **Exporter des données** empêche également les utilisateurs d’utiliser la fonctionnalité **Analyser dans Excel**.

### <a name="use-arcgis-maps-for-power-bi"></a>Utiliser ArcGIS Maps for Power BI

Les utilisateurs de l’organisation peuvent utiliser la visualisation ArcGIS Maps for Power BI fournie par Esri. [En savoir plus](../visuals/power-bi-visualization-arcgis.md)

### <a name="use-global-search-for-power-bi-preview"></a>Utiliser la recherche générale pour Power BI (préversion)

Les utilisateurs de l’organisation peuvent utiliser les fonctionnalités de recherche externe qui reposent sur le service Recherche Azure.

## <a name="power-bi-visuals-settings"></a>Paramètres des visuels Power BI

### <a name="add-and-use-power-bi-visuals"></a>Ajouter et utiliser des visuels Power BI

Les utilisateurs de l’organisation peuvent manipuler et partager des visuels Power BI. [En savoir plus](../developer/visuals/power-bi-custom-visuals.md)

> [!NOTE]
> Ce paramètre peut s’appliquer à toute l’organisation ou se limiter à des groupes particuliers.

Power BI Desktop (à compter de la version de mars 2019) prend en charge l’utilisation d’une **stratégie de groupe** pour désactiver l’utilisation des visuels Power BI sur les ordinateurs déployés d’une organisation.

<table>
<tr><th>Attribut</th><th>Valeur</th>
</tr>
<td>key</td>
    <td>Software\Policies\Microsoft\Power BI Desktop\</td>
<tr>
<td>valueName</td>
<td>EnableCustomVisuals</td>
</tr>
</table>

La valeur 1 (décimale) active l’utilisation des visuels Power BI dans Power BI (valeur par défaut).

La valeur 0 (décimale) désactive l’utilisation des visuels Power BI dans Power BI.

### <a name="allow-only-certified-visuals"></a>Autoriser uniquement les visuels certifiés

Les utilisateurs de l’organisation qui disposent d’autorisations pour ajouter et utiliser des visuels Power BI, définis par le paramètre « Ajouter et utiliser des visuels Power BI », peuvent uniquement utiliser des [visuels Power BI certifiés](https://go.microsoft.com/fwlink/?linkid=2002010) (les visuels non certifiés sont bloqués et affichent un message d’erreur lorsqu’ils sont utilisés). 


Power BI Desktop (à compter de la version de mars 2019) prend en charge l’utilisation d’une **stratégie de groupe** pour désactiver l’utilisation de visuels Power BI non certifiés sur les ordinateurs déployés d’une organisation.

<table>
<tr><th>Attribut</th><th>Valeur</th>
</tr>
<td>key</td>
    <td>Software\Policies\Microsoft\Power BI Desktop\</td>
<tr>
<td>valueName</td>
<td>EnableUncertifiedVisuals</td>
</tr>
</table>

La valeur 1 (décimale) active l’utilisation de visuels Power BI non certifiés dans Power BI (valeur par défaut).

La valeur 0 (décimale) désactive l’utilisation de visuels Power BI non certifiés dans Power BI (cette option active uniquement l’utilisation de [visuels Power BI certifiés](https://go.microsoft.com/fwlink/?linkid=2002010)).

## <a name="r-visuals-settings"></a>Paramètres des visuels R

### <a name="interact-with-and-share-r-visuals"></a>Utiliser et partager des éléments visuels R

Les utilisateurs de l’organisation peuvent manipuler et partager des visuels créés avec des scripts R. [En savoir plus](../visuals/service-r-visuals.md)

> [!NOTE]
> Ce paramètre s’applique à toute l’organisation et ne peut pas être limité à des groupes en particulier.

## <a name="audit-and-usage-settings"></a>Paramètres d'audit et d'utilisation

### <a name="create-audit-logs-for-internal-activity-auditing-and-compliance"></a>Créer des journaux d'audit pour l'audit des activités internes et la vérification de la conformité

Les utilisateurs de l’organisation peuvent utiliser l’audit pour surveiller les actions effectuées dans Power BI par d’autres utilisateurs de l’organisation. [En savoir plus](service-admin-auditing.md)

Ce paramètre doit être activé pour pouvoir enregistrer les entrées du journal d’audit. Une fois que vous avez activé l’audit, le délai avant de pouvoir voir les données d’audit peut aller jusqu’à 48 heures. Si vous ne voyez immédiatement les données, consultez les journaux d’audit plus tard. Le délai est sensiblement le même entre le moment où vous obtenez l’autorisation de voir les journaux d’audit et le moment où vous pouvez réellement y accéder.

> [!NOTE]
> Ce paramètre s’applique à toute l’organisation et ne peut pas être limité à des groupes en particulier.

### <a name="usage-metrics-for-content-creators"></a>Métriques d'utilisation pour les créateurs de contenu

Les utilisateurs de l’organisation peuvent voir les métriques d’utilisation des tableaux de bord et des rapports qu’ils créent. [En savoir plus](../collaborate-share/service-usage-metrics.md)

### <a name="per-user-data-in-usage-metrics-for-content-creators"></a>Données par utilisateur dans les métriques d'utilisation pour les créateurs de contenu

Les métriques d'utilisation pour créateurs de contenu exposent les noms d'affichage et les adresses e-mail des utilisateurs qui accèdent à du contenu. [En savoir plus](../collaborate-share/service-usage-metrics.md)

Par défaut, les données par utilisateur sont activées pour les métriques d’utilisation et les informations des comptes de créateur de contenu sont incluses dans le rapport des métriques. Si vous ne souhaitez pas recueillir ces informations pour tous les utilisateurs, vous pouvez désactiver la fonctionnalité pour des groupes de sécurité spécifiés ou pour l’ensemble de l’organisation. Les informations de compte des utilisateurs exclus figurent alors dans le rapport sous l’intitulé *Sans nom*.

## <a name="dashboard-settings"></a>Paramètres du tableau de bord

### <a name="data-classification-for-dashboards"></a>Classification des données des tableaux de bord

Les utilisateurs de l’organisation peuvent étiqueter les tableaux de bord avec des classifications indiquant les niveaux de sécurité des tableaux de bord. [En savoir plus](../create-reports/service-data-classification.md)

> [!NOTE]
> Ce paramètre s’applique à toute l’organisation et ne peut pas être limité à des groupes en particulier.

## <a name="developer-settings"></a>Paramètres de développement

### <a name="embed-content-in-apps"></a>Incorporer du contenu dans les applications

Les utilisateurs de l’organisation peuvent incorporer des tableaux de bord et des rapports Power BI dans des applications Saas (Software as a Service). La désactivation de ce paramètre empêche les utilisateurs d’utiliser les API REST pour incorporer du contenu Power BI dans leur application. [En savoir plus](../developer/embedded/embedding.md)

### <a name="allow-service-principals-to-use-power-bi-apis"></a>Autoriser les principaux de service à utiliser les API Power BI

Les applications web inscrites dans Azure Active Directory (Azure AD) utiliseront un principal de service affecté pour accéder aux API Power BI sans utilisateur connecté. Pour pouvoir autoriser une application à utiliser l’authentification du principal de service, il faut que ce dernier fasse partie d’un groupe de sécurité autorisé. [En savoir plus](../developer/embedded/embed-service-principal.md)

> [!NOTE]
> Les principaux de service héritent des autorisations de leur groupe de sécurité pour tous les paramètres du locataire Power BI. Pour limiter les autorisations, créez un groupe de sécurité dédié pour les principaux de service et ajoutez-le à la liste « À l’exception des groupes de sécurité spécifiques » pour les paramètres Power BI pertinents activés.

## <a name="dataflow-settings"></a>Paramètres de dataflow

### <a name="create-and-use-dataflows"></a>Créer et utiliser des dataflows

Les utilisateurs de l'organisation peuvent créer et utiliser des dataflows. Pour une vue d’ensemble des dataflows, consultez [Préparation des données en libre-service dans Power BI](../transform-model/service-dataflows-overview.md). Pour activer les dataflows dans une capacité Premium, consultez [Configurer des charges de travail](service-admin-premium-workloads.md).

> [!NOTE]
> Ce paramètre s’applique à toute l’organisation et ne peut pas être limité à des groupes en particulier.

## <a name="template-apps-settings"></a>Paramètres des applications modèles

Trois paramètres contrôlent la capacité des applications modèles à publier ou installer des applications modèles.

![Paramètres des applications modèles dans le portail d’application Power BI](media/service-admin-portal/power-bi-admin-portal-template-apps.png)

### <a name="publish-template-apps"></a>Publier des applications modèles

Les utilisateurs de l'organisation peuvent créer des espaces de travail d’applications modèles. Choisissez quels utilisateurs peuvent publier des applications modèles ou les distribuer à des clients extérieurs à votre organisation via [AppSource](https://appsource.microsoft.com) ou d’autres méthodes de distribution.

![Portail d’administration Power BI, paramètre Créer des applications modèles](media/service-admin-portal/power-bi-admin-portal-template-app-settings.png)

### <a name="install-template-apps-listed-on-appsource"></a>Installer des applications modèles répertoriées sur AppSource

Les utilisateurs de l’organisation peuvent télécharger et installer des applications modèles **uniquement** depuis [AppSource](https://appsource.microsoft.com). Choisissez quels utilisateurs spécifiques ou groupes de sécurité peuvent installer des applications modèles depuis AppSource.

![Portail d’administration Power BI, paramètre Installer des applications modèles](media/service-admin-portal/power-bi-admin-portal-template-app-settings-installer-appsource.png)

### <a name="install-template-apps-not-listed-on-appsource"></a>Installer des applications modèles non répertoriées sur AppSource

Choisissez quels utilisateurs dans l’organisation peuvent télécharger et installer des applications modèles **non répertoriées sur [AppSource](https://appsource.microsoft.com)** .

![Portail d’administration Power BI, paramètre Installer des applications modèles](media/service-admin-portal/power-bi-admin-portal-template-app-settings-installer-nonappsource.png)

## <a name="capacity-settings"></a>Paramètres de capacité

### <a name="power-bi-premium"></a>Power BI Premium

L’onglet **Power BI Premium** vous permet de gérer les capacités Power BI Premium (EM ou SKU P) achetées pour votre organisation. Tous les utilisateurs dans votre organisation peuvent voir l’onglet **Power BI Premium**, mais ne peuvent en voir le contenu que s’ils disposent d’autorisations *d’administrateur de capacité* ou d’autorisations d’affectation. Si un utilisateur ne possède aucune autorisation, le message suivant apparaît.

![Aucun accès aux paramètres Premium](media/service-admin-portal/premium-settings-no-access.png)

### <a name="power-bi-embedded"></a>Power BI Embedded

L’onglet **Power BI Embedded** vous permet d’afficher les capacités de Power BI Embedded (référence SKU A) que vous avez achetées pour votre client. Dans la mesure où vous ne pouvez acheter des références SKU A qu’à partir d’Azure, vous [gérez les capacités incorporées dans Azure](../developer/embedded/azure-pbie-create-capacity.md) depuis **le portail Azure**.

Pour plus d’informations sur la gestion des paramètres de Power BI Embedded (référence SKU A), consultez [Qu’est-ce que Power BI Embedded](../developer/embedded/azure-pbie-what-is-power-bi-embedded.md).

## <a name="embed-codes"></a>Codes incorporés

En tant qu’administrateur, vous pouvez afficher les codes incorporés générés pour votre tenant pour partager publiquement les rapports. Vous pouvez également révoquer ou supprimer des codes. [En savoir plus](../collaborate-share/service-publish-to-web.md)

![Codes incorporés au sein du portail d’administration Power BI](media/service-admin-portal/embed-codes.png)

 ## <a name=""></a><a name="organizational-visuals">Visuels de l’organisation</a> 

L’onglet **Visuels de l’organisation** vous permet de déployer et de gérer des visuels Power BI au sein de votre organisation. Avec les visuels d’organisation, vous pouvez facilement déployer des visuels propriétaires dans votre organisation, que les auteurs de rapports peuvent ensuite détecter et importer dans leurs rapports à partir de Power BI Desktop. [En savoir plus](../developer/visuals/power-bi-custom-visuals-organization.md)

> [!WARNING]
> Un visuel personnalisé est susceptible de contenir du code présentant des risques pour la sécurité ou la confidentialité ; vérifiez que vous faites confiance à son auteur et à sa source avant de le déployer dans le référentiel de l’organisation.

L’image suivante affiche tous les visuels Power BI actuellement déployés dans le référentiel d’une organisation.

![Visuel de l’administrateur de l’organisation](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-01.png)

### <a name="add-a-new-custom-visual"></a>Ajouter un visuel personnalisé

Pour ajouter un nouveau visuel personnalisé à la liste, procédez comme suit. 

1. Dans le volet droit, sélectionnez **Ajouter un visuel personnalisé**.

    ![Formulaire des visuels Power BI](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-02.png)

1. Renseignez le formulaire **Ajouter un visuel personnalisé** :

    * **Choisir un fichier .pbiviz** (obligatoire) : sélectionnez un fichier visuel personnalisé à charger. Seuls les visuels Power BI d’API avec version sont pris en charge (lisez ici ce que cela signifie).

    Avant de charger un visuel personnalisé, examinez-le afin de déterminer s’il présente un risque en matière de sécurité et de confidentialité et s’il répond aux standards de votre organisation.

    * **Nommer vos visuels personnalisés** (obligatoire) : donnez un titre court au visuel pour que les utilisateurs de Power BI Desktop comprennent facilement ce qu’il fait

    * **Icône** : Il s’agit du fichier d’icône qui s’affiche dans l’interface utilisateur de Power BI Desktop.

    * **Description** : rédigez une brève description du visuel pour donner plus de contexte et d’informations à l’utilisateur

1. Sélectionnez **Ajouter** pour lancer la requête de chargement. Si elle aboutit, le nouvel élément s’affiche dans la liste. En cas d’échec, vous recevez le message d’erreur correspondant.

### <a name="delete-a-custom-visual-from-the-list"></a>Supprimer un visuel personnalisé de la liste

Sélectionnez l’icône de la corbeille pour supprimer définitivement le visuel du référentiel.

> [!IMPORTANT]
> La suppression est irréversible. Le rendu du visuel supprimé disparaît immédiatement des rapports existants. Même si vous chargez le même visuel à nouveau, il ne remplace celui qui a été supprimé. Toutefois, les utilisateurs peuvent réimporter le nouveau visuel et remplacer l’instance présente dans leurs rapports.

### <a name="disable-a-custom-visual-in-the-list"></a>Désactiver un visuel personnalisé dans la liste

Pour désactiver le visuel à partir du magasin de l’organisation, sélectionnez l’icône d’engrenage. Dans la section **Accès**, désactivez le visuel personnalisé.

Après la désactivation du visuel, son rendu ne s’affiche plus dans les rapports existants et le message d’erreur suivant s’affiche.

*Ce visuel personnalisé n’est plus disponible. Pour plus d’informations, contactez votre administrateur.*

Toutefois, les visuels marqués d’un signet continuent à fonctionner.

Après une mise à jour ou un changement d’administrateur, les utilisateurs de Power BI Desktop doivent redémarrer l’application ou actualiser le navigateur dans le service Power BI pour voir les mises à jour.

### <a name="update-a-visual"></a>Mettre à jour un visuel

Pour mettre à jour le visuel à partir du magasin de l’organisation, sélectionnez l’icône d’engrenage. Parcourez et chargez une nouvelle version du visuel.

Assurez-vous que l’ID du visuel reste inchangé. Le nouveau fichier remplace le fichier précédent pour tous les rapports au sein de l’organisation. Toutefois, si la nouvelle version du visuel est susceptible de rompre l’utilisation ou la structure de données de la version précédente du visuel, alors ne remplacez pas la version précédente. Au lieu de cela, vous devez créer une nouvelle liste pour la nouvelle version du visuel. Par exemple, ajoutez un nouveau numéro de version (version X.X) au titre du nouveau visuel répertorié. Ainsi, il est clair qu’il s’agit du même visuel, avec un numéro de version mis à jour, ce qui permet de ne pas rompre les fonctionnalités des rapports existants. Encore une fois, assurez-vous que l’ID du visuel reste inchangé. Puis, la prochaine fois que les utilisateurs entrent dans le référentiel de l’organisation à partir de Power BI Desktop, ils peuvent importer la nouvelle version et sont alors invités à remplacer la version déjà présente dans leur rapport.

Pour plus d’informations, consultez [Questions fréquentes sur les visuels Power BI d’une organisation](../developer/visuals/power-bi-custom-visuals-faq.md#organizational-power-bi-visuals)

## <a name=""></a><a name="dataflowStorage">Stockage de dataflows (préversion)</a>

Par défaut, les données utilisées avec Power BI sont stockées dans le stockage interne offert par Power BI. Avec l’intégration entre les flux de données et Azure Data Lake Storage Gen2 (ADLS Gen2), vous pouvez stocker vos flux de données dans le compte Azure Data Lake Storage Gen2 de votre organisation. Pour plus d’informations, consultez [Flux de données et intégration à Azure Data Lake (préversion)](../transform-model/service-dataflows-azure-data-lake-integration.md).

## <a name="workspaces"></a>Espaces de travail

En tant qu’administrateur, vous pouvez afficher les espaces de travail qui existent dans votre locataire. Vous pouvez trier et filtrer la liste des espaces de travail et afficher les détails de chaque espace de travail. Les colonnes de la table correspondent aux propriétés retournées par l’[API REST administrateur Power BI](/rest/api/power-bi/admin) pour les espaces de travail. Les espaces de travail personnels sont de type **PersonalGroup**, les espaces de travail classiques sont de type **Group**, et les nouveaux espaces de travail modernes sont de type **Workspace**. Pour plus d’informations, consultez [Organiser le travail dans les nouveaux espaces de travail](../collaborate-share/service-new-workspaces.md).

Les administrateurs peuvent également gérer et récupérer des espaces de travail à l’aide du portail d’administration ou des applets de commande PowerShell. 

![Liste des espaces de travail](media/service-admin-portal/workspaces-list.png)

Sous l’onglet **Espaces de travail**, vous voyez l’*état* pour chaque espace de travail. Le tableau suivant fournit plus de détails sur la signification de ces états.

|État  |Description  |
|---------|---------|
| Actif | Un espace de travail normal. Il n’indique rien sur l’utilisation ou ce qui se trouve à l’intérieur, mais seulement le fait que l’espace de travail lui-même est « normal ». |
| Orphelin | Un espace de travail sans administrateur. |
| Supprimé | Un espace de travail supprimé. Pendant un délai pouvant atteindre 90 jours, nous conservons suffisamment de métadonnées pour restaurer l’espace de travail si nécessaire. |
| Suppression | Un espace de travail en cours de suppression, mais qui n’est pas encore supprimé. Les utilisateurs peuvent supprimer leurs propres espaces de travail, en plaçant les éléments en Suppression, puis en Supprimé. |

## <a name="custom-branding"></a>Marque personnalisée

En tant qu’administrateur, vous pouvez personnaliser l’apparence de Power BI pour l’ensemble de votre organisation. Actuellement, il existe trois options principales :

![Options de marque personnalisée](media/service-admin-portal/power-bi-custom-branding.png)

* **Télécharger le logo** : Pour de meilleurs résultats, téléchargez un logo enregistré au format .png de 10 ko ou moins et d’au moins 200 x 30 pixels.

* **Télécharger l’image de couverture** : Pour de meilleurs résultats, téléchargez une image de couverture enregistrée au format .jpg ou .png de 1 Mo ou moins, et d’au moins 1920 x 160 pixels.

* **Sélectionner la couleur du thème** : Vous pouvez sélectionner votre thème en fonction d’une valeur hexadécimale # RVB ou de la palette fournie.


Pour plus d’informations, consultez [Marque personnalisée pour votre organisation](https://aka.ms/orgBranding).

![Liste des espaces de travail](media/service-admin-portal/workspaces-list.png)

## <a name="manage-featured-content"></a>Gérer le contenu proposé

En tant qu’administrateur de locataire, vous pouvez gérer tous les rapports, les tableaux de bord et les applications qui ont été promus dans la section À la une de la page d’accueil Power BI à l’échelle de votre organisation.

- Dans le portail d’administration, sélectionnez **Contenu proposé**.

Vous y trouverez ici une vue d’ensemble des personnes qui ont proposé le contenu, du moment où il a été proposé et de toutes les métadonnées qui s’y rapportent. Si quelque chose semble suspect ou si vous souhaitez nettoyer la section À la une, vous pouvez supprimer le contenu promu en fonction des besoins.

Consultez [Contenu proposé](#featured-content) dans cet article pour obtenir des informations sur l’activation du contenu proposé.

## <a name="next-steps"></a>Étapes suivantes

[Administration de Power BI dans votre organisation](service-admin-administering-power-bi-in-your-organization.md)  
[Présentation du rôle d’administrateur Power BI](service-admin-role.md)  
[Audit de Power BI dans votre organisation](service-admin-auditing.md)  

D’autres questions ? [Essayez d’interroger la communauté Power BI](https://community.powerbi.com/)

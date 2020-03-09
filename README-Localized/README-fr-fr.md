---
page_type: sample 
products:
- office-365
- ms-graph
languages:
- swift
extensions:
  contentType: samples
  technologies:
  - Microsoft Graph
  - Azure AD
  - Microsoft identity platform
  services:
  - Office 365
  - Microosft identity platform
  platforms:
  - iOS
  createdDate: 1/27/2016 3:56:28 PM
---
# Exemple de connexion d’iOS à Microsoft Office 365 avec Microsoft Graph (Swift)

La connexion à Microsoft Office 365 est la première étape que chaque application iOS doit suivre pour commencer à travailler avec les données et services Office 365. Cet exemple explique comment connecter, puis appeler une API via Microsoft Graph.

> **Remarque :** Pour la version Objective-C de cet exemple, voir [O365-iOS-Microsoft-Graph-Connect](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample).

## Conditions préalables

- [Xcode](https://developer.apple.com/xcode/downloads/) version 10.2.1
- [CocoaPods](https://cocoapods.org)
- Un compte Office 365. Vous pouvez vous inscrire à [Office 365 Developer](https://aka.ms/devprogramsignup) pour accéder aux ressources dont vous avez besoin pour commencer à créer des applications Office 365.

## Connecter les exemples de fonctionnalités

Cet exemple illustre plusieurs appels REST vers le point de terminaison Microsoft Graph REST.

- [OBTENIR la photo de profil de l’utilisateur connecté](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/profilephoto_get) à partir du point de terminaison de l’*utilisateur*.
- DÉPOSER une demande pour [Télécharger la photo de profil dans le dossier racine OneDrive de l’utilisateur](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_put_content)
- PUBLIER une demande sur OneDrive pour [créer un lien de partage pour un élément de lecteur](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_createlink) pour accorder à l’accès à la photo téléchargée par un autre utilisateur
- PUBLIE une demande pour [envoyer un message électronique](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_sendmail) avec une photo en pièce jointe

## Enregistrement et configuration de l’application

1. Ouvrez un navigateur, accédez au [Centre d’administration Azure Active Directory](https://aad.portal.azure.com) et connectez-vous à l’aide d’un **compte personnel** (ou compte Microsoft) ou d’un **compte professionnel ou scolaire**.

1. Sélectionnez **Azure Active Directory** dans le volet de navigation gauche, puis sélectionnez **Inscriptions d’applications** sous **Gérer**.

1. Sélectionnez **Nouvelle inscription**. Sur la page **Inscrire une application**, définissez les valeurs comme suit.

    - Définissez le **Nom** sur `Exemple de connexion Swift REST `.
    - Définissez les **Types de comptes pris en charge** sur **Comptes figurant dans un annuaire organisationnel et comptes Microsoft personnels**.
    - Sous **URI de redirection**, remplacez la liste déroulante par **client public (mobile et bureau)** et définissez la valeur sur `msauth.com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST://auth`.

1. Choisissez **Inscrire**. Sur la page **Exemple de connexion Swift REST**, copiez la valeur de **ID d’application (client)** et enregistrez-la, car vous en aurez besoin à l’étape suivante.

### Mettez à jour l’exemple avec votre ID client

1. Ouvrez **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace**

1. Ouvrez **AuthenticationConstants.swift** et remplacez `<your-client-id>` par l’ID d’application que vous avez copié à l’étape précédente.

1. Exécutez l’exemple.

## Contribution

Si vous souhaitez contribuer à cet exemple, voir [CONTRIBUTING.MD](/CONTRIBUTING.md).

Ce projet a adopté le [code de conduite Open Source de Microsoft](https://opensource.microsoft.com/codeofconduct/). Pour en savoir plus, reportez-vous à la [FAQ relative au code de conduite](https://opensource.microsoft.com/codeofconduct/faq/) ou contactez [opencode@microsoft.com](mailto:opencode@microsoft.com) pour toute question ou tout commentaire.

## Questions et commentaires

Nous serions ravis de connaître votre opinion sur le projet Swift de connexion d’iOS à Office 365 avec Microsoft Graph. Vous pouvez nous faire part de vos questions et suggestions dans la rubrique [Problèmes](https://github.com/microsoftgraph/ios-swift-connect-rest-sample/issues) de ce référentiel.

Les questions générales sur le développement de Microsoft Graph doivent être publiées sur [Stack Overflow](http://stackoverflow.com/questions/tagged/MicrosoftGraph). Veillez à poser vos questions ou à rédiger vos commentaires en utilisant les tags \[MicrosoftGraph].

## Copyright

Copyright (c) 2017 Microsoft. Tous droits réservés.

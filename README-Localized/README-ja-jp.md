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
# Microsoft Graph を使った iOS 用 Microsoft Office 365 Connect サンプル (Swift)

各 iOS アプリで Office 365 のサービスとデータの操作を開始するため、最初に Microsoft Office 365 に接続する必要があります。このサンプルでは、Microsoft Graph 経由で接続を行い、1 つの API を呼び出す方法を示します。

> **注:**このサンプルの Objective-C バージョンについては、「[O365-iOS-Microsoft-Graph-Connect](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample)」を参照してください。

## 前提条件

- [Xcode](https://developer.apple.com/xcode/downloads/) バージョン 10.2.1
- [CocoaPods](https://cocoapods.org)
- Office 365 アカウント。Office 365 アプリのビルドを開始するために必要なリソースを含む [Office 365 Developer サブスクリプション](https://aka.ms/devprogramsignup)にサインアップできます。

## サンプル機能を接続する

このサンプルでは、Microsoft Graph REST エンドポイントに対する REST 呼び出しをいくつか例示します。

- [ユーザー](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/profilephoto_get) エンドポイントからの、*サインインしているユーザーのプロファイル画像の GET*。
- [ユーザーの OneDrive のルート フォルダーへプロファイル画像をアップロード](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_put_content)するための PUT 要求
- [ドライブ上のアイテムの共有リンクを作成](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_createlink)して他のユーザーがアップロードした写真にアクセスできるようにするための、OneDrive への要求の POST
- 写真の添付ファイル付きで[メール メッセージを送信](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_sendmail)するための要求の POST

## アプリを登録して構成する

1. ブラウザーを開き、[Azure Active Directory 管理センター](https://aad.portal.azure.com)に移動し、**個人用アカウント** (別名:Microsoft アカウント) か**職場または学校のアカウント**を使用してログインします。

1. 左側のナビゲーションで \[**Azure Active Directory**] を選択し、次に \[**管理**] で \[**アプリの登録**] を選択します。

1. **\[新規登録]** を選択します。\[**アプリケーションの登録**] ページで、次のように値を設定します。

    - \[**名称**] を、"`Swift REST Connect Sample`" にします。
    - \[**サポートされているアカウントの種類**] を \[**任意の組織のディレクトリ内のアカウントと個人用の Microsoft アカウント**] に設定します。
    - \[**リダイレクト URI**] で、ドロップ ダウンを \[**パブリック クライアント (モバイルとデスクトップ)**] に変更し、値を "`msauth.com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST://auth`" に設定します。

1. \[**登録**] を選択します。\[**Swift REST Connect Sample**] ページで、\[**アプリケーション (クライアント) ID**] の値をコピーして保存します。この値は次の手順で必要です。

### クライアント ID を使用してサンプルを更新する

1. **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace** を開きます。

1. **AuthenticationConstants.swift** を開き、`<your-client-id>` を、前の手順でコピーしたアプリケーション ID に置き換えます。

1. サンプルを実行します。

## 投稿

このサンプルに投稿する場合は、[CONTRIBUTING.MD](/CONTRIBUTING.md) を参照してください。

このプロジェクトでは、[Microsoft Open Source Code of Conduct (Microsoft オープン ソース倫理規定)](https://opensource.microsoft.com/codeofconduct/) が採用されています。詳細については、「[Code of Conduct の FAQ (倫理規定の FAQ)](https://opensource.microsoft.com/codeofconduct/faq/)」を参照してください。また、その他の質問やコメントがあれば、[opencode@microsoft.com](mailto:opencode@microsoft.com) までお問い合わせください。

## 質問とコメント

Office 365 iOS Microsoft Graph Connect Swift プロジェクトに関するフィードバックをお寄せください。質問や提案は、このリポジトリの「[問題](https://github.com/microsoftgraph/ios-swift-connect-rest-sample/issues)」セクションで送信できます。

Microsoft Graph 開発全般の質問については、「[Stack Overflow](http://stackoverflow.com/questions/tagged/MicrosoftGraph)」に投稿してください。質問やコメントには、必ず "MicrosoftGraph" とタグを付けてください。

## 著作権

Copyright (c) 2017 Microsoft.All rights reserved.

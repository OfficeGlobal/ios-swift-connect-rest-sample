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
# 使用 Microsoft Graph (Swift) 的 iOS 版 Microsoft Office 365 连接示例

连接到 Microsoft Office 365 是所有 iOS 应用开始使用 Office 365 服务和数据必须采取的第一步。本示例演示如何通过 Microsoft Graph 连接并调用一个 API。

> **注意：**有关此示例的 Objective-C 版本，请参阅 [O365-iOS-Microsoft-Graph-Connect](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample)。

## 先决条件

- [Xcode](https://developer.apple.com/xcode/downloads/) 版本 10.2.1
- [CocoaPods](https://cocoapods.org)
- Office 365 帐户。你可以注册 [Office 365 开发人员订阅](https://aka.ms/devprogramsignup)，其中包含你开始生成 Office 365 应用所需的资源。

## 连接示例功能

本示例将演示对 Microsoft Graph REST 终结点的多个 REST 调用。

- 从*用户*终结点[获取 (GET) 已登录用户的个人资料照片](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/profilephoto_get)。
- 通过 PUT 请求[将个人资料照片上传到用户的 OneDrive 根文件夹](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_put_content)
- 向 OneDrive 发布 (POST) 请求以[创建驱动器项的共享链接](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_createlink)，使其他用户可以访问已上传的照片
- 发布 (POST) 请求以[发送带照片附件的电子邮件](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_sendmail)

## 注册和配置应用

1. 打开浏览器，并导航到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)，然后使用**个人帐户**（亦称为“Microsoft 帐户”）或**工作/学校帐户**登录。

1. 选择左侧导航栏中的“Azure Active Directory”****，再选择“管理”****下的“应用注册”****。

1. 选择“新注册”****。在“**注册应用**”页面上，按如下方式设置值。

    - 将“**名称**”设置为 `Swift REST Connect Sample`。
    - 将“**受支持的帐户类型**”设置为“**任何组织目录中的帐户和个人 Microsoft 帐户**”。
    - 在“**重定向 URI**”中，将下拉列表更改为“**公共客户端(移动和桌面)**”，然后将值设为 `msauth.com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST://auth`。

1. 选择“**注册**”。在“**Swift REST Connect Sample**”页面上，复制并保存“**应用程序(客户端) ID**”的值，你将在下一步中用到它。

### 使用客户端 ID 来更新示例

1. 打开 **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace**

1. 打开 **AuthenticationConstants.swift** 并将 `<your-client-id>` 替换为上一步中复制的应用程序 ID。

1. 运行示例。

## 参与

如果想要参与本示例，请参阅 [CONTRIBUTING.MD](/CONTRIBUTING.md)。

此项目已采用 [Microsoft 开放源代码行为准则](https://opensource.microsoft.com/codeofconduct/)。有关详细信息，请参阅[行为准则 FAQ](https://opensource.microsoft.com/codeofconduct/faq/)。如有其他任何问题或意见，也可联系 [opencode@microsoft.com](mailto:opencode@microsoft.com)。

## 问题和意见

我们乐意倾听你有关 Office 365 iOS Microsoft Graph Connect Swift 项目的反馈。你可通过该存储库中的[问题](https://github.com/microsoftgraph/ios-swift-connect-rest-sample/issues)部分向我们发送问题和建议。

与 Microsoft Graph 开发相关的一般问题应发布到 [Stack Overflow](http://stackoverflow.com/questions/tagged/MicrosoftGraph)。请确保你的问题或意见标记有 \[MicrosoftGraph]。

## 版权信息

版权所有 (c) 2017 Microsoft。保留所有权利。

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
# Пример подключения Microsoft Office 365 для iOS с использованием Microsoft Graph (Swift)

Подключение к Microsoft Office 365 — это первый шаг, который должно выполнить каждое приложение для iOS, чтобы начать работу со службами и данными Office 365. В этом примере показано, как подключиться, а затем вызвать один API через Microsoft Graph.

> **Примечание.** Версию Objective-C этого примера см. в статье [O365-iOS-Microsoft-Graph-Connect](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample).

## Необходимые компоненты

- [Xcode](https://developer.apple.com/xcode/downloads/) версии 10.2.1.
- [CocoaPods](https://cocoapods.org)
- Учетная запись Office 365. Вы можете [подписаться на план Office 365 для разработчиков](https://aka.ms/devprogramsignup), который включает ресурсы, необходимые для создания приложений Office 365.

## Возможности примера подключения

В этом примере показано несколько вызовов REST в конечную точку REST в Microsoft Graph.

- [ПОЛУЧЕНИЕ фотографии профиля пользователя, выполнившего вход, ](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/profilephoto_get)с конечной точки*пользователя*.
- Запрос PUT для [отправки изображения профиля в корневую папку пользователя OneDrive](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_put_content)
- ПУБЛИКАЦИЯ запроса в OneDrive для [создания ссылки совместного доступа к элементу диска ](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_createlink) с целью предоставить доступ к отправленному изображению другому пользователю.
- ОТПРАВКА запроса для [отправки сообщения электронной почты ](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_sendmail) с изображением в приложении

## Регистрация и настройка приложения

1. Откройте браузер, перейдите в [Центр администрирования Azure Active Directory](https://aad.portal.azure.com) и войдите с помощью **личной учетной записи** (т. е.  учетной записи Майкрософт) или **рабочей или учебной учетной записи**.

1. Выберите **Azure Active Directory** на панели навигации слева, затем выберите **Регистрация приложения** в разделе **Управление**.

1. Выберите **Новая регистрация**. На странице **Регистрация приложения** задайте необходимые значения следующим образом:

    - Установите **Имя** как `Swift REST Connect Sample`.
    - Задайте для параметра **Поддерживаемые типы учетных записей** значение **Учетные записи в любом каталоге организации и личные учетные записи Майкрософт**.
    - В разделе **URI перенаправления** выберите в раскрывающемся списке **Общедоступный клиент (для мобильных и классических приложений)** и задайте значение `msauth.com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST://auth`.

1. Нажмите кнопку **Зарегистрировать**. На странице **Swift REST Connect Sample** скопируйте значение **Идентификатор приложения (клиента)** и сохраните его — оно потребуется на следующем этапе.

### Обновление примера внесением идентификатора клиента

1. Откройте **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace**.

1. Откройте **AuthenticationConstants.swift** и замените `<your-client-id>` на идентификатор приложения, скопированный на предыдущем этапе.

1. Запустите пример.

## Участие

Если вы хотите добавить код в этот пример, просмотрите статью [CONTRIBUTING.MD](/CONTRIBUTING.md).

Этот проект соответствует [Правилам поведения разработчиков открытого кода Майкрософт](https://opensource.microsoft.com/codeofconduct/). Дополнительные сведения см. в разделе [часто задаваемых вопросов о правилах поведения](https://opensource.microsoft.com/codeofconduct/faq/). Если у вас возникли вопросы или замечания, напишите нам по адресу [opencode@microsoft.com](mailto:opencode@microsoft.com).

## Вопросы и комментарии

Мы будем рады получить от вас отзывы о проекте приложения на Swift для iOS, подключающегося к Office 365 и использующего Microsoft Graph. Вы можете отправлять нам вопросы и предложения в разделе [Проблемы](https://github.com/microsoftgraph/ios-swift-connect-rest-sample/issues) этого репозитория.

Общие вопросы о разработке решений для Microsoft Graph следует задавать на сайте [Stack Overflow](http://stackoverflow.com/questions/tagged/MicrosoftGraph). Добавляйте тег \[MicrosoftGraph] к своим вопросам или комментариям.

## Авторские права

(c) Корпорация Майкрософт (Microsoft Corporation), 2017. Все права защищены.

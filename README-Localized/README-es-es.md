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
# Ejemplo de Connect de Microsoft Office 365 para iOS con Microsoft Graph (Swift)

Conectarse a Microsoft Office 365 es el primer paso que necesita realizar cada aplicación de iOS para empezar a trabajar con los datos y servicios de Office 365. En este ejemplo, se muestra cómo conectar y después realizar una llamada a una API con la API de Microsoft Graph.

> **Nota:** Para ver la versión para Objective-C de este ejemplo, consulte [O365-iOS-Microsoft-Graph-Connect](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample).

## Requisitos previos

- [Xcode](https://developer.apple.com/xcode/downloads/) Versión 10.2.1
- [CocoaPods](https://cocoapods.org)
- Una cuenta de Office 365. Puede registrarse para obtener [una suscripción a Office 365 Developer](https://aka.ms/devprogramsignup) que incluye los recursos que necesita para comenzar a crear aplicaciones de Office 365.

## Características de muestra de Connect

Este ejemplo muestra varias llamadas REST al punto de conexión de REST de Microsoft Graph.

- [Obtiene la foto de perfil del usuario que ha iniciado sesión](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/profilephoto_get) desde el punto de conexión *usuario*.
- Solicitud PUT para [cargar la foto de perfil a la carpeta raíz de OneDrive del usuario](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_put_content)
- ENVIAR una solicitud a OneDrive para [crear un vínculo para compartir para un elemento de unidad](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_createlink) para dar acceso a otro usuario a la foto cargada
- PUBLICA una solicitud para [enviar un mensaje de correo electrónico](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_sendmail) con una foto como dato adjunto

## Registrar y configurar la aplicación

1. Abra un explorador y vaya al [Centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: una cuenta de Microsoft) o una **cuenta profesional o educativa**.

1. Seleccione **Azure Active Directory** en el panel de navegación izquierdo y, después, **Registros de aplicaciones** en **Administrar**.

1. Seleccione **Nuevo registro**. En la página **Registrar una aplicación**, establezca los valores siguientes.

    - Establezca **Nombre** en `Swift REST Connect Sample`.
    - Establezca **Tipos de cuenta admitidos** en **Cuentas en cualquier directorio de organización y cuentas personales de Microsoft**.
    - En **URI de redirección**, cambie la lista desplegable a **Cliente público (móvil y escritorio)** y establezca el valor en `msauth.com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST://auth`.

1. Elija **Registrar**. En la página **Swift REST Connect Sample**, copie el valor del **Id. de aplicación (cliente)** y guárdelo. Lo necesitará en el paso siguiente.

### Actualizar el ejemplo con su Id. de cliente

1. Abra **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace**

1. Abra **AuthenticationConstants.swift** y reemplace `<your-client-id>` con el ID. de la aplicación que copió en el paso anterior.

1. Ejecute el ejemplo.

## Colaboradores

Si quiere hacer su aportación a este ejemplo, vea [CONTRIBUTING.MD](/CONTRIBUTING.md).

Este proyecto ha adoptado el [Código de conducta de código abierto de Microsoft](https://opensource.microsoft.com/codeofconduct/). Para obtener más información, vea [Preguntas frecuentes sobre el código de conducta](https://opensource.microsoft.com/codeofconduct/faq/) o póngase en contacto con [opencode@microsoft.com](mailto:opencode@microsoft.com) si tiene otras preguntas o comentarios.

## Preguntas y comentarios

Nos encantaría recibir sus comentarios sobre el proyecto Connect de Office 365 para iOS con Microsoft Graph (Swift). Puede enviarnos sus preguntas y sugerencias mediante la sección [Problemas](https://github.com/microsoftgraph/ios-swift-connect-rest-sample/issues) de este repositorio.

Las preguntas sobre el desarrollo de Microsoft Graph en general deben publicarse en [Stack Overflow](http://stackoverflow.com/questions/tagged/MicrosoftGraph). Asegúrese de que sus preguntas o comentarios estén etiquetados con \[MicrosoftGraph].

## Copyright

Copyright (c) 2017 Microsoft. Todos los derechos reservados.

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
# Exemplo de conexão com o Microsoft Office 365 para iOS usando o Microsoft Graph (Swift)

A primeira etapa para que os aplicativos iOS comecem a funcionar com dados e serviços do Microsoft Office 365 é estabelecer uma conexão com essa plataforma. Este exemplo mostra como conectar e chamar uma única API por meio do Microsoft Graph.

> **Observação:** Confira a versão Objective-C deste exemplo em [O365-iOS-Microsoft-Graph-Connect](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample).

## Pré-requisitos

- [Xcode](https://developer.apple.com/xcode/downloads/) versão 10.2.1
- [CocoaPods](https://cocoapods.org)
- Uma conta do Office 365. Inscreva-se para uma [Assinatura de Desenvolvedor do Office 365](https://aka.ms/devprogramsignup), que inclui os recursos necessários para começar a criação de aplicativos do Office 365.

## Exemplos de recursos de conexão

Este exemplo demonstra várias chamadas REST para o terminal REST do Microsoft Graph.

- [(GET) Obtém a foto do perfil do usuário conectado](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/profilephoto_get) do terminal do *usuário*.
- (PUT) Solicita [o upload da foto do perfil para a pasta raiz do OneDrive do usuário](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_put_content).
- (POST) Publica uma solicitação para o OneDrive para [criar um link de compartilhamento de um item da unidade](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/driveitem_createlink) para dar aos outros usuários acesso à foto carregada.
- (POST) Publica uma solicitação para [enviar um email](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_sendmail) com uma foto em anexo

## Registrar e configurar o aplicativo

1. Abra um navegador e navegue até o [centro de administração do Azure Active Directory](https://aad.portal.azure.com) e faça logon, usando uma **conta pessoal** (também conhecida como: Conta Microsoft) **Conta Corporativa ou de Estudante**.

1. Selecione **Azure Active Directory** na navegação à esquerda e, em seguida, selecione **Registros de aplicativos** em **Gerenciar**.

1. Selecione **Novo registro**. Na página **Registrar um aplicativo**, defina os valores da seguinte forma.

    - Defina **Nome** como `Exemplo de Swift REST Connect`.
    - Defina **Tipos de contas com suporte** para **Contas em qualquer diretório organizacional e contas pessoais da Microsoft**.
    - Em **URI de redirecionamento**, altere a lista suspensa para **Cliente público (celular e computador)** e defina o valor como `msauth.com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST://auth`.

1. Escolha **Registrar**. Na página **Swift REST Connect**, copie e salve o valor de **ID do aplicativo (cliente)** para usar na próxima etapa.

### Atualizar o exemplo com o ID do cliente

1. Abra **O365-iOS-Microsoft-Graph-Connect-Swift.xcworkspace**

1. Abra **AuthenticationConstants.swift** e substitua `<your-client-id>` pelo ID do aplicativo que você copiou na etapa anterior.

1. Execute o exemplo.

## Colaboração

Se quiser contribuir para esse exemplo, confira [CONTRIBUTING.MD](/CONTRIBUTING.md).

Este projeto adotou o [Código de Conduta de Código Aberto da Microsoft](https://opensource.microsoft.com/codeofconduct/).  Para saber mais, confira as [Perguntas frequentes sobre o Código de Conduta](https://opensource.microsoft.com/codeofconduct/faq/) ou entre em contato pelo [opencode@microsoft.com](mailto:opencode@microsoft.com) se tiver outras dúvidas ou comentários.

## Perguntas e comentários

Gostaríamos de saber sua opinião sobre o projeto Swift de conexão com o Office 365 para iOS usando o Microsoft Graph. Você pode enviar perguntas e sugestões na seção [Problemas](https://github.com/microsoftgraph/ios-swift-connect-rest-sample/issues) deste repositório.

As perguntas sobre o desenvolvimento do Microsoft Graph em geral devem ser postadas no [Stack Overflow](http://stackoverflow.com/questions/tagged/MicrosoftGraph). Não deixe de marcar as perguntas ou comentários com \[MicrosoftGraph].

## Direitos autorais

Copyright (c) 2017 Microsoft. Todos os direitos reservados.

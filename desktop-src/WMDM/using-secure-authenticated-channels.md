---
title: 使用安全驗證通道
description: 使用安全驗證通道
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media 裝置管理員，驗證
- 裝置管理員，驗證
- 桌面應用程式，驗證
- 服務提供者，驗證
- 程式設計指南，驗證
- 驗證 (authentication)
- Windows Media 裝置管理員，安全通訊
- 裝置管理員，安全通訊
- 桌面應用程式，安全通訊
- 服務提供者，安全通訊
- 程式設計指南，安全通訊
- 安全通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021077"
---
# <a name="using-secure-authenticated-channels"></a>使用安全驗證通道

Windows Media 裝置管理員提供兩個 helper 類別、適用于應用程式的 [CSecureChannelClient](csecurechannelclient-class.md) () 與服務提供者的 [CSecureChannelServer](csecurechannelserver-class.md) (，以及) 的一個介面 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (，藉以啟用元件之間的驗證和安全通訊。 這些會一起組成 API，以使用安全驗證通道 (SAC) 。 SAC 針對使用 Windows Media 裝置管理員的服務提供者或應用程式處理下列三項工作：

-   [元件驗證](component-authentication.md)
-   [加密和解密](encryption-and-decryption.md)
-   [訊息驗證](message-authentication.md)

應用程式或服務提供者必須處理元件驗證、加密和解密;訊息驗證是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式和服務提供者的一般工作**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





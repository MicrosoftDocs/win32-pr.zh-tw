---
title: 使用安全驗證通道
description: 使用安全驗證通道
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows媒體裝置管理員，驗證
- 裝置管理員，驗證
- 桌面應用程式，驗證
- 服務提供者，驗證
- 程式設計指南，驗證
- 驗證 (authentication)
- Windows媒體裝置管理員，安全通訊
- 裝置管理員，安全通訊
- 桌面應用程式，安全通訊
- 服務提供者，安全通訊
- 程式設計指南，安全通訊
- 安全通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a86eb364baca933eea1c81e587f99c9381786c5c3f62f2cefcfe3ceaed6e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124108"
---
# <a name="using-secure-authenticated-channels"></a>使用安全驗證通道

Windows媒體裝置管理員藉由提供兩個協助程式類別、適用于應用程式的 [CSecureChannelClient](csecurechannelclient-class.md) () 與服務提供者的 [CSecureChannelServer](csecurechannelserver-class.md) (，以及) 的一個介面 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (，來啟用元件之間的驗證和安全通訊。 這些會一起組成 API，以使用安全驗證通道 (SAC) 。 SAC 使用 Windows 媒體裝置管理員來處理服務提供者或應用程式的下列三項工作：

-   [元件驗證](component-authentication.md)
-   [加密和解密](encryption-and-decryption.md)
-   [訊息驗證](message-authentication.md)

應用程式或服務提供者必須處理元件驗證、加密和解密;訊息驗證是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式和服務提供者的一般工作**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





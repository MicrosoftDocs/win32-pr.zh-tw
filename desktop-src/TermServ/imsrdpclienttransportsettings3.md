---
title: IMsRdpClientTransportSettings3 介面
description: 定義遠端桌面閘道 (RD 閘道) server 的其他屬性。 |IMsRdpClientTransportSettings3 介面
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings3 介面遠端桌面服務
- IMsRdpClientTransportSettings3 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7680e27b0d67c9273e4f47da4725c0acab6d173c560bb5b288a30a96931d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606923"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>IMsRdpClientTransportSettings3 介面

定義遠端桌面閘道 (RD 閘道) server 的其他屬性。

## <a name="members"></a>成員

**IMsRdpClientTransportSettings3** 介面繼承自 [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)。 **IMsRdpClientTransportSettings3** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientTransportSettings3** 介面具有這些屬性。



| 屬性                                                                                                           | 存取類型           | 描述                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GatewayAuthCookieServerAddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | 讀取/寫入<br/> | 以 cookie 為基礎的驗證的伺服器位址。<br/>                                                                                       |
| [**GatewayAuthLoginPage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | 讀取/寫入<br/> | 用來驗證使用者的登入網頁位址。<br/>                                                                           |
| [**GatewayCredSourceCookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | 讀取/寫入<br/> | 指定認證來源是否以 cookie 為基礎。<br/>                                                                                       |
| [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | 讀取/寫入<br/> | 加密的驗證 cookie。<br/>                                                                                                      |
| [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | 讀取/寫入<br/> | [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)屬性的大小（以字元為單位）。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                    |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 定義為3D5B21AC-748D-41DE-8F30-E15169586BD4<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 






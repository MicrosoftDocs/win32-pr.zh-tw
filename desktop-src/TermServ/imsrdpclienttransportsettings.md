---
title: IMsRdpClientTransportSettings 介面
description: 管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。 |IMsRdpClientTransportSettings 介面
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings 介面遠端桌面服務
- IMsRdpClientTransportSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd2cbcdaba0a4324c4501339e972f8bb967f64716d1688cef7c3c38bb22b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771448"
---
# <a name="imsrdpclienttransportsettings-interface"></a>IMsRdpClientTransportSettings 介面

管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。

## <a name="members"></a>成員

**IMsRdpClientTransportSettings** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IMsRdpClientTransportSettings** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientTransportSettings** 介面具有這些屬性。



| 屬性                                                                                                          | 存取類型           | 描述                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**GatewayCredsSource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | 讀取/寫入<br/> | RD 閘道伺服器驗證方法。<br/>     |
| [**GatewayDefaultUsageMethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | 唯讀<br/>  | 預設的 RD 閘道使用方法。<br/>             |
| [**GatewayHostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | 讀取/寫入<br/> | RD 閘道伺服器的主機名稱。<br/>              |
| [**GatewayIsSupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | 唯讀<br/>  | 指出是否支援 RD 閘道。<br/>       |
| [**GatewayProfileUsageMethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | 讀取/寫入<br/> | RD 閘道設定檔使用方法。<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | 讀取/寫入<br/> | RD 閘道伺服器使用方法。<br/>              |
| [**GatewayUserSelectedCredsSource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | 讀取/寫入<br/> | 使用者指定的 RD 閘道認證來源。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 


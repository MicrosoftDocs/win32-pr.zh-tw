---
title: IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr 屬性
description: 以 cookie 為基礎的驗證的伺服器位址。
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- GatewayAuthCookieServerAddr 屬性遠端桌面服務
- GatewayAuthCookieServerAddr 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayAuthCookieServerAddr 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330a1ddb15d548988c23f8140ce848f7f68be5d1deb17fc51bd88eed23b9eec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000918"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a>IMsRdpClientTransportSettings3：： GatewayAuthCookieServerAddr 屬性

以 cookie 為基礎的驗證的伺服器位址。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a>屬性值

以 cookie 為基礎的驗證的新伺服器位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 






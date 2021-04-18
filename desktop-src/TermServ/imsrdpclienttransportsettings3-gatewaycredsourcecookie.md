---
title: IMsRdpClientTransportSettings3 GatewayCredSourceCookie 屬性
description: 指定認證來源是否以 cookie 為基礎。
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- GatewayCredSourceCookie 屬性遠端桌面服務
- GatewayCredSourceCookie 屬性遠端桌面服務，IMsRdpClientTransportSettings3 介面
- IMsRdpClientTransportSettings3 介面遠端桌面服務，GatewayCredSourceCookie 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968996"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a>IMsRdpClientTransportSettings3：： GatewayCredSourceCookie 屬性

指定認證來源是否以 cookie 為基礎。 如果認證來源是以 cookie 為基礎或為零，則會包含一個。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a>屬性值

**ULONG** 值，指定認證來源是否以 cookie 為基礎。

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

 

 






---
title: IMsRdpClientTransportSettings GatewayCredsSource 屬性
description: 指定或抓取遠端桌面閘道 (RD 閘道) 驗證方法。
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- GatewayCredsSource 屬性遠端桌面服務
- GatewayCredsSource 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayCredsSource 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384174"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>IMsRdpClientTransportSettings：： GatewayCredsSource 屬性

指定或抓取遠端桌面閘道 (RD 閘道) 驗證方法。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>屬性值

指定 RD 閘道驗證方法的 **ULONG** 變數。 此參數可以是下列其中一個值。

<dt>

TSC \_ PROXY \_ 認證 \_ 模式 \_ USERPASS (0) 
</dt> <dd>

使用 (NTLM) 的密碼做為 RD 閘道的驗證方法。

</dd> <dt>

TSC \_ PROXY \_ 認證 \_ 模式 \_ 智慧卡 (1) 
</dt> <dd>

使用智慧卡做為 RD 閘道的驗證方法。

</dd> <dt>

\_ \_ \_ \_ 所有 (4) 的 TSC PROXY 認證模式
</dt> <dd>

針對 RD 閘道使用任何驗證方法。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

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

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 






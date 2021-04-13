---
title: IMsRdpClientTransportSettings2 GatewayPreAuthRequirement 屬性
description: 指定或抓取遠端桌面閘道 (RD 閘道) 單次密碼 (OTP) 功能是否已啟用的設定。
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- GatewayPreAuthRequirement 屬性遠端桌面服務
- GatewayPreAuthRequirement 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayPreAuthRequirement 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509351"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>IMsRdpClientTransportSettings2：： GatewayPreAuthRequirement 屬性

指定或抓取遠端桌面閘道 (RD 閘道) 單次密碼 (OTP) 功能是否已啟用的設定。

啟用 OTP 時， **GatewayPreAuthRequirement** 會嘗試使用 [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) 屬性從網際網路 COOKIE 存放區查詢 otp cookie。 如果成功， **GatewayPreAuthRequirement** 會將 OTP cookie 傳送到防火牆伺服器 (例如，Microsoft Internet Security and 加速 \[ ISA \] server) 以進行預先驗證。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a>屬性值

如果設定為1，則會啟用 OTP 功能。 如果設定為0，則會停用 OTP 功能。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista SP1<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                    |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 






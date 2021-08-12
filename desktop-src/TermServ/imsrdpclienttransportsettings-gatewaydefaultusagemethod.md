---
title: IMsRdpClientTransportSettings GatewayDefaultUsageMethod 屬性
description: 遠端桌面閘道 (RD 閘道) 的預設使用方法。
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- GatewayDefaultUsageMethod 屬性遠端桌面服務
- GatewayDefaultUsageMethod 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayDefaultUsageMethod 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6403f319eaa79b9d140a3d75f9dd4f7625eced916ee907755c017d3e58a1767f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607419"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>IMsRdpClientTransportSettings：： GatewayDefaultUsageMethod 屬性

遠端桌面閘道 (RD 閘道) 的預設使用方法。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>屬性值

RD 閘道之預設使用方法的指標。 傳回 [**put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)和群組原則設定所設定之使用者設定的聯集。 如果 **put \_ GatewayUsageMethod ()** 沒有設定任何使用者設定， **get \_ GatewayDefaultUsageMethod ()** 將會傳回 [ **TSC \_ PROXY 模式偵測 \_ ] \_** 的預設值。

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

 

 






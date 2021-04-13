---
title: IMsRdpClientTransportSettings GatewayIsSupported 屬性
description: 指定是否支援遠端桌面閘道 (RD 閘道) 。
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- GatewayIsSupported 屬性遠端桌面服務
- GatewayIsSupported 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayIsSupported 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383885"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a>IMsRdpClientTransportSettings：： GatewayIsSupported 屬性

指定是否支援遠端桌面閘道 (RD 閘道) 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a>屬性值

指定是否支援 RD 閘道。

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

 

 






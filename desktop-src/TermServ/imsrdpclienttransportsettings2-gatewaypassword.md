---
title: IMsRdpClientTransportSettings2 GatewayPassword 屬性
description: 指定使用者提供的密碼，以連接到遠端桌面閘道 (RD 閘道) server。
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- GatewayPassword 屬性遠端桌面服務
- GatewayPassword 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayPassword 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508380"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a>IMsRdpClientTransportSettings2：： GatewayPassword 屬性

指定使用者提供的密碼，以連接到遠端桌面閘道 (RD 閘道) server。

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a>屬性值

使用者為了連接到 RD 閘道伺服器所提供的密碼。

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

 

 






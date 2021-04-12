---
title: IMsRdpClientTransportSettings2 GatewayCredSharing 屬性
description: 指定或抓取遠端桌面閘道 (RD 閘道) 認證共用功能是否已啟用的設定。
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- GatewayCredSharing 屬性遠端桌面服務
- GatewayCredSharing 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayCredSharing 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464581"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>IMsRdpClientTransportSettings2：： GatewayCredSharing 屬性

指定或抓取遠端桌面閘道 (RD 閘道) 認證共用功能是否已啟用的設定。 啟用此功能時，遠端桌面 ActiveX 控制項會嘗試使用相同的認證來驗證遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和 RD 閘道伺服器。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>屬性值

如果設定為1，則會啟用認證共用。 如果設定為零，則會停用認證共用。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

ActiveX 控制項會使用這個屬性來執行 RD 工作階段主機伺服器與 RD 閘道伺服器之間共用認證的單一提示。 認證共用不支援使用 [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) 或 [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)的 web 密碼共用。

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

 

 






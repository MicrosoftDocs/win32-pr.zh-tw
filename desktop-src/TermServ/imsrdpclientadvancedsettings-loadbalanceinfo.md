---
title: IMsRdpClientAdvancedSettings LoadBalanceInfo 屬性
description: 指定將放置在遠端桌面工作階段主機 (RD 工作階段主機) server 通訊協定連接順序中的 x.500 連接要求封包中的負載平衡 cookie。
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- LoadBalanceInfo 屬性遠端桌面服務
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，LoadBalanceInfo 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384309"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>IMsRdpClientAdvancedSettings：： LoadBalanceInfo 屬性

指定將放置在遠端桌面工作階段主機 (RD 工作階段主機) server 通訊協定連接順序中的 x.500 連接要求封包中的負載平衡 cookie。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>屬性值

新 cookie 的指標。 如需詳細資訊，請參閱「備註」一節。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

負載平衡路由器會使用負載平衡資訊，在使用 RD 工作階段主機伺服器的伺服器陣列時，為用戶端選擇最佳的伺服器。 RD 工作階段主機伺服器本身並不會使用此資訊，而且會捨棄它。

Cookie 會使用下列區分大小寫的語法：

**Cookie： msts =**_IpAddressAndPortNumber_ *_\\ r \\ n_*

其中 *IpAddressAndPortNumber* 是 IP 位址和埠號碼（以網路位元組順序排列）。

例如，用來存取 172.31.249.216 IP 位址的 cookie （埠號碼3389）如下所示：

**Cookie： msts = 3640205228.15629.0000 \\ r \\ n**

最後四個零是選擇性的，並保留。 最後一個小數點是必要的，如同尾端的回車和換行。 字串的長度（以字元為單位）必須是2的偶數倍數，因此如有需要，請加上空格。

如果未提供 cookie，預設值為 **cookie： mstshash =**_UserName_ *_\\ r \\ n_*。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                        |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                  |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 






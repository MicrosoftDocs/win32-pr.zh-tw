---
title: IMsRdpClientAdvancedSettings7 NetworkConnectionType 屬性
description: 取得或設定用戶端與伺服器之間使用的網路連接類型。 傳遞至伺服器的網路連接類型資訊，可協助伺服器根據網路連線類型調整數個參數。
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- NetworkConnectionType 屬性遠端桌面服務
- NetworkConnectionType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，NetworkConnectionType 屬性
- NetworkConnectionType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，NetworkConnectionType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969179"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>IMsRdpClientAdvancedSettings7：： NetworkConnectionType 屬性

取得或設定用戶端與伺服器之間使用的網路連接類型。 傳遞至伺服器的網路連接類型資訊，可協助伺服器根據網路連線類型調整數個參數。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>屬性值

網路連接類型。

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**連接 \_輸入 \_ 數據機** (1 (0x1) ) 


</dt> <dd>

數據機 (56 Kbps) 

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**連接 \_輸入 \_ 寬頻 \_ 低** (2 (0x2) ) 


</dt> <dd>

低速度寬頻 (256 Kbps 到 2 Mbps) 

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**連接 \_輸入 \_ 衛星** (3 (0x3) ) 


</dt> <dd>

附屬 (2 Mbps 至 16 Mbps，具有高延遲) 

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**連接 \_輸入 \_ 寬頻 \_ HIGH** (4 (0x4) ) 


</dt> <dd>

高速寬頻 (2 Mbps 至 10 Mbps) 

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**連接 \_輸入 \_ WAN** (5 (0x5) ) 


</dt> <dd>

廣域網路 (WAN)  (10 Mbps 或更高，且具有高延遲) 

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**連接 \_輸入 \_ LAN** (6 (0x6) ) 


</dt> <dd>

區域網路 (LAN)  (10 Mbps 或更高版本) 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 






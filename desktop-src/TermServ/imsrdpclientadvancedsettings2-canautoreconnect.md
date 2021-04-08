---
title: IMsRdpClientAdvancedSettings2 CanAutoReconnect 屬性
description: 指定當網路連線中斷時，用戶端控制項是否能夠自動重新連接到目前的會話。
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- CanAutoReconnect 屬性遠端桌面服務
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，CanAutoReconnect 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843108"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a>IMsRdpClientAdvancedSettings2：： CanAutoReconnect 屬性

指定當網路連線中斷時，用戶端控制項是否能夠自動重新連接到目前的會話。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a>屬性值

如果控制項能夠自動重新連接， **則接收 variant \_ TRUE** ，否則會傳回 **variant \_ FALSE** 。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

可能未啟用自動重新連線的情況包括：系統管理員使用群組原則來停用自動重新連線，以及不支援自動重新連接的舊版環境。

連接控制項時，無法設定這個屬性。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 定義為9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

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

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 






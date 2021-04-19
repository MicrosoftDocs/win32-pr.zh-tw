---
title: IMsRdpClientAdvancedSettings DisplayConnectionBar 屬性
description: 指定是否使用連接列。 預設值為 VARIANT \_ TRUE，可啟用屬性。
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- DisplayConnectionBar 屬性遠端桌面服務
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，DisplayConnectionBar 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967725"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a>IMsRdpClientAdvancedSettings：:D isplayConnectionBar 屬性

指定是否使用連接列。 預設值為 **VARIANT \_ TRUE**，可啟用屬性。 在安全腳本環境中將這個屬性設定為 **VARIANT \_ FALSE** ， **會傳回 E \_ FAIL**。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a>屬性值

將此參數設定為 **VARIANT \_ FALSE** ，以停用此功能或 **variant \_ TRUE** 來啟用此功能。 預設值為 **VARIANT \_ TRUE**。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

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

 

 






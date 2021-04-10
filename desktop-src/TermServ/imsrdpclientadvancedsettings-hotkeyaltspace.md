---
title: IMsRdpClientAdvancedSettings HotKeyAltSpace 屬性
description: 指定要新增至 ALT 的虛擬金鑰程式碼，以判斷 ALT + 空格鍵的熱鍵取代。
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- HotKeyAltSpace 屬性遠端桌面服務
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyAltSpace 屬性
- HotKeyAltSpace 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyAltSpace 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b257bd04171f8bff22bbe91ee7310fafe89c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934297"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a>IMsRdpClientAdvancedSettings：： HotKeyAltSpace 屬性

指定要新增至 ALT 的虛擬金鑰程式碼，以判斷 ALT + 空格鍵的熱鍵取代。

只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a>屬性值

新的虛擬金鑰程式碼。 **VK \_DELETE** 是預設值，以 ALT + DELETE 作為產生的順序。

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

 

 






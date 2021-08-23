---
title: IMsRdpClientAdvancedSettings HotKeyCtrlAltDel 屬性
description: 指定要新增至 CTRL + ALT 的虛擬金鑰程式碼，以決定 CTRL + ALT + DELETE 的熱鍵取代，也稱為 (SAS) 的安全注意順序。
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- HotKeyCtrlAltDel 屬性遠端桌面服務
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47975b2c4586728fc4727044b7340d87c275c5a5f47aac1c68ab3d9fdafbda6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424408"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a>IMsRdpClientAdvancedSettings：： HotKeyCtrlAltDel 屬性

指定要新增至 CTRL + ALT 的虛擬金鑰程式碼，以決定 CTRL + ALT + DELETE 的熱鍵取代，也稱為 (SAS) 的安全注意順序。

> [!Note]  
> CTRL + ALT + DELETE 絕不會重新導向至遠端伺服器，即使已啟用 [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性;CTRL + ALT + DELETE 是本機 SAS 序列。

 

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a>屬性值

新的虛擬金鑰程式碼。 **VK \_END** 是預設值。

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

 

 






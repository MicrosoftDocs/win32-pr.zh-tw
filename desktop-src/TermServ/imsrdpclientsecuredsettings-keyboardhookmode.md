---
title: IMsRdpClientSecuredSettings KeyboardHookMode 屬性
description: 指定鍵盤重新導向設定，指定套用 Windows 鍵盤快捷方式的方式和時機 (例如，ALT + TAB) 。
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- KeyboardHookMode 屬性遠端桌面服務
- KeyboardHookMode 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，KeyboardHookMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a291eeb26f8011440b8629ed46e1bb12c8b9cfb7adb937d33f80afe60a4d5cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657588"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>IMsRdpClientSecuredSettings：： KeyboardHookMode 屬性

指定鍵盤重新導向設定，指定套用 Windows 鍵盤快捷方式的方式和時機 (例如，ALT + TAB) 。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>屬性值

新的設定。 此參數可以是下列其中一個值。

<dt>

0
</dt> <dd>

只將金鑰組合套用到用戶端電腦的本機。

</dd> <dt>

1
</dt> <dd>

將金鑰組合套用到遠端伺服器。

</dd> <dt>

2
</dt> <dd>

只有在用戶端以全螢幕模式執行時，才將金鑰組合套用至遠端伺服器。 這是預設值。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

連接控制項時無法設定這些屬性。

如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings 定義為605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 






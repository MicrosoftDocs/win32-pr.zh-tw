---
description: 設定 appbar 的大小和螢幕位置。
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: 'ABM_SETPOS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861600"
---
# <a name="abm_setpos-message"></a>ABM \_ SETPOS 訊息

設定 appbar 的大小和螢幕位置。 此訊息會指定螢幕邊緣和 appbar 的周框。 系統可能會調整周框，讓 appbar 不會干擾 Windows 的工作列或其他任何透過像 appbars。


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。 **UEdge** 成員會指定螢幕邊緣，而 **rc** 成員會包含周框。 當 [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) 函式傳回時， **rc** 會包含已核准的周框。 傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge** 和 **rc** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="remarks"></a>備註

這則訊息會導致系統將 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息傳送至所有透過像 appbars。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 





---
description: 要求 appbar 的大小和螢幕位置。
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: 'ABM_QUERYPOS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f7a5e78b6b040904144a64e1068fea3a3e56c7b42fdfcf314f2ced4bfff9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225029"
---
# <a name="abm_querypos-message"></a>ABM \_ QUERYPOS 訊息

要求 appbar 的大小和螢幕位置。 提出要求時，訊息會提出 appbar 的螢幕邊緣和周框。 系統會調整周框，讓 appbar 不會干擾 Windows 的工作列或其他任何透過像 appbars。


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。 **UEdge** 成員會指定螢幕邊緣，而 **rc** 成員會包含建議的周框。 當 [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) 函式傳回時， **rc** 會包含已核准的周框。 傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge** 和 **rc** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="remarks"></a>備註

Appbar 應該會在傳送 [**ABM \_ SETPOS**](abm-setpos.md) 訊息之前傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 





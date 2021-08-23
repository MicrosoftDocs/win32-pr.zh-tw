---
title: 'NM_RDBLCLK (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父系，使用者在控制項內按兩下滑鼠右鍵。 此通知會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK (樹狀檢視) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da45d7ac3363a5dc362ef6d34255531f71ce780075e8106fb9579126298a1e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826068"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>NM \_ RDBLCLK (樹狀檢視) 通知碼

通知樹狀檢視控制項的父系，使用者在控制項內按兩下滑鼠右鍵。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零以防止預設處理，或零以允許預設處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






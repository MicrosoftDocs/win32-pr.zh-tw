---
title: 'NM_RCLICK (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- NM_RCLICK (樹狀檢視) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0cb27b37764090a778e2c3ba91f4dbaa807d9cd8cc4e48371f0b2839fda417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078902"
---
# <a name="nm_rclick-tree-view-notification-code"></a>NM \_ RCLICK (樹狀檢視) 通知碼

通知樹狀檢視控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RCLICK 

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



 

 






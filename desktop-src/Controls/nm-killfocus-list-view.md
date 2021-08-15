---
title: 'NM_KILLFOCUS (清單視圖) 通知碼 (Commctrl) '
description: 通知清單視圖控制項的父視窗，控制項已遺失輸入焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- NM_KILLFOCUS (清單視圖) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34335644af6e1657f6e50792e4d9d2477ad06306977d754d3757bb49ebbb799d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018846"
---
# <a name="nm_killfocus-list-view-notification-code"></a>NM \_ KILLFOCUS (清單視圖) 通知碼

通知清單視圖控制項的父視窗，控制項已遺失輸入焦點。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






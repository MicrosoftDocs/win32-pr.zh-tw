---
title: 'NM_RDBLCLK (狀態列) 通知碼 (Commctrl) '
description: 通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- NM_RDBLCLK (的狀態列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: d8aa5c754eed028d050f1f42ab6ab7ae652bfb3a3dc8bedb49df81357db6b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410679"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a>NM \_ RDBLCLK (狀態列) 通知碼

通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。 **DwItemSpec** 成員包含已按下之區段的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示滑鼠按一下已處理，並隱藏系統的預設處理。 傳回 **FALSE** 以允許按一下的預設處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






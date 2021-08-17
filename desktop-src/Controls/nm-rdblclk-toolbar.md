---
title: 'NM_RDBLCLK (工具列) 通知碼 (Commctrl) '
description: 通知控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- NM_RDBLCLK (工具列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 14d81fadafa6faa0a4375d9aa34e98bb22a0099f9d0cdabcdbe1a385317e5df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391528"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a>NM \_ RDBLCLK (工具列) 通知碼

通知控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知碼的相關資訊。 如果滑鼠已按下工具列專案， **dwItemSpec** 成員就會包含專案識別碼，而 **dwItemData** 成員會包含專案資料。 如果按一下工具列上的分隔符號或空白字元， **dwItemSpec** 成員會包含-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **FALSE** 以允許工具列控制項執行事件的預設處理，或傳回 **TRUE** 以防止控制項處理事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






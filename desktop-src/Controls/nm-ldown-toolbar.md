---
title: 'NM_LDOWN (工具列) 通知碼 (Commctrl) '
description: 通知工具列的父視窗已按下滑鼠左鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- NM_LDOWN (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf283e8b3e0d1ed780a80d5608849bc42f200b61a5a94692c0924cb2e6241a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919648"
---
# <a name="nm_ldown-toolbar-notification-code"></a>NM \_ LDOWN (工具列) 通知碼

通知工具列的父視窗已按下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_LDOWN

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

## <a name="remarks"></a>備註

此通知會在傳送 [TBN \_ 下拉式](tbn-dropdown.md) 通知碼之後傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






---
title: 'NM_RCLICK (工具列) 通知碼 (Commctrl) '
description: 當使用者按一下具有滑鼠右鍵的工具列時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- NM_RCLICK (工具列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 6464c30a031aa55aef94bccd3ab852720fb14403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967575"
---
# <a name="nm_rclick-toolbar-notification-code"></a>NM \_ RCLICK (工具列) 通知碼

當使用者按一下具有滑鼠右鍵的工具列時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RCLICK

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






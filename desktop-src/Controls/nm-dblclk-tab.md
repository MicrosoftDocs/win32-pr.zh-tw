---
title: 'NM_DBLCLK (] 索引標籤) 通知碼 (Commctrl) '
description: 通知索引標籤控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- NM_DBLCLK (] 索引標籤) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105455"
---
# <a name="nm_dblclk-tab-notification-code"></a>NM \_ DBLCLK (tab) 通知碼

通知索引標籤控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零以允許預設處理，或零以允許預設處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






---
title: 'NM_RETURN (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父視窗，控制項具有輸入焦點，而且使用者已按下該按鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- NM_RETURN (樹狀檢視) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934799"
---
# <a name="nm_return-tree-view-notification-code"></a>NM 傳回 \_ (樹狀檢視) 通知碼

通知樹狀檢視控制項的父視窗，控制項具有輸入焦點，而且使用者已按下該按鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RETURN

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






---
title: 'NM_SETCURSOR (ComboBoxEx) 通知碼 (Commctrl .h) '
description: 通知 ComboBoxEx 控制項的父視窗，控制項正在設定資料指標以回應 WM \_ SETCURSOR 訊息。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0f7c7ffc8459ae1da279b6e53329f894662dd6ae6f30888fd9bdbdf631fa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798988"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>NM \_ SETCURSOR (ComboBoxEx) 通知碼

通知 ComboBoxEx 控制項的父視窗，控制項正在設定資料指標以回應 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以讓控制項設定資料指標或非零值，以防止控制項設定資料指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


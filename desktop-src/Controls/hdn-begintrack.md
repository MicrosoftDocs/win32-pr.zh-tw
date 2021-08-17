---
title: 'HDN_BEGINTRACK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，使用者已開始拖曳控制項中的分隔線 (也就是說，當滑鼠游標位於標題控制項) 的分隔線上時，使用者按下滑鼠左鍵。
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4250f178c4e1e2322e1609159eabd2fbd99611c10420bb90ce7bd287c44a5d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170938"
---
# <a name="hdn_begintrack-notification-code"></a>HDN \_ BEGINTRACK 通知碼

通知標題控制項的父視窗，使用者已開始拖曳控制項中的分隔線 (也就是說，當滑鼠游標位於標題控制項) 的分隔線上時，使用者按下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及要拖曳其分割的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **FALSE** 以允許追蹤分隔，或為 **TRUE** 以防止追蹤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_BEGINTRACKW** (Unicode) 和 **HDN \_ BEGINTRACKA** (ANSI) <br/>             |



 

 






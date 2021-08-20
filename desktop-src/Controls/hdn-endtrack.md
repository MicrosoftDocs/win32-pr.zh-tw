---
title: 'HDN_ENDTRACK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，指出使用者已完成拖曳分隔線。 此通知碼以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59467874643ba3a57ebf65919366077e3c9031d2de317d74c94ad0d51b7304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006063"
---
# <a name="hdn_endtrack-notification-code"></a>HDN \_ ENDTRACK 通知碼

通知標題控制項的父視窗，指出使用者已完成拖曳分隔線。 此通知碼以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及已拖曳其分割的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_ENDTRACKW** (Unicode) 和 **HDN \_ ENDTRACKA** (ANSI) <br/>                 |



 

 






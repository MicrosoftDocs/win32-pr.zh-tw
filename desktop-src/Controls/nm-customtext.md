---
title: 'NM_CUSTOMTEXT (Commctrl 的通知碼) '
description: 通知控制項的父視窗有關自訂文字作業的相關資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512ccb6cd94ce680b9832c342696941d98c0e6543c319caeb89eb409de1fe73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018869"
---
# <a name="nm_customtext-notification-code"></a>NM \_ CUSTOMTEXT 通知碼

通知控制項的父視窗有關自訂文字作業的相關資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項會忽略傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






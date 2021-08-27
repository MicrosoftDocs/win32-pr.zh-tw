---
title: 'TTN_POP (Commctrl 的通知碼) '
description: 通知擁有者視窗即將隱藏工具提示。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- TTN_POP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3322da3ddbb677631a433e4cce1d2a9eb6e56c3484314026242f23c91c103f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109478"
---
# <a name="ttn_pop-notification-code"></a>TTN \_ POP 通知碼

通知擁有者視窗即將隱藏工具提示。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






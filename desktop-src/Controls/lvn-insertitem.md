---
title: 'LVN_INSERTITEM (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出已插入新專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c706c7329e192559cb307962e293f0bbf02109c81fcde177eb36d8d39e37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062148"
---
# <a name="lvn_insertitem-notification-code"></a>LVN \_ INSERTITEM 通知碼

通知清單視圖控制項的父視窗，指出已插入新專案。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。 **IItem** 成員會識別新的專案，而其他成員則為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






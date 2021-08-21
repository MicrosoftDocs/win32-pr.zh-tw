---
title: 'TBN_QUERYDELETE (Commctrl 的通知碼) '
description: 當使用者正在自訂工具列時，通知工具列的父視窗是否可從工具列中刪除按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a01d1322ce8461c5cdb53fc76cfc220bbb5d292dedbe589d8b6ada5a48756d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077882"
---
# <a name="tbn_querydelete-notification-code"></a>TBN \_ QUERYDELETE 通知碼

當使用者正在自訂工具列時，通知工具列的父視窗是否可從工具列中刪除按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。 **iItem** 成員包含所要刪除的按鈕之以零為起始的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示允許刪除按鈕，或傳回 **FALSE** 以防止刪除按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






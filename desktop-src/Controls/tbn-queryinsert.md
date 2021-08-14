---
title: 'TBN_QUERYINSERT (Commctrl 的通知碼) '
description: 當使用者正在自訂工具列時，通知工具列的父視窗是否可將按鈕插入指定按鈕的左邊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f741fd7cfa5c6f72405b10ba9678aed71f7cb2359743593f117b17c8ad1c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166958"
---
# <a name="tbn_queryinsert-notification-code"></a>TBN \_ QUERYINSERT 通知碼

當使用者正在自訂工具列時，通知工具列的父視窗是否可將按鈕插入指定按鈕的左邊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。 **iItem** 成員包含所要插入的按鈕之以零為起始的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示允許在指定按鈕之前插入按鈕，或傳回 **FALSE** 以防止插入按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






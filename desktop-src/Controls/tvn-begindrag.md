---
title: 'TVN_BEGINDRAG (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，表示正在起始涉及滑鼠左鍵的拖放操作。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95952ee42dfe8eb8dd1a46c66dcd452f41cbc9723fa175c2a0d1fc75056c31ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957917"
---
# <a name="tvn_begindrag-notification-code"></a>IZDEBSKI \_ BEGINDRAG 通知碼

通知樹狀檢視控制項的父視窗，表示正在起始涉及滑鼠左鍵的拖放操作。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。 **ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含在 **hItem**、 **state** 和 **lParam** 成員中拖曳之專案的相關有效資訊。 **PtDrag** 成員會指定滑鼠目前的螢幕座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

具有 [**電視 \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項不會傳送此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_BEGINDRAGW** (Unicode) 和 **izdebski \_ BEGINDRAGA** (ANSI) <br/>               |



 

 






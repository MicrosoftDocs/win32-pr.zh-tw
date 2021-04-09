---
title: 'TVN_ITEMEXPANDING (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，表示父專案的子專案清單即將展開或折迭。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934999"
---
# <a name="tvn_itemexpanding-notification-code"></a>IZDEBSKI \_ ITEMEXPANDING 通知碼

通知樹狀檢視控制項的父視窗，表示父專案的子專案清單即將展開或折迭。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。 **ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含有關 **hItem**、 **state** 和 **lParam** 成員中父專案的有效資訊。 **動作** 成員表示清單是要展開還是折迭。 如需可能值的清單，請參閱 [**TVM \_ 展開**](tvm-expand.md) 訊息的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以防止清單展開或折迭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_ITEMEXPANDINGW** (Unicode) 和 **izdebski \_ ITEMEXPANDINGA** (ANSI) <br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IZDEBSKI \_ ITEMEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 






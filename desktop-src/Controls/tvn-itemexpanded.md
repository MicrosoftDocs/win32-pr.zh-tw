---
title: 'TVN_ITEMEXPANDED (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，表示父專案的子專案清單已展開或折迭。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105947"
---
# <a name="tvn_itemexpanded-notification-code"></a>IZDEBSKI \_ ITEMEXPANDED 通知碼

通知樹狀檢視控制項的父視窗，表示父專案的子專案清單已展開或折迭。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。 **ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含有關 **hItem**、 **state** 和 **lParam** 成員中父專案的有效資訊。 **動作** 成員表示清單是否展開或折迭。 如需可能值的清單，請參閱 [**TVM \_ 展開**](tvm-expand.md) 訊息的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_ITEMEXPANDEDW** (Unicode) 和 **izdebski \_ ITEMEXPANDEDA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IZDEBSKI \_ ITEMEXPANDING](tvn-itemexpanding.md)
</dt> </dl>

 

 






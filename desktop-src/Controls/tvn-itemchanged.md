---
title: 'TVN_ITEMCHANGED (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，專案屬性已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d140346d66a87bd394bc5aa36555b8accedef56891e722a4b28272e22f804ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018646"
---
# <a name="tvn_itemchanged-notification-code"></a>IZDEBSKI \_ ITEMCHANGED 通知碼

通知樹狀檢視控制項的父視窗，專案屬性已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange)結構的指標，描述已變更的專案。 **UChanged** 成員設定為 TVIF \_ STATE。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果接受變更，則傳回 **FALSE** ，否則會傳回 **TRUE** 以防止變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_ITEMCHANGEDW** (Unicode) 和 **izdebski \_ ITEMCHANGEDA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IZDEBSKI \_ ITEMCHANGING](tvn-itemchanging.md)
</dt> </dl>

 

 






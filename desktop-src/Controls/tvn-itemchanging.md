---
title: 'TVN_ITEMCHANGING (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，專案屬性即將變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85416e22562720455da3e3c03c95b3cee25b5f0f7420a31250b244f47dab0caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957867"
---
# <a name="tvn_itemchanging-notification-code"></a>IZDEBSKI \_ ITEMCHANGING 通知碼

通知樹狀檢視控制項的父視窗，專案屬性即將變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

描述正在變更之專案的 [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) 結構指標。 **UChanged** 成員設定為 TVIF \_ STATE。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果接受變更，則傳回 **FALSE** ，否則會傳回 **TRUE** 以防止變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_ITEMCHANGINGW** (Unicode) 和 **izdebski \_ ITEMCHANGINGA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IZDEBSKI \_ ITEMCHANGED](tvn-itemchanged.md)
</dt> </dl>

 

 






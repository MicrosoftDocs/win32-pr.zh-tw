---
title: 'TVN_SELCHANGING (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，選取範圍即將從某個專案變更為另一個專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024984"
---
# <a name="tvn_selchanging-notification-code"></a>IZDEBSKI \_ SELCHANGING 通知碼

通知樹狀檢視控制項的父視窗，選取範圍即將從某個專案變更為另一個專案。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。 **ItemOld** 和 **itemNew** 成員包含目前所選項目和新選取專案的相關有效資訊。 **動作** 成員指出滑鼠或鍵盤動作是否會造成選取範圍變更。 如需可能值的清單，請參閱 [izdebski \_ SELCHANGED](tvn-selchanged.md) 通知碼的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以防止選取範圍變更。

## <a name="remarks"></a>備註

回應此通知碼時，應用程式不應該刪除取得或遺失選取專案的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_SELCHANGINGW** (Unicode) 和 **izdebski \_ SELCHANGINGA** (ANSI) <br/>           |



 

 






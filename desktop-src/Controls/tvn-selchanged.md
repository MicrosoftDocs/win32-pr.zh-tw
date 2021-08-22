---
title: 'TVN_SELCHANGED (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，選取範圍已從某個專案變更為另一個專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7708d797edebc8c2c0bf43b910aec4dc0a1d6ece1a8a535fdcac57e6b15d6e04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957777"
---
# <a name="tvn_selchanged-notification-code"></a>IZDEBSKI \_ SELCHANGED 通知碼

通知樹狀檢視控制項的父視窗，選取範圍已從某個專案變更為另一個專案。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。 **NMTREEVIEW** 結構的 **itemOld** 和 **itemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含先前選取之專案和新選取專案的相關資訊。 只有這些結構的 **mask**、 **hItem**、 **state** 和 **lParam** 成員有效。 在輸入時， **itemOld** 和 **itemNew** 所指定之 **TVITEM** 結構的 **stateMask** 成員是未定義的。 **NMTREEVIEW** 結構的 **action** 成員表示導致選取專案變更的動作類型。 它可能是下列其中一個值：



| 需求 | 值 |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | 按鍵。   |
| TVC \_ BYMOUSE    | 按一下滑鼠按鍵。 |
| TVC \_ 不明    | 未知。          |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_SELCHANGEDW** (Unicode) 和 **izdebski \_ SELCHANGEDA** (ANSI) <br/>             |



 

 






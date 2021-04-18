---
title: 'TVN_DELETEITEM (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，指出正在刪除專案。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465461"
---
# <a name="tvn_deleteitem-notification-code"></a>IZDEBSKI \_ DELETEITEM 通知碼

通知樹狀檢視控制項的父視窗，指出正在刪除專案。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。 **ItemOld** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其 **hItem** 和 **lParam** 成員包含有關正在刪除之專案的有效資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

如果 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **lParam** 成員指向您的應用程式所配置的記憶體，您可以在收到 izdebski \_ DELETEITEM 通知碼時釋放它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_DELETEITEMW** (Unicode) 和 **izdebski \_ DELETEITEMA** (ANSI) <br/>             |



 

 






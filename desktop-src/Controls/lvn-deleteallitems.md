---
title: 'LVN_DELETEALLITEMS (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示控制項中的所有專案即將刪除。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f76ec4deaf67c1448fab5054c05ea8ede79c0972061c8be8e4f36b2e40ef54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019126"
---
# <a name="lvn_deleteallitems-notification-code"></a>LVN \_ DELETEALLITEMS 通知碼

通知清單視圖控制項的父視窗，表示控制項中的所有專案即將刪除。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。 **IItem** 成員為-1，而其他成員為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要隱藏後續的 [LVN \_ DELETEITEM](lvn-deleteitem.md) 通知碼，請傳回 **TRUE**。

若要接收後續的 [LVN \_ DELETEITEM](lvn-deleteitem.md) 通知碼，請傳回 **FALSE**。

## <a name="remarks"></a>備註

當 [**lvm \_ DELETEALLITEMS**](lvm-deleteallitems.md) 通知程式碼損毀或收到 **lvm \_ DELETEALLITEMS** 訊息時，它會傳送該控制項。 如果 **LVM \_ DELETEALLITEMS** 未傳回 **TRUE**，則此控制項也會在每個專案遭到刪除時，傳送 [LVN \_ DELETEITEM](lvn-deleteitem.md) 通知碼。

如果 [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) 訊息處理常式位於對話方塊程式中，請從對話方塊程式傳回 **TRUE** ，並使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 來設定訊息傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


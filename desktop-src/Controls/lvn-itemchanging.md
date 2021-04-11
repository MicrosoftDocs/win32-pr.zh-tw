---
title: 'LVN_ITEMCHANGING (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出專案正在變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935168"
---
# <a name="lvn_itemchanging-notification-code"></a>LVN \_ ITEMCHANGING 通知碼

通知清單視圖控制項的父視窗，指出專案正在變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標，該結構會識別專案並指定其屬性的變更。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以防止變更，或傳回 **FALSE** 以允許變更。

## <a name="remarks"></a>備註

如果清單視圖控制項有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式， \_ 則不會傳送 LVN ITEMCHANGING 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





